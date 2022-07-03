---
title: "Dwinhmi"
date: 2022-07-03T14:06:55+05:30
lastmod: 2022-07-03T14:06:55+05:30
draft: true
keywords: []
description: "Using DWIN HMI Software"
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

# Setup

![setup](/images/post/dwinsetup.jpeg)
I bought DWIN COF 4.3 inch display from [robu](https://robu.in/product/dwin-tn-resistive-touch-4-3-inch-cof-display/) along with [HDL66A](https://robu.in/product/debugging-hdl662s-adapter-board/) adapter board. These 2 connected to PC USB port with male to male USB cable.

Default HMI interface is in chinease and I want to use my own UI.

# Development Tools

# Demo project
I downloaded [Demo GUI](https://www.electroniclinic.com/dmg80480c043_02wtc-touch-screen-getting-started-tutorial/)

Using tutorial when I tried to download project as is, it was not successful. But then I made sure resolution
is changed to matching with my COF display (480 * 272) I was able download files and see change in factory 
programmed UI.

Next task is to download through SD card.

# Formatting SD card
SD card size limitations as per documentation in 1 to 16 GB. For my system
card was on D drive hence I issued folloing command

```
FORMAT d:/fs:fat32/a:4096 
```

This took almost 10 minutes or more to format 16 GB of card.

