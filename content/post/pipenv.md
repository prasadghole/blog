---
title: "Pipenv uncomplicated package manager for python"
date: 2022-08-27T11:58:18+05:30
lastmod: 2022-08-27T11:58:18+05:30
draft: true
keywords: []
description: "Creating and managing virtual environments in python"
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

# Installation
Well we need pip only at startup.
```shell
pip install pipenv
```

# Usage
Starting blank virtual environment 
As I using both python2 and 3 its better to specify version

```shell
pipenv shell --three
```

Once created we can verify current installed pip packages
```shell
pipenv graph
```

This should return empty in case we start from fresh python install
else will show packages installed in base interpreter from which
this new environment is created.
