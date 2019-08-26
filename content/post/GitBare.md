---
author: "Prasad Ghole"
date: 2019-07-29
linktitle: Git in a box
menu:
  main:
    parent: tutorials
next: /tutorials/github-pages-blog
prev: /tutorials/automated-deployments
title: Vim Tips
weight: 10
---
# Git in a box 
Github is certailnly a good source of keeping master copy of your decentralized git repo. But in some 
secret project thing it would be much better to have git repository as portable copy.This is where 
git bare repository helps.

## bare repository
A bare repository is one without working copy. We can push or pull our changes to/from this repo. We
can keep this repository portable and handy. Can be mount on shared drive and your github is done.
```
git init --bare 
```

## Using bare repository




