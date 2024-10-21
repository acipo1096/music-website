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

### The Website

The website was built using Joomla5! Even though I could have coded the site from scratch (and may migrate to doing that one day), I wanted something I could launch quickly instead of spending time writing code. I also wanted to get more hands-on experience being in control of a CMS, as opposed to limits to access at work.

### Hardware & Operating System

The server is hosted on an old Lenovo Tiny PC. I installed Proxmox on that machine and created two VMs:
- One VM running Ubuntu Server, which hosts the Joomla! and necessary MySQL database in separate Docker containers
- Another VM running Ubuntu Server and NGINX, which proxies the requests to my website to the VM hosting the site.
