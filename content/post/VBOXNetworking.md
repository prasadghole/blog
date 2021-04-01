---
title: "Virtual Box Networking"
date: 2021-03-27T23:59:06+05:30
lastmod: 2021-03-27T23:59:06+05:30
draft: true
keywords: []
description: "Host to guest networking access with VirtualBox"
tags: ["Networking"]
categories: ["Development"]
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

# Network Settings
VirtualBox provide multiple ways to connect guest to host OS along with external 
internet acsess. I have summarized high level configuration with respect to access
to internet and host environment.

| Type              | Internet Access | Guest Acess | Host Access | IP Address  |
|-------------------|-----------------|-------------|-------------|-------------|
| NAT               | Yes             | No          | No          | Auto DHCP   |
| NAT Network       | Yes             | No          | No          | Auto DHCP   |
| Bridged Adapter   | Yes             | Yes         | Yes         | Auto/manual |
| Internal Network  | No              | No          | No          | Auto/manual |
| Host-only Adapter | No              | No          | Yes         | Auto/manual |
| Generic Drive     |                 |             |             |             |

[Referance 1](https://www.nakivo.com/blog/virtualbox-network-setting-guide/)

## NAT
This is very basic default confiugration used for access to internet connection
to host.
