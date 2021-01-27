+++
author = "Prasad Ghole"
date = 2020-08-25
title = "Be careful with pointers"

tags = [
"C",
]

categories = [
"development",
]
+++

Pointers in C/C++ are dual edge swords provide low level control over 
memory and hardware. This call for very careful usage which may lead 
to following problems.

## Memory leak
When pointer is made invalid without releasing actual memory pointed by
memory pointer on heap. This cause memory not getting reused even though
its available.


