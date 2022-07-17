---
title: "Vpssetup"
date: 2022-07-12T01:08:58+05:30
lastmod: 2022-07-12T01:08:58+05:30
draft: true
keywords: []
description: ""
tags: []
categories: []
author: ""

# You can also close(false) or open(true) something for this content.
# P.S. comment can only be closed
comment: false
toc: false
autoCollapseToc: false
postMetaInFooter: false
hiddenFromHomePage: false
# You can also define another contentCopyright. e.g. contentCopyright: "This is another copyright."
contentCopyright: false
reward: false
mathjax: false
mathjaxEnableSingleDollar: false
mathjaxEnableAutoNumber: false

# You unlisted posts you might want not want the header or footer to show
hideHeaderAndFooter: false

# You can enable or disable out-of-date content warning for individual post.
# Comment this out to use the global config.
#enableOutdatedInfoWarning: false

flowchartDiagrams:
  enable: false
  options: ""

sequenceDiagrams: 
  enable: false
  options: ""

---

<!--more-->

# VPS setup 
This page document various steps and tasks performed to manage my own vps server. I choose
VPS service from hostinger.

## Initial setp
After registering and payment, I logged in and started server instance. I choose non default
ubuntu os. (Centos was default)

I added my personal public ssh key to account. 

## SSH connection
[Reference](https://www.hostinger.in/tutorials/getting-started-with-vps-hosting)
Once started on vps manage page you will see ip address of my vps machine.

I ssh into it.

## Web Server
Apache was pre installed on this machine. Hence when I types ip address I was able to default 
http page. Next task is convert this to https only secured website.

## Creating new non root user
```
adduser usename
usermod -aG sudo usrname
```

SSH access for new user
```
su - username
mkdir .ssh
chmod 700 .ssh

```

Create public private key pair or use existing public key. I used my existing
public key as

```
scp ~/.ssh/id_rsa.pub username@hostname:/home/username/.ssh
```

On VPS server

```
~/home/username/.ssh/id_rsa.pub >> authorized_keys
```


### Creating git user
To use VPS as git server I have created git user with 
[setting up git server](https://git-scm.com/book/en/v2/Git-on-the-Server-Setting-Up-the-Server)


## Hosting web site
My current vps support apache webserver as default. File served from 
/var/www/html.index is my home page.

## Domain name in direction

## Setting up https secured access

Login to remote server with non root user
```
sudo apt install software-properties-common
sudo add-apt-repository ppa:certbot/certbot

sudo apt update
sudo apt install certbot python3-certbot-apache

```

# References
1. https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-22-04#step-5-setting-up-virtual-hosts-recommended
2. https://www.digitalocean.com/community/tutorials/how-to-secure-apache-with-let-s-encrypt-on-ubuntu-22-04
