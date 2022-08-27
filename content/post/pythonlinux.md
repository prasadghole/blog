---
title: "Pythonlinux"
date: 2022-08-27T12:07:31+05:30
lastmod: 2022-08-27T12:07:31+05:30
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

# Development environment on WSL2 Debian

It comes with python 2 pre installed, hence updated to python 3
```shell
sudo apt install python3

sudo install pip

```


# Vim Plugins
## Python support in VIM
Most of default vim comes with no inbuilt python support. Hence we may have to 
build the vim from source code. You comleteme plugin has very good documented 
steps to build it.
[Build VIM](https://github.com/ycm-core/YouCompleteMe/wiki/Building-Vim-from-source)


[pymode](https://github.com/python-mode/python-mode) is sufficient for complete
python development. It almost make as python IDE. I can run the scripts directly
using *Pymoderun* 


