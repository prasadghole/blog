---
title: "Whats in C Object name?"
date: 2021-03-21T23:11:48+05:30
lastmod: 2021-03-21T23:11:48+05:30
draft: false
keywords: []
description: "C objects names to avoid "
tags: ["Programming",]
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
# C Objects Naming
Although we know the common resrtictions on naming identifiers like it should not start with number. There ar some substle
conventions we need to know. In this post I will note down those along with reasons behind these.

# Underscore
C compliler will not complain if we name identifiers starting with underscore, but it can create issues with portability
as C standard reserve the use of it by for naming new additional C keywords. Like 
```
_Bool
```

This is a new datatype introduced by C99 standard. Indetifier starting with underscore followed by Capitol letter or another
underscore can or will be reserved keyword in future.

# _t (Underscore t)
When we define our own typedefs generally we follow the conventions of using postfix **underscore t**
We should avoid this as C standard reserves all the identifiers matching patterns 

```
int[0-9a-z_]_t

uint[0-9a-z_]_t

```
