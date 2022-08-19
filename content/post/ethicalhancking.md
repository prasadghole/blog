---
title: "Ethical Hacking"
date: 2022-08-19T16:13:11+05:30
lastmod: 2022-08-19T16:13:11+05:30
draft: true
keywords: []
description: ""
tags: []
categories: []
author: "Prasad Ghole"

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

My notes on setting up home labs for ethical hacking from book "Ethical Hacking" by
Daniel G. Graham.

# Setup

![Setup](/images/post/ethhack_1.jpg)
## Virtual box
## pfSense
This router firewall will prevent our machines from outside attacks.

Downloaded the image [from](https://www.pfsense.org/download://www.pfsense.org/download/)
install as regular virtual machine.

### Installation
During OS installation select Auto (UFS) BIOS option.

### System Configuration 
- RAM 1024
- Hard Disk 5 GB

### network configuration 
- Adapter 1 Bridge network
- Adapter 2 Internal network

### Installation Success

![Setup](/images/post/VirtualBox_PFSense_Boot.png)

## Install metasploitable

Download [from](https://sourceforge.net/projects/metasploitable/files/latest/download)
This is pre built virtual box image hence only machine need to be created and no new
VDI need to be created.


### network configuration 
- Adapter 1 Internal network Name = Internal LAN

### Credentials 
- Username msfadmin
- password msfadmin

![Boot](/images/post/VirtualBox_Metasploitable.png)

## KALI Linux
This is our main source of penetration test client.

![Kali boot](/images/post/VirtualBox_KALI.png)

