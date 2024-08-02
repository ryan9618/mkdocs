# RNlist   
### tages:
    - py
    - 行事历
    - 模块
    - 包和库
    - Py示例随记  


```
## 行事历
# 模块/包和库


```
# Py示例随记   
```



#nicegui界面库
from nicegui import ui
ui.label('开始学习nicegui')
ui.run()


#简易版行事历
class Supercal():

    number = 0

    def __init__(self, date, item, content, status):

        self.date = date

        self.item = item

        self.content = content

        self.status = status

        Supercal.number += 1

    def show(self):

        

        print("Date:{}.Item:{}.Content:{}.Status:{}".format(self.date,self.item,self.content,self.status))

# 创建多个Supercal对象并存储在列表中
print('行事历息如下：')
print('*'*72)
super_events = [

    Supercal('10月5日', '设计', '交一个设计', '紧急'),

    Supercal('10月8日', '私事', '广州火车站接爸妈', '重要'),

    Supercal('10月12日', '联系', '提前联系林总了解扫描情况', '正常'),

    Supercal('10月15日', '出差', '计划到云浮扫描', '正常')

]

# 遍历列表并调用每个对象的show()方法

for event in super_events:

    event.show()

    print()  # 添加空行分隔不同的事件信息



#另一种写法

class List:
    def __init__(self, date, item, content, status):
        self.date = date
        self.item = item
        self.content = content
        self.status = status

    def Supercal(self):
        print("{}\t{}\t{}\t{}".format(self.date, self.item, self.content, self.status))

print("日期\t事项\t内容\t等级")

person = [List(20231018, '设计', '后天交设计', 'AAA'), List(20231011, '出差', '计划去云浮扫描', 'BBB')]
for p in person:
    p.Supercal()



#数据库版行事历
import random
import shelve
import datetime
import time
import itertools

# 定义一个生成唯一序列号的函数
def generate_sequence_number():
    return random.randint(1, 1000)

# 定义录入功能函数
def insert_data():
    with shelve.open('my_supercal') as db:
        dateup=[]
        
        DATE_FORMAT = "%Y-%m-%d"
        supercal_name = input("请输入行事历名称：")
        if supercal_name == 'q':
            return
        supercal_date = input("请输入日期（默认为当前日期）：") or time.strftime(
        "%Y-%m-%d", time.localtime())

        # 生成唯一的序列号
        sequence_number = str(generate_sequence_number())

        # 将数据存储在字典中
        supercal_content = input("请输入行事内容")
        supercal_grade = input("等级默认 AAA  ")
        if supercal_grade=="":
            supercal_grade=='AAA'

        date= {'sequence_number': sequence_number, 'date': supercal_date, 'supercal_name': supercal_name,'supercal_content': supercal_content, 'supercal_grade': supercal_grade}
        
        dateup.append(date)
        #print(dateup)
        if 'cal' in db:  
            db['cal']+=dateup
        else:
            db['cal']=dateup


# 定义查询功能函数
def query_data(sequence_number):
    with shelve.open('my_supercal') as db:
        mydate = db['cal']
        print("序号\t\t", "日期\t\t", "事项\t\t", "内容\t\t\t\t", "等级\t\t")
        for i, item in enumerate(mydate):
            if item['sequence_number']==str(sequence_number):
                values=item.values()
                for value in values:
                    print(value,end='            ')

            #else:
            #    print("未找到相关记录")


# 定义删除功能函数
def delete_data(sequence_number):
    with shelve.open('my_supercal') as db:
        mydate = db['cal']
        for i, item in enumerate(mydate):
            if item['sequence_number']==str(sequence_number):
                mydate.pop(i)
                db['cal']=mydate
        #print(mydate)
        print(f"已成功删除序列号为{sequence_number}的行事历记录。")


#清空所有数据
def delete_all_date():
    with shelve.open('my_supercal') as db:
        #获取要清空的表名
        table_name = 'cal'
        #删除表中的所有数据
        if table_name in db:
            del db[table_name]
            print("File Clear out successfully")



    

# 定义显示所有数据的函数
def show_all_data():
    with shelve.open('my_supercal') as db:
        list1= db.get('cal', [])
        #print(list1)
        print()
        print("-----行事历信息界面-----")
        print()
        print("序号\t\t", "日期\t\t", "事项\t\t", "内容\t\t\t\t", "等级\t\t")
        for item in list1:
            print("%s\t\t%s\t\t%s\t\t\t\t%s\t\t\t%s\t\t" % (
                item["sequence_number"], item["date"], item["supercal_name"], item["supercal_content"], item["supercal_grade"])) 
    

# 定义菜单函数
def menu():
    print("欢迎使用行事历系统，希望你有缘为精神家园找到一片栖息地！")
    while True:
        print("-------------------------------")
        print("         行事历系统 V3.0")
        print("                          ")
        print("        1. 写入行事历        ")
        print("        2. 查询行事历        ")
        print("        3. 删除行事历        ")
        print("        4. 展示所Cal       ")
        print("        5. 清空行事历       ")
        print("        6. 退出  系统      ")
        choice = int(input("请输入你的选择："))
        if choice == 1:
            insert_data()
        elif choice == 2:
           query_data(int(input("请输入要查询的行事历序列号：")))
        elif choice == 3:
           delete_data(int(input("请输入要删除的行事历序列号：")))
        elif choice == 4:
           show_all_data()
        elif choice == 5:
            delete_all_date()
        elif choice == 6:
            print("感谢使用！")
            exit()

# 主程序
while True:
    menu()
    





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
result = cv2.resize(src, (x*Multiple,y*Multiple))
 
for RGB_DATA_Y in range(y):  # 循环所有文件 Y有多少像素 就有多少个RGB颜色文件
    '''循环读取刚刚存储的RGB颜色文件 并循环进行绘制 以倍数进行绘图 确保无损放大'''
    NAME_ = eval(open(f'DATA/{RGB_DATA_Y}', 'r', encoding='utf-8').read())  # 读取文件并转为列表
    for RGB_DATA_X in range(len(NAME_)):  # 获取 文件内有多少个子列表
        '''
        因为通过getpixel 获取出来的颜色是反过来的 RGB 也就是 BGR  
        在颜色文件内的数值也是反过来的，所以在这里读取的时候要将其颠倒一下，反向转换一下
        '''
        _DATA = NAME_[RGB_DATA_X]
        _DATA.reverse()
 
        '''
        当前这个模块是核心模块 主要是用来读取并绘制出原图的倍数 
        原理：
        result[1,1] = [255,255,255]    填充 图片的第一个像素为白色   [255,255,255] 是RGB的白色颜色数值
        result[0:2,0:4] = [255,255,255]      填充图片 X轴从0像素到2像素为白色  Y轴从0像素到4像素为白色  
        '''
        try:
            result[RGB_DATA_Y*Multiple:RGB_DATA_Y*Multiple+Multiple,RGB_DATA_X*Multiple:RGB_DATA_X*Multiple+Multiple] = _DATA
        except:pass
# 写入保存图像
cv2.imwrite(DATA_file, result)
print('完成....')
try:
    shutil.rmtree("DATA") # 删除文件夹和文件
except:pass
————————————————
版权声明：本文为CSDN博主「小木_.」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/weixin_46625757/article/details/126622097




# 无损放大PNG源代码：

#!/usr/bin/python
# -*- coding:utf-8 -*-
import cv2
from PIL import Image
import time
import shutil
import os
 
 
 
DATA = input('请输入要放大的图片名称(PNG文件名称必须使用数字或英文)：')
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
 
# 模板
# 图像缩放  要将原图进行翻倍放大  然后在原图的基础上进行绘图
result = cv2.resize(src, (x*Multiple,y*Multiple))
# 写入保存图像 - 模板图片不用管
cv2.imwrite('8UY88767.png', result)
 

 
# 临时装饰器
List_elements = []
# 存储文件的个数 后期读取方便，不会错读取
Number_documents = 0
 
for YY in range(y):   # 获取图片的Y轴有多少像素  也相当于长度
    '''意思：循环读取图片的每一个像素点的RGBA值 并以列表的形式存储起来'''
    if int(len(List_elements)) >= 2:   # 每次循环完毕后要将列表的值恢复无
        List_elements = []
    for XX in range(x):  # 获取图片的X轴有多少像素   也相当于宽度
        # IMG.getpixel((a, aa))  用来获取图片某位置的RGBA像素值
        List_elements = List_elements + [IMG.getpixel((XX, YY))]*Multiple   # 读取某坐标的像素值并将元组为列表进行存储   Multiple是倍数
    for a in range(Multiple):    # Multiple是倍数  如果是2倍 则生成两个同样的颜色文件   在后期进行单行输出多次 确保以像素点进行放大
        NAME = open(f"DATA/{Number_documents}", 'w')  # 存储
        NAME.write(str(List_elements))  # 将列表转为字符串保存
        NAME.close()
        Number_documents = Number_documents + 1
 
time.sleep(1)   # 延迟一下 ，防止文件加载过慢读取错误
 
DATA_ = list()  # 定义需要处理的数据列表
for a in range(Number_documents):
    NAME = open(f"DATA/{a}", 'r').read()  # 读取颜色文件
    NAME = list(eval(NAME))   # 将颜色文件转换为列表
    for aa in range(len(NAME)):  # 循环读取列表的颜色值
        DATA_.append(NAME[aa])    # 将颜色值保存到数据列表
 
# 打开写入模板图片
IMG_2 = Image.open('8UY88767.png')
# 转化为RGBA
RGBA_IMG = IMG_2.convert("RGBA")
RGBA_IMG.putdata(DATA_)  # 写入图片
RGBA_IMG.save(DATA_file, "PNG")  # 保存图片
print('完成....')
try:
    shutil.rmtree("DATA") # 删除文件夹和文件
except:pass
try:
    os.remove("8UY88767.png") # 删除文件
except:pass
————————————————
版权声明：本文为CSDN博主「小木_.」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/weixin_46625757/article/details/126622097
```
