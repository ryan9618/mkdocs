

### tages:
    - py
    - 数字函数
    - 字符串函数
    - 内置函数
    - 列表函数
    - 字典函数
    - 元组函数
    - 集合函数



### 68fun   
### 68个Python内置函数   







```


原创 华安9527 测试开发学习交流 2023-07-13 07:00 发表于浙江
图片

Python是一种非常流行的编程语言，其内置的函数库也很强大。本文将介绍Python内置函数库中的68个常用函数，并提供相应的代码示例。这些函数涵盖了Python中常见的数据类型、字符串、列表、字典、元组、集合、文件操作以及其他常用功能。下面分别进行介绍：

https://mp.weixin.qq.com/s/X74Pd6YPMf8H832UOWNlYw

## 数字函数


### abs()
用于返回一个数的绝对值。
a = -5
print(abs(a))  # 5

### divmod()
用于取两个数的商和余数。
a, b = 10, 3
print(divmod(a, b))  # (3, 1)

### pow()
用于计算一个数的幂。
a, b = 2, 3
print(pow(a, b))  # 8

### round()
用于对一个数进行四舍五入。
a = 2.8
print(round(a))  # 3

图片

字符串函数


### chr()
用于将ASCII码转换为对应的字符。
print(chr(97))  # 'a'

### ord()
用于将一个字符转换为它的ASCII码。
print(ord('a'))  # 97

### len()
用于返回一个字符串的长度。
s = 'hello world'
print(len(s))  # 11

### str()
用于将其他类型的数据转换为字符串类型。
a = 123
print(str(a))  # '123'
### capitalize()
用于将字符串的第一个字符转换为大写。
s = 'hello world'
print(s.capitalize())  # 'Hello world'
### lower()
用于将字符串中的所有字符都转换为小写。
s = 'Hello World'
print(s.lower())  # 'hello world'
### upper()
用于将字符串中的所有字符都转换为大写。
s = 'Hello World'
print(s.upper())  # 'HELLO WORLD'
### swapcase()
用于将字符串中的大小写字母互换。
s = 'Hello World'
print(s.swapcase())  # 'hELLO wORLD'
### title()
用于将字符串中每个单词的首字母转换为大写。
s = 'hello world'
print(s.title())  # 'Hello World'
### strip()
用于去除字符串的开头和结尾的空格或者指定字符。
s = '   hello world  '
print(s.strip())  # 'hello world'
### replace()
用于将字符串中的指定字符替换为指定的字符。
s = 'hello world'
print(s.replace('l', 'i'))  # 'heiioworid'
### split()
用于将字符串按照指定的字符分割为多个子串。
s = 'hello,world'
print(s.split(','))  # ['hello', 'world']
### join()
用于将多个字符串连接成一个字符串。
lst = ['hello', 'world']
print('-'.join(lst))  # 'hello-world'


列表函数


### len()
用于返回一个列表的长度。
lst = [1, 2, 3, 4, 5]
print(len(lst))  # 5

### max()
用于返回一个列表中的最大值。
lst = [1, 2, 3, 4, 5]
print(max(lst))  # 5
### min()
用于返回一个列表中的最小值。
lst = [1, 2, 3, 4, 5]
print(min(lst))  # 1

### sum()
用于返回一个列表中所有元素的和。
lst = [1, 2, 3, 4, 5]
print(sum(lst))  # 15

### sorted()
用于对一个列表进行排序。
lst = [3, 1, 4, 2, 5]
print(sorted(lst))  # [1, 2, 3, 4, 5]
### reversed()
用于反转一个列表中的元素。
lst = [1, 2, 3, 4, 5]
print(list(reversed(lst)))  # [5, 4, 3, 2, 1]
### list()
用于将其他类型的数据转换为列表类型。
t = (1, 2, 3)
print(list(t))  # [1, 2, 3]

### append()
用于在一个列表的末尾添加一个元素。
lst = [1, 2, 3]
lst.append(4)
print(lst)  # [1, 2, 3, 4]
### insert()
用于在一个列表的指定位置插入一个元素。
lst = [1, 2, 3]
lst.insert(1, 4)
print(lst)  # [1, 4, 2, 3]
### remove()
用于删除一个列表中的指定元素。
lst = [1, 2, 3]
lst.remove(2)
print(lst)  # [1, 3]
### pop()
用于从一个列表的末尾删除一个元素并返回该元素。
lst = [1, 2, 3]
print(lst.pop())  # 3
print(lst)  # [1, 2]
### extend()
用于将一个列表中的元素添加到另一个列表的末尾。
lst1 = [1, 2, 3]
lst2 = [4, 5, 6]
lst1.extend(lst2)
print(lst1)  # [1, 2, 3, 4, 5, 6]
### index()
用于返回一个元素在列表中首次出现的位置。
lst = [1, 2, 3, 4, 5]
print(lst.index(3))  # 2
### count()
用于返回一个元素在列表中出现的次数。
lst = [1, 2, 2, 3, 3, 3]
print(lst.count(2))  # 2



字典函数


### len()
用于返回一个字典中键值对的个数。
d = {'a': 1, 'b': 2, 'c': 3}
print(len(d))  # 3

### keys()
用于返回一个字典中所有的键。
d = {'a': 1, 'b': 2, 'c': 3}
print(d.keys())  # dict_keys(['a', 'b', 'c'])
### values()
用于返回一个字典中所有的值。
d = {'a': 1, 'b': 2, 'c': 3}
print(d.values())  # dict_values([1, 2, 3])

### items()
用于返回一个字典中所有的键值对。
d = {'a': 1, 'b': 2, 'c': 3}
print(d.items())  # dict_items([('a', 1), ('b', 2), ('c', 3)])
### get()
用于返回一个字典中指定键的值，如果键不存在则返回默认值。
d = {'a': 1, 'b': 2, 'c': 3}
print(d.get('a'))  # 1
print(d.get('d', 0))  # 0

### pop()
用于从一个字典中删除指定键并返回对应的值。
d = {'a': 1, 'b': 2, 'c': 3}
print(d.pop('b'))  # 2
print(d)  # {'a': 1, 'c': 3}

### update()
用于将一个字典中的键值对更新到另一个字典中。
d1 = {'a': 1, 'b': 2}
d2 = {'b': 3, 'c': 4}
d1.update(d2)
print(d1)  # {'a': 1, 'b': 3, 'c': 4}



元组函数


### len()
用于返回一个元组中元素的个数。
t = (1, 2, 3)
print(len(t))  # 3

### max()
用于返回一个元组中的最大值。
t = (1, 2, 3)
print(max(t))  # 3

### min()
用于返回一个元组中的最小值。
t = (1, 2, 3)
print(min(t))  # 1

### tuple()
用于将其他类型的数据转换为元组类型。
lst = [1, 2, 3]
print(tuple(lst))  # (1, 2, 3)



集合函数


### len()
用于返回一个集合中元素的个数。
s = {1, 2, 3}
print(len(s))  # 3

### max()
用于返回一个集合中的最大值。
s = {1, 2, 3}
print(max(s))  # 3

### min()
用于返回一个集合中的最小值。
s = {1, 2, 3}
print(min(s))  # 1

### set()
用于将其他类型的数据转换为集合类型。
lst = [1, 2, 3]
print(set(lst))  # {1, 2, 3}

### add()
用于向集合中添加一个元素。
s = {1, 2, 3}
s.add(4)
print(s)  # {1, 2, 3, 4}

### remove()
用于从集合中删除一个元素。
s = {1, 2, 3}
s.remove(2)
print(s)  # {1, 3}



文件操作函数


### open()
用于打开一个文件并返回文件对象。
f = open('test.txt', 'r')

### close()
用于关闭一个已打开的文件。
f.close()

### read()
用于读取一个文件中的内容。
f = open('test.txt', 'r')
print(f.read())
f.close()

### write()
用于向一个文件中写入内容。
f = open('test.txt', 'w')
f.write('hello world\n')
f.close()



其他函数


### isinstance()
用于检查一个对象是否属于指定的类。
x = 10
print(isinstance(x, int))  # True

### range()
用于生成一个指定范围内的整数序列。
print(list(range(5)))  #
[0, 1, 2, 3, 4]

### zip()
用于将多个序列中对应的元素打包成一个元组。
lst1 = [1, 2, 3]
lst2 = ['a', 'b', 'c']
print(list(zip(lst1, lst2)))  # [(1, 'a'), (2, 'b'), (3, 'c')]

### map()
用于对一个序列中的每个元素执行指定的函数。
lst = [1, 2, 3]
print(list(map(lambda x: x * 2, lst)))  # [2, 4, 6]

### filter()
用于对一个序列中的元素进行筛选。
lst = [1, 2, 3, 4, 5]
print(list(filter(lambda x: x % 2 == 0, lst)))  # [2, 4]

### reduce()
用于对一个序列中的元素依次执行指定的函数。
from functools import reduce
lst = [1, 2, 3]
print(reduce(lambda x, y: x * y, lst))  # 6

### round()
用于对一个数进行四舍五入。
a = 2.8
print(round(a))  # 3

### open()
用于打开一个文件并返回文件对象。
f = open('test.txt', 'r')
print(f.read())
f.close()

```
[01001-Python](01001-python.md)    
