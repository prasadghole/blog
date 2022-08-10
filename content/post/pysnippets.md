---
title: "Python snippets"
date: 2022-07-26T14:14:57+05:30
lastmod: 2022-07-26T14:14:57+05:30
draft: false
keywords: []
description: "Regular python snippets"
tags: []
categories: []
author: "Prasad Ghole"

# You can also close(false) or open(true) something for this content.
# P.S. comment can only be closed
comment: True
toc: True
autoCollapseToc: True
postMetaInFooter: True
hiddenFromHomePage: True
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

# Python snippets
As a embedded C programmer more prone to imperative style of programming, 
python provide more declarative, abstract and compact coding style. 

This post summarises the various coding snippet for handy shortcut notations
or templates.

## List Comprehensions 
```python
numbers = [1,2,3,4,5,6,7,8]    
```


```python
squares = []

for n in numbers:
  squares.append(n*n)

  print(squares)
```

[1, 4, 9, 16, 25, 36, 49, 64]



```python
numbers = [1,2,3,4,5,6,7,8]
sqaures = [n*n for n in numbers]
print(squares)
```

[1, 4, 9, 16, 25, 36, 49, 64]

```python

```

## Generators
```python
def genrate_seq(start,end):
  while start < end :
    start = start + 2

    if start > end:
      break

    yield start

    return 


g = genrate_seq(2,100)

try:
  while True:
    print(next(g))
except:
  print('stop')
```

```python
81
83
85
87
89
91
93
95
97
99
stop
```

## Reactive programming

Basic observable example for version 3 of RxPy. 
```python
import sys
import  rx

print("RX module version{0} ".format(rx.__version__))
# Create observable
argv = rx.from_(sys.argv)

#subscribe to observable for event stream
argv.subscribe(on_next = lambda i: print("Received {0}".format(i)),
               on_error= lambda i: print("Received Error{0}".format(i)),
                             on_completed=lambda : print("Complete"))
```

