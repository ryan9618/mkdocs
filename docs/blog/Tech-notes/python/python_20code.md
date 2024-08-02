# python_20code   

### tages:
    - py
    - 20个非常有用的Python单行代码
    - 库 
    - 包
 
```

编辑丨数据STUDIO
来源丨https://python.plainenglish.io/20-extremely-useful-python-one-liners-you-must-know

大家好，我是菜鸟哥！
在本文中，给大家分享20 个 Python 一行代码，你可以在 30 秒或更短的时间内轻松学习它们。这种单行代码将节省你的时间，并使你的代码看起来更干净且易于阅读。

1 一行 For 循环
for 循环是一个多行语句，但是在 Python 中，我们可以使用列表推导式方法在一行中编写 for 循环。以过滤小于250的值为例，查看下面的代码示例。

## For循环在一行
mylist = [200, 300, 400, 500]
#正常方式
result = [] 
for x in mylist: 
    if x > 250: 
        result.append(x) 
print(result) # [300, 400, 500]
##  一行代码方式
result = [x for x in mylist if x > 250] 
print(result) # [300, 400, 500]
2 一行 While 循环
这个 One-Liner 片段将向你展示如何在一行中使用 While 循环代码，我已经展示了两种方法。

## 方法 1 Single Statement 
while True: print(1) #infinite 1
#方法 2 多语句
x = 0 
while x < 5: print(x); x= x + 1 # 0 1 2 3 4 5
3 一行 IF Else 语句
好吧，要在一行中编写 IF Else 语句，我们将使用三元运算符。三元的语法是“[on true] if [expression] else [on false]”。

我在下面的示例代码中展示了 3 个示例，以使你清楚地了解如何将三元运算符用于一行 if-else 语句。要使用 Elif 语句，我们必须使用多个三元运算符。

#if Else 在一行中
#Example 1 if else
print("Yes") if 8 > 9 else print("No") # No
#Example 2 if elif else 
E = 2 
print("High") if E == 5 else print("数据STUDIO") if E == 2 else 
print("Low") # 数据STUDIO 
 
#Example 3 only if
if 3 > 2: print("Exactly") # Exactly
4 一行合并字典
这个 单行代码段将向你展示如何使用一行代码将两个字典合并为一个。下面我展示了两种合并字典的方法。

##  在一行中合并字典
d1 = { 'A': 1, 'B': 2 } 
d2 = { 'C': 3, 'D': 4 }
#方法 1 
d1.update(d2) 
print(d1) # {'A': 1, 'B': 2, 'C': 3, 'D': 4}
#方法 2 
d3 = {**d1, **d2} 
print(d3) # {'A': 1, 'B': 2, 'C': 3, 'D': 4}
5 一行函数
我们有两种方法可以在一行中编写函数，在第一种方法中，我们将使用与三元运算符或单行循环方法相同的函数定义。

第二种方法是用 lambda 定义函数。查看下面的示例代码以获得更清晰的理解。

#函数在一行中
#方法一
def fun(x): return True if x % 2 == 0 else False 
print(fun(2)) # False
#方法2
fun = lambda x : x % 2 == 0 
print(fun(2)) # True 
print(fun(3)) # False
6 一行递归
这个单行代码片段将展示如何在一行中使用递归。我们将使用一行函数定义和一行 if-else 语句。下面是查找斐波那契数的示例。

##  单行递归
#Fibonaci 单行递归示例
def Fib(x): return 1 if x in {0, 1} else Fib(x-1) + Fib(x-2)
print(Fib(5)) # 8
print(Fib(15)) # 987
7 一行数组过滤
Python 列表可以通过使用列表推导方法在一行代码中进行过滤。以过滤偶数列表为例。

##  一行中的数组过滤
mylist = [2, 3, 5, 8, 9, 12, 13, 15]
#正常方式
result = [] 
for x in mylist: 
    if x % 2 == 0: 
        result.append(x)
print(result) # [2, 8, 12]
##  单线方式
result = [x for x in mylist if x % 2 == 0] 
print(result) # [2, 8, 12]
8 一行异常处理
我们使用异常处理来处理 Python 中的运行时错误。你知道我们可以在一行中编写这个 Try except 语句吗？通过使用 exec() 语句，我们可以做到这一点。

##  一行异常处理
#原始方式
try:
    print(x)
except:
    print("Error")
#单行方式
exec('try:print(x) \nexcept:print("Error")') # 错误
9 一行列表转字典
我们可以使用 Python enumerate() 函数将 List 转换为一行字典。在enumerate() 中传递列表并使用dict() 将最终输出转换为字典格式。

##  字典在一行
mydict = ["John", "Peter", "Mathew", "Tom"]
mydict = dict(enumerate(mydict))
print(mydict) # {0: 'John', 1: 'Peter', 2: 'Mathew', 3: 'Tom'}
10 一行多变量
Python 允许在一行中进行多个变量赋值。下面的示例代码将向你展示如何做到这一点。

## 多行变量
### 正常方式
x = 5 
y = 7 
z = 10 
print(x , y, z) # 5 7 10
#单行方式
a, b, c = 5, 7, 10 
print(a, b, c) # 5 7 10
11 一行交换值
交换是编程中一项有趣的任务，并且总是需要第三个变量名称 temp 来保存交换值。这个单行代码段将向你展示如何在没有任何临时变量的情况下交换一行中的值。

#换成一行
#正常方式
v1 = 100
v2 = 200
temp = v1
v1 = v2 
v2 = temp
print(v1, v2) # 200 100
###  单行交换
v1, v2 = v2, v1 
print(v1, v2) # 200 100
12 一行排序
排序是编程中的一个普遍问题，Python 有许多内置的方法来解决这个排序问题。下面的代码示例将展示如何在一行中进行排序。

# 在一行中排序
mylist = [32, 22, 11, 4, 6, 8, 12] 
# 方法 1
mylist.sort() 
print(mylist) # # [4, 6, 8, 11, 12, 22, 32]
print(sorted(mylist)) # [4, 6, 8, 11, 12, 22, 32]
13 一行读取文件
不使用语句或正常读取方法，也可以正确读取一行文件。

#一行读取文件
#正常方式
with open("data.txt", "r") as file: 
    data = file.readline() 
    print(data) # Hello world
#单行方式
data = [line.strip() for line in open("data.txt","r")] 
print(data) # ['hello world', 'Hello Python']
14 一行类
上课总是多线工作。但是在 Python 中，有一些方法可以在一行代码中使用类特性。

# 一行中的类
#普通方式
class Emp: 
    def __init__(self, name, age): 
        self.name = name 
        self.age = age
        emp1 = Emp("云朵君", 22) 
print(emp1.name, emp1.age) # 云朵君 22
## 单行方式
#方法 1 带有动态 Artibutes 的 Lambda

Emp = lambda:None; Emp.name = "云朵君"; Emp.age = 22
print(Emp.name, Emp.age) # 云朵君 22

## 方法 2 
from collections import namedtuple
Emp = namedtuple('Emp', ["name", "age"]) ("云朵君", 22) 
print(Emp.name, Emp.age) # 云朵君 22
15 一行分号
一行代码片段中的分号将向你展示如何使用分号在一行中编写多行代码。

# 一行分号
# 例 1 
a = "Python"; b = "编程"; c = "语言"; print(a, b, c)
# 输出
# Python 编程语言
16 一行打印
这不是很重要的片段，但有时当你不需要使用循环来执行任务时它很有用。

# 一行打印
## 正常方式
for x in range(1, 5):
    print(x) # 1 2 3 4
## 单行方式
print(*range(1, 5)) # 1 2 3 4
print(*range(1, 6)) # 1 2 3 4 5
17 一行map函数
Map 函数是适用的高阶函数。这将函数应用于每个元素。下面是我们如何在一行代码中使用 map 函数的示例。

# 在一行中map
print(list(map(lambda a: a + 2, [5, 6, 7, 8, 9, 10])))
# 输出
# [7, 8, 9, 10, 11, 12]
18 删除列表第一行中的 Mul 元素
你现在可以使用 del 方法在一行代码中删除 List 中的多个元素，而无需进行任何修改。

# 删除一行中的Mul元素
mylist = [100, 200, 300, 400, 500]
del mylist[1::2]
print(mylist) # [100, 300, 500]
19 一行打印图案
现在你不再需要使用for循环来打印相同的图案。你可以使用 print 语句和星号 (*) 在一行代码中执行相同的操作。

# 在一行中打印图案# 
# 正常方式
for x in range(3):
    print('😀')
# 输出
# 😀 😀 😀
#单行方式
print('😀' * 3) # 😀 😀 😀 
print('😀' * 2) # 😀 😀 
print('😀' * 1) # 😀
20 一行查找质数
此代码段将向你展示如何编写单行代码来查找范围内的素数。

# 查找质数
print(list(filter(lambda a: all(a % b != 0 for b in range(2, a)),
                  range(2,20))))
# 输出
# [2, 3, 5, 7, 11, 13, 17, 19]


万水千山总是情，点个 👍 行不行。



推荐阅读:

入门: 最全的零基础学Python的问题  | 零基础学了8个月的Python  | 实战项目 |学Python就是这条捷径



干货:爬取豆瓣短评，电影《后来的我们》 | 38年NBA最佳球员分析 |   从万众期待到口碑扑街！唐探3令人失望  | 笑看新倚天屠龙记 | 灯谜答题王 ｜用Python做个海量小姐姐素描图 ｜碟中谍这么火，我用机器学习做个迷你推荐系统电影



趣味:弹球游戏  | 九宫格  | 漂亮的花 | 两百行Python《天天酷跑》游戏!



AI: 会做诗的机器人 | 给图片上色 | 预测收入 | 碟中谍这么火，我用机器学习做个迷你推荐系统电影



小工具: Pdf转Word，轻松搞定表格和水印！ | 一键把html网页保存为pdf！|  再见PDF提取收费！ | 用90行代码打造最强PDF转换器，word、PPT、excel、markdown、html一键转换 | 制作一款钉钉低价机票提示器！ ｜60行代码做了一个语音壁纸切换器天天看小姐姐！｜



年度爆款文案

1).卧槽！Pdf转Word用Python轻松搞定！
2).学Python真香！我用100行代码做了个网站，帮人PS旅行图片，赚个鸡腿吃
3).首播过亿，火爆全网，我分析了《乘风破浪的姐姐》，发现了这些秘密 
4).80行代码！用Python做一个哆来A梦分身 
5).你必须掌握的20个python代码，短小精悍，用处无穷 
6).30个Python奇淫技巧集 
7).我总结的80页《菜鸟学Python精选干货.pdf》,都是干货 
8).再见Python！我要学Go了！2500字深度分析！
9).发现一个舔狗福利！这个Python爬虫神器太爽了，自动



```
## python模块、包和库   
```

# 一文带你分清python模块、包和库
Python宝典 2023-02-24 09:00 发表于安徽
一、模块

Python 模块(Module)，是一个 Python 文件，以 .py 结尾，包含了 Python 对象定义和Python语句。

模块能定义函数，类和变量，模块也能包含可执行的代码。

1.1 导入模块
1.1.1 导入模块的方式

import 模块名
from 模块名 import 功能名
from 模块名 import *
import 模块名 as 别名
from 模块名 import 功能名 as 别名
1.2 导入方式详解
import 语法：

## 1. 导⼊模块
import 模块名
import 模块名1, 模块名2...

## 2. 调⽤功能
模块名.功能名()
体验：

import math
print(math.sqrt(9)) # 3.0
from..import..

语法：

from 模块名 import 功能1, 功能2, 功能3...
体验：

from math import sqrt 
print(sqrt(9))
from .. import *
语法

from 模块名 import *
体验：

from math import *
print(sqrt(9))
as定义别名

语法

##  模块定义别名
import 模块名 as 别名

##  功能定义别名
from 模块名 import 功能 as 别名
体验

##  模块别名
import time as tt

tt.sleep(2)
print('hello')

##  功能别名
from time import sleep as sl
sl(2)
print('hello')
1.2 制作模块
在Python中，每个Python文件都可以作为一个模块，模块的名字就是文件的名字。也就是说定义模块名必须要符合标识符命名规则。

1.2.1 定义模块

新建一个Python文件，命名为 my_module1.py ，并定义 testA 函数。

def testA(a, b):
 print(a + b)
1.2.2 测试模块

在实际开发中，当一个开发员编写完一个模块后，为了让模块能够在项目中达到想要的效果，这个开发员会在py文件中添加一些测试信息.，例如，在 my_module1.py 文件中添加测试代码。

def testA(a, b):
 print(a + b)

testA(1, 1) 12345
此时，无论是当前文件，还是其他已经导入了该模块的⽂件，在运行的时候都会自动执行 testA 函数的调用。

解决办法如下：

def testA(a, b): 
 print(a + b) 
##  只在当前⽂件中调⽤该函数，其他导⼊的⽂件内不符合该条件，则不执⾏testA函数调⽤ 
if __name__ == '__main__': 
 testA(1, 1)
1.2.3 调用模块

import my_module1
my_module1.testA(1, 1)
1.2.4 注意事项

如果使用 from .. import .. 或 from .. import * 导入多个模块的时候，且模块内有同名功能。当调 ⽤这个同名功能的时候，调用到的是后导入的模块的功能。

体验：

##  模块1代码
def my_test(a, b):
 print(a + b)
##  模块2代码
def my_test(a, b):
 print(a - b)
 
##  导⼊模块和调⽤功能代码
from my_module1 import my_test
from my_module2 import my_test

##  my_test函数是模块2中的函数
my_test(1, 1)
1.3 模块的定位顺序
当导入一个模块，Python解析器对模块位置的搜索顺序是：

1. 当前目录

2. 如果不在当前目录，Python则搜索在shell变量PYTHONPATH下的每个目录。

3. 如果都找不到，Python会查看默认路径。UNIX下，默认路径⼀般为/usr/local/lib/python/

模块搜索路径存储在system模块的sys.path变量中。变量包含当前目录，PYTHONPATH和由安装过 程决定的默认目录。

注意：⾃⼰的⽂件名不要和已有模块名重复，否则导致模块功能用法使用，使用from 模块名 import 功能 的时候，如果功能名字重复，调用到的是最后定义或导入的功 能。
1.4 __all__

如果一个模块文件中有 __all__ 变量，当使用 from xxx import * 导入时，只能导入这个列表中的元素。

my_module1模块代码：

__all__ = ['testA']

def testA():
 print('testA')


def testB():
 print('testB')
导入模块的文件代码：

from my_module1 import * 
testA() 
testB()
图片


二、库
严格来说，Python中没有库(library)的概念，模块(module)和包(package)才是Python语法中有的概念。这个库的概念是从其他编程语言引进来的，库的概念是具有相关功能模块的集合，只是一个通俗的说法。平时说的库既可以是一个模块，也可以是一个包。

包和模块之间的关系，如下图：

图片

一个包里面可以包含很多的模块。模块是一个包含有组织的代码片段，一个.py文件对应一个模块，文件名就是模块名（去除掉后缀.py）。



三、包
包将有联系的模块组织在一起，即放到同一个文件夹下，并且在这个文件夹创建一个名字 为 __init__.py 文件，那么这个文件夹就称之为包。

3.1 制作包
[New] — [Python Package] — 输入包名 — [OK] — 新建功能模块(有联系的模块)。

注意：新建包后，包内部会自动创建 __init__.py 文件，这个文件控制着包的导入。

3.1.1 快速体验

1. 新建包 mypackage

2. 新建包内模块：my_module1 和 my_module2

3. 模块内代码如下

##  my_module1
print(1)


def info_print1():
 print('my_module1')


##  my_module2
print(2)


def info_print2():
 print('my_module2')
3.2 导入包
3.2.1 方法一：

import 包名.模块名

包名.模块名.⽬标
3.2.2 快速体验

import my_package.my_module1

my_package.my_module1.info_print1()
3.2.3 方法二

注意：必须在 __init__.py ⽂件中添加 __all__ = [] ，控制允许导⼊的模块列表。

from 包名 import *
模块名.⽬标
3.2.4 快速体验

from my_package import * 
my_module1.info_print1()



 #  pip install Pillow  放大图片先安装这个库

#  无损放大JPG源代码：

#!/usr/bin/python
# -*- coding:utf-8 -*-
import cv2
from PIL import Image
import time
import shutil
import os
 
 
 
DATA = input('请输入要放大的图片名称(JPG文件名称必须使用数字或英文)：')
Multiple = int(input('请输入要放大的图片的倍数(必须大于1)：'))
DATA_file = input('请输入要图片要保存的图片名称：')
print('开始放大....')
os.mkdir('DATA') # 新建
#读取图片  要放大的图片
src = cv2.imread(DATA)
# 用来读取原图片的像素RGB颜色值  先读取图片文件
IMG = Image.open(DATA)
#获取图像大小  获取图像的大写XY也是颠倒过来的
y, x = src.shape[:2]
 
# 临时装饰器
List_elements = []
for YY in range(y):   # 获取图片的Y轴有多少像素  也相当于长度
    '''意思：循环读取图片的每一个像素点的RGB值 并以列表的形式存储起来'''
    if int(len(List_elements)) >= 2:   # 每次循环完毕后要将列表的值恢复无
        List_elements = []
    for XX in range(x):  # 获取图片的X轴有多少像素   也相当于宽度
        # IMG.getpixel((a, aa))  用来获取图片某位置的RGB像素值  提示：获取的值 对应 BGR  是RGB反过来的
        List_elements = List_elements + [list(IMG.getpixel((XX, YY)))]  # 读取某坐标的像素值并将元组为列表进行存储
    NAME = open(f"DATA/{YY}", 'w')  # 存储
    NAME.write(str(List_elements))  # 将列表转为字符串保存
    NAME.close()
 
time.sleep(2)  # 延迟一下 ，防止文件加载过慢读取错误
 
# 图像缩放  要将原图进行翻倍放大  然后在原图的基础上进行绘图
result = cv2.resize(src, (x*Mult

```
