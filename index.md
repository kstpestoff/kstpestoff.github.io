***Заметка 1***

**generator:**
```python
M = [[1,2,3],[4,5,6],[7,8,9]]

G=(sum(row) for row in M)
```

***Заметка 2***
```python
map(sum, M)
```

Отображение множества M функционалом sum в новое множество. [Функциональное_программирование](https://ru.m.wikipedia.org/wiki/Функциональное_программирование) - основа python

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
>>> L=list(s)
>>> L
['f', 'r', 'a', 'u', 'n', 'g', 'h', 'o', 'f', 'e', 'r']
>>> L[1] = 'L'
>>> L
['f', 'L', 'a', 'u', 'n', 'g', 'h', 'o', 'f', 'e', 'r']
```