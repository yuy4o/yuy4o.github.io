---
title: Python Decorators
author: yuyao
date: 2023-11-27 15:21:20 +0800 
categories: [Projects, python]
tags: [python]
---

### 调试代码

```python
import time

def login(func):
    def warpper(string):
        func(string)
        print('login')

    return warpper

def timeget(func):
    def war(string):
        print(time.time())
        func(string)

    return war
@login
@timeget

def f1(string):
    print('1.this is ', string)

@timeget
@login
def f2(string):
    print('2.this is ', string)

f1('asad')
f2('asad')
```
### 输出结果
```shell
1701069790.3941672
1.this is  asad
login
1701069790.3941672
2.this is  asad
login
```