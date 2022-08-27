---
title: "Python for embedded software modelling"
date: 2022-07-06T14:56:38+05:30
lastmod: 2022-07-06T14:56:38+05:30
draft: false
keywords: []
description: ""
tags: []
categories: []
author: "Prasad Ghole"

# You can also close(false) or open(true) something for this content.
# P.S. comment can only be closed
comment: false
toc: True
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

# Why Python?
Quick prototyping and availability of rich library set makes easy to model
embedded software in python. Current scope of this blog post is to modelling
embedded software and not embedded system.

# Architectural patterns
[pypubsub](https://pypubsub.readthedocs.io) is suitable for simulating decoupled
system using observer pattern. Hierarchical topic pattern gives more structured
view to design and build decoupled system.

[rxpy](https://rxpy.readthedocs.io/en/latest/) is more natural pattern for 
modelling embedded systems as it a reactive framework.

# Basic building blocks
Below sections I am exploring many alternative approaches, which may not bind
to above mentioned Architectural patterns. 

## Timers
This is most fundamental unit of embedded system. On windows OS we can use
win32event module to generate timing events. Based on these events as basic
timer tick we can run or simulate the embedded system.

We need to use thread and win32event to create an actor which will wait for
timer event and execute function or in case of reactive system emit message.

```python

fromm threading import Thread
import win32event

class TimerEventGenerator(Thread):
  def __init__(self,period):
    super(TimerEventGenerator,self).__init__()
    self.period = period
    self.event = win32event.CreateWaitableTimer(None,False,None)
    self.stoprequest = False

  def Start(self):
    win32event.SetWaitableTimer(self.event.handle,0,self.period,None,None,None)

  def run(self):
    while not self.stoprequest:
      win32event.WaitForSingleObject(self.event.handle,self.period)
      print("Do your work")ku

t = TimerEventGenerator(1000)

t.start()


```



