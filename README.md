# Music Website
Built a website to create an online presence for my music and show knowledge of different tech skills, including Content Management Systems (CMS), web hosting, server security, and DNS. (https://alexfloydmusic.com)

## Motivation

As a musician in several bands and as a solo cover artist, I had been meaning to build a website just as another way to market myself. I decided to create and host the website myself for two reasons: so I could save money on paying for a cloud service such as AWS (where the fees you pay can sometimes be unpredictable, even if you use their built-in billing tools), and so I could get some more hands-on experience with servers.

## Tech Stack

The following technologies were used to create and host the website:
- Joomla!
- MySQL
- PHP
- Docker
- NGINX
- Ubuntu Server
- Proxmox
- AWS Route 53

### The Website

The website was built using Joomla5! Even though I could have coded the site from scratch (and may migrate to doing that one day), I wanted something I could launch quickly instead of spending time writing code. I also wanted to get more hands-on experience being in control of a CMS, as opposed to limits to access at work.

### Hardware & Operating System

The server is hosted on an old Lenovo Tiny PC. I installed Proxmox on that machine and created two VMs:
- One VM running Ubuntu Server, which hosts the Joomla! and necessary MySQL database in separate Docker containers
- Another VM running Ubuntu Server and NGINX, which proxies the requests to my website to the VM hosting the site.
- For security reasons, I decided to place my server behind a different router. The VMs and web configurations can currently only be accessed if I connect a laptop directly to a router port. I used a TP-Link Omada Router for this purpose. (For the cost and purpose based on research, I decided to go with this router. I know, through my research, that TP-Link is not recommended in a business or enterprise setting.)

### Containers
3 separate Docker containers are used: one for Joomla, one for MySQL, and a third to host a custom "Song Requests" application that I built. See (https://github.com/acipo1096/song-requests). My sceond web server running NGINX proxies the appropriate requests to each container and port.

## Design
The website is currently made up of 5 pages
- A home page
- A page dedicated to my upcoming performances (solo and with a band)
- An "About Me" page, detailing my bio and musical influences
- A page that lists the bands I'm currently a part of
- A Contact page so people can send me an email through the website
