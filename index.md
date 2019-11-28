<head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/katex.min.css" integrity="sha384-yFRtMMDnQtDRO8rLpMIKrtPCD5jdktao2TV19YiZYWMDkUR5GQZR/NOVTdquEx1j" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/katex.min.js" integrity="sha384-9Nhn55MVVN0/4OFx7EE5kpFBPsEMZxKTCnA+4fqDmg12eCTqGi6+BB2LjY8brQxJ" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
$$\a^2 + b^2 = c^2$$
  </head>

***Заметка 1***

**generator:**
```python
M = [[1,2,3],[4,5,6],[7,8,9]]

G=(sum(row) for row in M)
```
#python 

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

***Заметка 4***
Принудительная очистка памяти в для больших объектов python.
```python
M = [[1,2,3],[4,5,6],[7,8,9]]
#работаем с M и когда оно больше не нужно, то принудительно освобождаем память
M = 0
```
#python 

***Заметка 5***
Множества в python содержат элементы множества. Все операции и свойства соответствуют математическим [множествам](https://ru.wikipedia.org/wiki/Множество). 
```python
>>> X = set([1,2,3,4])
>>> Y = {3,4,5,6,7}
#Пересечение
>>> X&Y
{3, 4}
#Объединение
>>> X|Y
{1, 2, 3, 4, 5, 6, 7}
#Разность
>>> X-Y
{1, 2}

```
#python 

***Заметка 6***
Объединение операций сравнения "по-человечески"!
```python
#Можно писать
if (x<y<z):
    
#Вместо
if (x<y) and (y<z):

```
#python 


***Заметка 7***
Переменная в python - имя определяющее ссылку на объект.
```python
name = 42 
```
Создается объект 42 (<class 'int'>) и name связывается с этим объектом по ссылке.
#python 

***Заметка 8***
Разделяемые ссылки на неизменяемые типы:
```python
>>>a=42
>>>b=a
>>>a=a-10
```
Создается объект "42" и ссылка на него сохраняется в имя a, затем в имя b помещается ссылка на "42". Вконце создается новый объект и ссылка на него пересохраняется в a. 
#python

***Заметка 9***
Разделяемые ссылки на изменяемые типы:
```python
>>>L1=[1,2,3]
>>>L2=L1
>>>L1[1]=24
>>> print (L2)
[1, 24, 3]
```
Здесь новый объект не создается, а модифицируется объект на который ссылаются имена L1 и L2. Но объект 2 удалился, а создался объект 24.
#python

***Заметка 10***
Несколько методов правильного копирования с созданием нового объекта, для избежания проблем связанных с разделяемыми ссылками
```python
#Для списков 
L2=L1[:]
#не только для списков
L3=L1.copy()
#универсальный вариант
import copy
L4=copy.copy(L1)    
```
#python