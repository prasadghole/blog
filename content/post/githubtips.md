---
title: "Github Tips"
date: 2021-04-06T02:37:08+05:30
lastmod: 2021-04-06T02:37:08+05:30
draft: false
type: post
keywords: []
description: ""
tags: ["git"]
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

# Using multiple github with ssh
I used this with my Conemulator
```
exec ssh-agent bash
eval ssh-agent -s
ssh-add ~/.ssh/xxxxxxxxx*

```

# Configure beyond compare as diff tool
``` shell
git config --global diff.tool bc
git config --global difftool.bc.path "C:\Program Files\Beyond Compare 4\BComp.exe"
git config --global merge.tool bc
git config --global mergetool.bc.path "C:\Program Files\Beyond Compare 4\BComp.exe"
git config --global alias.mydiff "difftool --dir-diff --tool=bc --no-prompt"
```
[Thanks To aaronhoffman](https://gist.githubusercontent.com/aaronhoffman/60536ceb0812ce0ab0f594ae2e78f475/raw/3351b12fc0564831e17d814dac003bae80768429/git-bc.cmd)