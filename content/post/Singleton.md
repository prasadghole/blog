---
author: "Prasad Ghole"
date: 2019-07-29
linktitle: SingleTon
menu:
  main:
    parent: tutorials
next: /tutorials/github-pages-blog
prev: /tutorials/automated-deployments
title: SingleTon class
weight: 10
---
SingleTon pattern is used to create only single instance of class object system wide. There are many possible
implementation ways to implemente it. 
```
    class SingleTon {
  public:
  static SingleTon & GetInstance
  {
  static SingleTon instance;
  return instance;
  }
  private:
  SingleTon() {
  /*Default constructor */
  }

  }
```
In above implementation why can't we simply create static function instead of create class objects. We need instance semantics
in case we need to pass this object as callback. This is true in case of QT singnals and slot mechanism.
