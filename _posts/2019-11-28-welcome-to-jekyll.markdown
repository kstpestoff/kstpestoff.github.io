---
layout: post
mathjax: true
title:  "Welcome to Jekyll!"
date:   2019-11-28 16:21:51 +0300
categories: jekyll update
---
***Заметка 2***
```python
map(sum, M)
```

Отображение множества M функционалом sum в новое множество. [Функциональное_программирование](https://ru.m.wikipedia.org/wiki/Функциональное_программирование) - основа python
#python 

***Заметка 3***
Числа, строки и кортежи неизменяемые, а списки, словари и множества - нет.
```python
>>> s='fraunghofer'
>>> s[1]
'r'
>>> s[1]='l'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
```
Только через list
```python
>>> L=list(s)
>>> L
['f', 'r', 'a', 'u', 'n', 'g', 'h', 'o', 'f', 'e', 'r']
>>> L[1] = 'L'
>>> L
['f', 'L', 'a', 'u', 'n', 'g', 'h', 'o', 'f', 'e', 'r']
```
#python 