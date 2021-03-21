---
title: "Not a Volatile - Restrict"
date: 2021-03-22T00:11:46+05:30
lastmod: 2021-03-22T00:11:46+05:30
draft: false
keywords: []
description: " Restrict keyword in C"
tags: ["Programming"]
categories: []
author: "Prasad Ghole"

# You can also close(false) or open(true) something for this content.
# P.S. comment can only be closed
comment: false
toc: true
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

# restrict type qualifier
C99 introduced new C only **restrict** keyword. It does exactly opposite work of 
**volatile**  keyword but with very few restricted use cases. It applies only to
pointers to objects. 

Objects indirectly accessed by pointers cannot be optimized 
by compiler due to potential aliasing, which may occur when more than one pointer
can point to same object.
Due to this compiler may or may not optimize the code. 

# Use case
As mentioned above by using restrict keyword we can tell compiler to optimize use
of parameters of function accessing restricated objects via pointers.

```
void f(unsigned int n, int * restrict p, int * restrict q) {
  while (n-- > 0) {
    *p++ = *q++;
  }

```

Here programmer is telling compiler that obects accessed by pointer p and q are 
accessing different objects in memory.

But remember it is the programmers responsibility to make sure above statement is 
correct else undefined behaviour can happen due to optimization.

# Demo
```

int foo(int *a, int *b)
{
    *a = 5;
    *b = 6;
    return *a + *b;
}
 

```

## Results
![Optimized functions ](/images/post/restrict.png)

As we can see function rfoo has optimized the use of pointers and placed
direct results in register eax.
