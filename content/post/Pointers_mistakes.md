---
author: "Prasad Ghole"
date: 2019-09-11
linktitle: Be careful with pointers
menu:
  main:
    parent: tutorials
next: /tutorials/github-pages-blog
prev: /tutorials/automated-deployments
title: Be careful with pointers
weight: 10
---

Pointers in C/C++ are dual edge swords provide low level control over 
memory and hardware. This call for very careful usage which may lead 
to following problems.

## Memory leak
When pointer is made invalid without releasing actual memory pointed by
memory pointer on heap. This cause memory not getting reused even though
its available.


