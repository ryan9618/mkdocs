#  用法查询笔记 
#  py_qnotes   
  
# Python基础知识 
### tags:
      - py
      - py_qnotes
      - 用法查询笔记
      - Python基础知识  
      - 

######  返回首页 [Home][Home]
     [Home]: /index.md



```


## 用法查询笔记: Python基础知识

## 如何解题:

**1.分析问题，明确结果**

**2.思考需要的知识，或搜索新知识**

**3.思考切入点**

**4.尝试解决问题的一部分**

**5.重复1-4步**

完成一个项目的流程

1.明确项目目标

2.分析过程，拆解项目

3.逐步执行，代码实现


```
## 1.1、理解:print()函数   
```
### **1、理解:print()函数**

\`\`\`python
#功能:打印
#print()函数:
print('')       #单引号和双引号：直接输出
print(''' ''')  #三引号：可以进行格式换行
print()         #让计算机读懂括号里的内容，打印最终的结果
#变量命名要规范:
 1.只能是一个词;
 2.只能包含字母、数字和下划线;
 3.不能以数字开头;
 4.尽量描述包含的数据内容;
 5.不要使用Python函数名或关键字。
#变量与赋值
  赋值用[=] 表示
  变量的最终值等于最后赋值的值
#转义字符: \+需 要转义的功能的英文缩写字母

#补充小知识:
end=''        #可以打印出不换行   
print('')     #双引号内为空,用它来换行

```
## 1.2、知识: print()函数   
```
print(520)
#》》520
print(1+1)
#》》2
print('千寻')
#》》千寻
print("一起玩吧")   # 单引号和双引号输出结果一样
#》》一起玩吧
print('''我愿意留在汤婆婆的澡堂里工作两年，
第一年在锅炉房和锅炉爷爷一起烧锅炉水，
将在这个世界变成一头猪。
''')
#》》我愿意留在汤婆婆的澡堂里工作两年，
#》》第一年在锅炉房和锅炉爷爷一起烧锅炉水，
#》》将在这个世界变成一头猪。
print('''
=============================
   干物妹！うまるちゃんの年齢
=============================
''')                 #
#》》=============================
#》》   干物妹！うまるちゃんの年齢
#》》=============================

print('我愿意留在汤婆婆的澡堂里工作两年，\n如果我违背工作内容的话，\n将在这个世界变成一头猪。')
                                      #\n之外，转义字符还有很多，它们的特征就是：反斜杠+想要实现的转义功能首字母。
#》》我愿意留在汤婆婆的澡堂里工作两年，
#》》如果我违背工作内容的话，
#》》将在这个世界变成一头猪。
name='小千'
print(name)
#》》小千
name='魔法少女千酱'
name='夏目千千'
name='千寻'
print(name)  #虽然name被赋值了两次，但最后一次赋值的值是【千寻】，因此能打印出【千寻】
#》》小千

who = '我的'
action = '是'
destination = '镜像世界'
number = '153'
code = '通行密码'
print(who+destination+code+action+number) #字符串拼接:用字符串拼接符号【+】，将需要拼接的变量连在一起.
#》》我的镜像世界通行密码是153

hero = '我'
organization = '风变编程'
identity = '学员'
action = '是'
ID = '007'
print(hero+action+organization+identity+ID)  #字符串拼接能让我们的数据整合更为灵活，组合出任意我们想要的内容
print(organization+identity+ID+action+hero)
#》》我是风变编程学员007
#》》风变编程学员007是我

who = '我的'
action = '是'
destination = '镜像世界'
number = 153
code = '通行密码'
print(type(who))       #type()函是帮助我们查询不确定数据的类型
print(type(action))
print(type(destination))
print(type(number))
print(type(code))
#》》<class 'str'>
#》》<class 'str'>
#》》<class 'str'>
#》》<class 'int'>
#》》<class 'str'>

```
## 2、理解: 数据转换   
```
#基本类型
字符串-str  #字符串英文string，简写str。只要是被【单/双/三引号】这层皮括起来的内容，不论那个内容是中文、英文、数字甚至火星文。只要是被括起来的，就表示是字符串类型。
整数-int  #整数英文为integer，简写做int。和我们数学课本中定义的一样：是正整数、负整数和零的统称，是没有小数点的数字。
浮点数-float  #浮点数的英文名是float，与整数(int)和字符串(str)不同，浮点数没有简写。带小数点的数字.
#数据拼接
使用符号 '+'   #利用数据拼接符号【+】，将需要拼接的变量连在一起就行了。目的:数据整合
#相关函数
str()    #作用:将其他类型转成字符串
int()    #作用:将其他类型转成整数
float()  #作用:将其他类型转成浮点数
#例如:
1、字符串(str): 用引号括起来的文本
   案例: '千寻'、'2'’、 'love'
2、整数(int):普通的整数数字
   案例: 2、40、-11
3、浮点数(float): 带小数点的数
   案例: 12.0、 5.5、-0.13

```
### 2.1知识: 数据转换   
```
magic = '水仙花数'
action = '是'
unit = '个'
expression = '＝1x1x1+5x5x5+3x3x3'
number = 153
print(str(number)+expression+action+unit+magic)  #str()函数把数字转换成字符串
#》》153＝1x1x1+5x5x5+3x3x3是个水仙花数

number1 = '6'
number2 = '1'
print(int(number1)+int(number2))  #int()函数把字符串转换成整数
#》》7
print(int(3.8)) #int()函数的本质是将数据转换为整数。int()函数会做取整处理
#》》 3

height = 188.0
weight = 180.0
age = 89
print(height)
print(weight)
print(float(age))  #float()函数也可以将整数和字符串转换为浮点类型
#》》188.0
#》》180.0
#》》89.0

```
## 3、知识: 转义字符   
```
#转义字符是一种特殊的字符常量，在编程语言中，我们用转义字符表示不能直接显示的字符，比如换行键、后退键，回车键等。
#比如在单引号输出时，我们不能直接使用格式换行，那么就可以使用转义字符  \n  进行换行
转义字符       意义     
\a       响铃(BEL)
\b       退格(BS),将当前位置移到前一列
\f       换页(FF),将当前位置移到下页开头
\n       换行(L .F),将当前位置移到下一行开头
\r       回车(CR)，将当前位置移到本行开头
\t       水平制表(HT) (跳到下一个TAB位置)
\v        垂直制表(VT)
\\       代表一个反斜线字符
\'       代表一个单引号(撇号)字符
\''      代表一个双引号字符
\0       空字符(NUL)
\ddd     1到3位八进制所代表的任意字符
\xhh     1到2位十六进制所代表的任意字符
注意:区分，斜杠"/"与反斜杠"\"，此处不可互换

Python转义字符
在需要在字符中使用特殊字符时，python用反斜杠()转义字符。如下表:
转义宇符                描 述
\(在行尾时)            续行符
\\                   反斜杠符号
\'                    单引号
\''                   双引号
\a                    响铃
\b 5                   退格(Backspace),将当前位置移到前一列
\e                    转义
\000                  空
\n                   换行
\V                   纵向制表符
\t                   横向制表符
\r                    回车
\f                   换页
\oyy                八进制数，yy代表的字符，例如: \012代表换行
\xyy                十六进制数，yy代表的字符，例如: \x0a代表换行
\other              其它的字符以普通格式输出

```
## 4、知识: 算数运算符   
```
print( 2+1) #加法
#》》3
print( 1-2) #減法
#》》-1
print(1*2) #乘法
#》》2
print( 1/ 2) #除法
#》》0.5
print( 2**3) #冪(呟里是2的3次方)
#》》8
print ( 10%3) #取模(做除法返回余数)
#》》1
print(10/ /3) #取整除(做除法返回商的整数部分)
#》》3

```
## 5、知识: 格式化字符串   
```
知识:格式化字符串
a=10
b=3. 1415926
c='哈哈'
print( '我今年%d岁了' %a) # %d代表填充整数到指定位置
#》》我今年10岁了
print( '我知道圆周率是%f' %b) # %f代表填充浮点数到指定位置
#》》我知道圆周率是3.141593
print( '我%s大笑' %c) # %s代表填充字符串到指定位置
#》》我哈哈大笑
print( '我今年%d岁了，我知道圆周率是%f，%s!' %(a,b,c)) #同时填充多个占位
#》》我今年10岁了，我知道圆周率是3.141593,哈哈!

#format用法
 相对基本格式化输出采用‘%’的方法，format()功能更强大，该函数把字符串当成一个模板，通过传入的参数进行格式化，并且使用大括号‘{}’作为特殊字符代替‘%’
#使用方法由两种：b.format(a)和format(a,b)。
#1、基本用法
  （1）不带编号，即“{}”
  （2）带数字编号，可调换顺序，即“{1}”、“{2}”
  （3）带关键字，即“{a}”、“{tom}”
    >>> print('{} {}'.format('千锋','教育'))  # 不带字段
         #》》千锋 教育
    >>> print('{0} {1}'.format('千锋','教育'))  # 带数字编号
         #》》千锋 教育
    >>> print('{0} {1} {0}'.format('千锋','教育'))  # 打乱顺序
         #》》 千锋 教育 千锋
    >>> print('{1} {1} {0}'.format('千锋','教育'))
         #》》教育 教育 千锋
    >>> print('{a} {b} {a}'.format(a='千锋',b='教育'))  # 带关键字
         #》》千锋 教育 千锋
#2、进阶用法
（1）< （默认）左对齐、> 右对齐、^ 中间对齐、= （只用于数字）在小数点后进行补齐
（2）取位数“{:4s}”、"{:.2f}"等.

```
## 格式化字符串格式化字符串的进阶用法   
```


方法 [str.format()](https://docs.python.org/3/library/stdtypes.html#str.format) 的基本用法如下:

> > print('We are the {} who say "{}!"'.format('knights', 'Ni'))
We are the knights who say "Ni!"
大括号和其中的字符会被替换成传入 [str.format()](https://docs.python.org/3/library/stdtypes.html#str.format) 的参数。大括号中的数值指明使用传入 [str.format()](https://docs.python.org/3/library/stdtypes.html#str.format) 方法的对象中的哪一个:

> > print('{0} and {1}'.format('spam', 'eggs'))
spam and eggs

> > print('{1} and {0}'.format('spam', 'eggs'))
eggs and spam
如果在 [str.format()](https://docs.python.org/3/library/stdtypes.html#str.format) 调用时使用关键字参数，可以通过参数名来引用值:

> > print('This {food} is {adjective}.'.format(
...       food='spam', adjective='absolutely horrible'))
This spam is absolutely horrible.
位置参数和关键字参数可以随意组合:

> > print('The story of {0}, {1}, and {other}.'.format('Bill', 'Manfred',
other='Georg'))
The story of Bill, Manfred, and Georg. `'!a'` (应用 [ascii()](https://docs.python.org/3/library/functions.html#ascii))，`'!s'` （应用 [str()](https://docs.python.org/3/library/stdtypes.html#str) ）和 `'!r'` （应用 [repr()](https://docs.python.org/3/library/functions.html#repr) ）可以在格式化之前转换值:

> > import math

> > print('The value of PI is approximately {}.'.format(math.pi))
The value of PI is approximately 3.14159265359.

> > print('The value of PI is approximately {!r}.'.format(math.pi))
The value of PI is approximately 3.141592653589793.
字段名后允许可选的 `':'` 和格式指令。这允许对值的格式化加以更深入的控制。下例将 Pi 转为三位精度。

> > import math

> > print('The value of PI is approximately {0:.3f}.'.format(math.pi))
The value of PI is approximately 3.142.
在字段后的 `':'` 后面加一个整数会限定该字段的最小宽度，这在美化表格时很有用:

> > table = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 7678}

> > for name, phone in table.items():
...     print('{0:10} ==> {1:10d}'.format(name, phone))
...
Jack       ==>       4098
Dcab       ==>       7678
Sjoerd     ==>       4127
如果你有个实在是很长的格式化字符串，不想分割它。如果你可以用命名来引用被格式化的变量而不是位置就好了。有个简单的方法，可以传入一个字典，用中括号( `'[]'` )访问它的键:

> > table = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 8637678}

> > print('Jack: {0[Jack]:d}; Sjoerd: {0[Sjoerd]:d}; '
'Dcab: {0[Dcab]:d}'.format(table))
Jack: 4098; Sjoerd: 4127; Dcab: 8637678
也可以用 ‘**’ 标志将这个字典以关键字参数的方式传入:

> > table = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 8637678}

> > print('Jack: {Jack:d}; Sjoerd: {Sjoerd:d}; Dcab: {Dcab:d}'.format(**table))
Jack: 4098; Sjoerd: 4127; Dcab: 8637678
这种方式与新的内置函数 [vars()](https://docs.python.org/3/library/functions.html#vars) 组合使用非常有效。该函数返回包含所有局部变量的字典。
要进一步了解字符串格式化方法 [str.format()](https://docs.python.org/3/library/stdtypes.html#str.format)，参见 [格式字符串语法](https://docs.python.org/3/library/string.html#formatstrings)。





### **6、理解: input()函数**

\`\`\`python
input()函数的数据类型   #函数返回类型，必为str 不管你在终端输入的是整数还是字符串， 输入值必为字符串。
   有问有答，有来有往    #终端区输入
   函数好用，赋值第一    #必须赋值
   返回类型，必为str    #输入值类型为字符串
   输入值需要整数时     #想要整数，源头转换,input()函数的结果需强制转换

```
## 6.2、知识: input()函数   
```
name = input('请输入你的名字：')
print(name)

name=input('请在以下四个选项【格兰芬多；斯莱特林；拉文克劳；赫奇帕奇】中，输入你想去的学院名字: ') #用input()收集信息
print(name)
 #》》请在以下四个选项【格兰芬多；斯莱特林；拉文克劳；赫奇帕奇】中，输入你想去的学院名字: 拉文克劳
 #》》拉文克劳

choice = int(input('请输入您的选择：'))
if choice==1:
    print('霍格沃茨欢迎您的到来')
else:
    print('您可是被梅林选中的孩子，我们不接受这个选项.')
 #》》请输入您的选择：1
 #》》霍格沃茨欢迎您的到来
    
money = int(input('你一个月工资多少钱？'))
#将输入的工资数（字符串），强制转换为整数
if money >= 10000:
#当工资数（整数）大于等于10000（整数）时
    print('土豪我们做朋友吧！')
#打印if条件下的结果
else:
#当工资数（整数）小于10000（整数）时
    print('我负责赚钱养家，你负责貌美如花～')
#打印else条件下    
 #》》你一个月工资多少钱？12000
 #》》土豪我们做朋友吧?    
    
import time
print('亲爱的同学：')
time.sleep(1)
print('我们愉快地通知您，您已获准在霍格沃茨魔法学校就读。')
time.sleep(2)
 #》》亲爱的同学：
 #》》我们愉快地通知您，您已获准在霍格沃茨魔法学校就读。

import time     #python time 时间模块
import random   #random模块 
time.sleep(1.5)
print('  \n——————现在是第一局——————' )
player_life = random.randint(100,150)   ##用于生成一个100到150的整数
player_attack = random.randint(30,50)   ##用于生成一个130到50的整数
enemy_life = random.randint(100,150)
enemy_attack = random.randint(30,50)
print('【玩家】\n血量：%s\n攻击：%s' % (player_life,player_attack))
print('------------------------')
time.sleep(1)                            # time时间模块,等待时间为1秒
print('【敌人】\n血量：%s\n攻击：%s' % (enemy_life,enemy_attack))
print('-----------------------')
time.sleep(1)
 #》》——————现在是第一局——————
 #》》【玩家】
 #》》血量：147
 #》》攻击：48
 #》》------------------------
 #》》【敌人】
 #》》血量：101
 #》》攻击：34
 #》》-----------------------

```
## 7、理解: if...elif...else   
```
#if..else...知识点:
1、单向判断：if   #含义：如果.....就....
2、双向判断：if ... else ...  # 含义：如果...就...否则...   双向判断语句是:如果不满足if的条件，就执行else下的命令。
2. 多向判断：if…elif…else…  #含义：如果...如果...否则...    三者所代表的条件是互斥的。
#if..elif..else...知识点
1. [if..elf..else..]多向判断语句是:如果不满足if的条件，就判断是否满足elif下的命令，满足执行，不满足执行else下的命令。
2. if、elif和else三者所代表的条件是互斥的。
3. elif后可不接else。
#if条件判断    
 #一、条件判断   
     1、#单向判断: if           #》》逻辑:如果..... 就.....注意:冒号下缩进
     2、#双向判断: if..else...   #》》逻辑:如果.不满足..就.注意: else需要-个平级的前提条件，条件可以是if也可以是其他
     3、#多向判断: if..elif..else.. #》》逻辑:如果..不满足.就下一个....再下一个..注意: elif需要if, 但可不需要else 
#二、if嵌套  #》》  条件套条件   额外条件要在基础条件下缩进
#三、嵌套写法 #》》 扒洋葱式写法  #》》  1.写基础条件代码 2.写基础条件1的额外条件 3.写基础条件2的额外条件

```
## 7.2、知识: if...elif...else   
```
#例一:
stonenumber=3 # 赋值语句：为宝石数量赋值
# 条件：如果你拥有的宝石数量大于等于6个
if stonenumber>=6:
    # 结果：显示‘你拥有了毁灭宇宙的力量’的结果
    print('你拥有了毁灭宇宙的力量') 
# 条件：当赋值不满足if条件时，执行else下的命令
else: 
    # 结果：显示‘去找灵魂宝石’的结果
    print('带着卡魔拉去沃弥尔星寻找灵魂宝石')
#》》带着卡魔拉去沃弥尔星寻找灵魂宝石

#例二:
weight=101   #要先为酱酱的体重赋值，酱酱的体重是101斤
# 如果体重超过100斤的条件下，就……(条件后需加冒号)
if weight>100:  
  # 就打印结果：不吃了！(注意检查是否自动缩进)
  print('不吃了')
# 如果体重没有超过100斤的条件，就……(else条件前无缩进，条件后需加冒号)
else:
 # 就打印：放心吃吧(注意检查是否自动缩进)
  print('放心吃吧')
#》》不吃了
 
#例三:  
stonenumber=5    # 为宝石数量赋值
# 条件：如果你拥有的宝石数量大于等于6个
if stonenumber>=6: 
    # 结果：显示‘就拥有了毁灭宇宙的力量’的结果
    print('你拥有了毁灭宇宙的力量') 
# 条件：如果想让宝石数量停留在5个以下，至少一个
elif 0<stonenumber<=5:
    # 结果：显示‘绯红女巫需要亲手毁掉幻视额头上的心灵宝石’的结果
    print('绯红女巫需要亲手毁掉幻视额头上的心灵宝石')
# 条件：当赋值不满足if和elif条件时，执行else下的命令，宝石数量为0个
else:
    # 结果：显示‘需要惊奇队长逆转未来’的结果
    print('需要惊奇队长逆转未来')
#》》绯红女巫需要亲手毁掉幻视额头上的心灵宝石

```
## 8、理解: 列表和字典\*\*\*\*   
```
#什么时候需要用到列表和字典?
 ●需要将数据收纳起来的时候
#什么时候用列表，什么时候用字典?
 ●当数据需要依次放好的时候用列表，就像把一堆东西堆起来的收纳方式
 ●当数据需要打上标签放好的时候用字典，就像图书馆的书架用标签分类
#列表和字典的常见用法?
 ●用于存数据和取数据，可以相互嵌套
 ●用于for循环，依次遍历列表或字典

```
## 8.2、知识: 列表   
```
s=[ '弘福寺'，'大兴善寺'，'青龙寺'，'卧龙寺']
print(s) #打印列表
#》》['弘福寺'，'大兴善寺'，'青龙寺'，'卧龙寺']
print(len(s) ) #打印列表s的长度
#》》4
print(type(s) ) #打印列表s的类型
#》》<class ! list'>
print(s[3] ) #打印列表s里面的第3个元素
#》》卧龙寺
print(s[-2] ) #打印列表s里面的倒数第二个元素
#》》青龙寺
print(s[0:4]) #打印列表s中0、1、2、3的元素
#》》['弘福寺'，'大兴善寺'，'青龙寺'，'卧龙寺']
pr int(s[1:3] ) #打印列表s中1、2的元素
#》》['大兴善寺'，'青龙寺']
print(s[1: ]) #打印列表s中第 1个和此之后的所有元素
#》》['大兴善寺'，'青龙寺'，'卧龙寺']
print(s[ :2] ) #打印列表s中第2个元素 之前的所有元素
#》》['弘福寺'，'大兴善寺']
S. append( '观音禅寺' ) #把数据'观音禅寺'放进列表s的尾部
print(s[4] ) #打印列表s里面的第4个元素(.上一步新增的)
#》》观音禅寺

```
## 9、知识:字典   
```
d ={'QQ':['甲' ,'乙'，'丙'] ,123:[ 'A'，'B' ,'C']，家' : 10000} #定义字典和列表的嵌套
a = d['QQ' ] #取出字典d中的'QQ ' 键的值，并把这个值赋值给变量a, a被赋值为列表['甲','乙'，'丙']
b = a[0] #取出列表a中的第0个索引，也就是'甲'，并把这个值赋值给变量b
print(b) #打印变量b
#》》甲
print(d[ 123] [1]) #从嵌套中提取元素，d[123]提取出['A','B' ,'C']，d[123] [1]提取出'B'
#》》B
d['家'] = 900 #改变字典中的值
print(d['家'])
#》》900
d[3.1415926] = '圆周率 ' #给 字典新增键和值
print(d)
#》》{3. 1415926: '圆周率'，'QQ':[ '甲','乙','丙'] ,123: [ 'A,'B','C'],'家' :900} 

A={ '绿色' :1, '红色' :2, '黄色' :3}
print(key)
#》》 绿色，红色，黄色
print(value)
#》》1,2,3 
    
#字典使用keys (方法) :字典提取键
A={'绿色' :1, '红色' :2, '黄色':3}
for key in A.keys():
print (key)
#》》 绿色，红色，黄色
    
#字典使用values方法:字典提取值
A={'绿色' :1, '红色' :2, '黄色' :3}
for value in A. values() :
print(value)
#》》1,2,3

#如字典使用values提取值
i='100010'
d11={'乾为天（乾卦)自强不息':'111111','坤为地（坤卦）厚德载物':'000000','水雷屯（屯卦）起始维艰':'010001','山水蒙（蒙卦）启蒙奋发':'100010','水天需（需卦）守正待机':'010111'}
for k,v in d11.items():
    if v ==i:  
        print(k)
#》》山水蒙（蒙卦）启蒙奋发

#合并列表-
例如:
list1 =  [91, 95, 97, 99]  
list2 =  [92, 93, 96, 98]
# 把 A 组成绩赋值给一个新列表，用来存合并的成绩——这个细节要注意！
list1.extend(list2)
print(list1)
#》》[91, 95, 97, 99, 92, 93, 96, 98]

#列表排序
主动搜索，掌握新知
老师鼓励你自己去探寻解决问题的方法，上网搜索一下列表的排序方法吧，是不是发现了一个以字母s开头的方法？

例如:
list3= [91, 95, 97, 99, 92, 93, 96, 98]
list3.sort()
print(list3)
#》》[91, 92, 93, 95, 96, 97, 98, 99]

#Python 求平均值

import random, numpy , math
punches = [3,45,56]
punches1 = [5,6,89]
print(punches.index(56)) # 列表的取下标
punches3 =punches.copy() #列表的复制
punches3.extend(punches1) #列表的合并
print(punches3)
punches3.sort() #列表的排列升序
print(punches3)
print(random.choice(punches3)) #随机挑选
print(random.randint(0,10)) #区间内随机生成
punches4-punches3.pop(0) # 列表内的元素删除，可以存入变量
print(punches4)
punches3.append(punches4) # 列表的添加，注意只能添加一个
print(punches3)
print(numpy.mean(punches3)) # 求平均值
print(numpy.array(punches3)) # 列表的数组显示
number = math.ceil(size*80 / time)

```
### 理解:append函数和pop()函数   
```
# append(）
1、描述：列表append()方法用于将传入的对象附加(添加)到现有列表中。
2、语法：list.append(obj)
3、参数：这是要添加到列表中的内容
4、运行后的结果返回： 已更新到原列表，不会产生结果。
 # pop()
1、描述：pop() 函数用于移除列表中的一个元素(默认最后一个元素），并返回该元素的值。
2、参数：obj – 可选参数，要移除列表元素的对象。
3、返回值：该方法返回从列表中移除的元素对象。     
 #小拓展:                         
append函数：append() 方法用于在列表末尾添加新的对象，需要注意的是每次只能添加一个元素，且该方法无返回值，但是会修改原来的列表。         #使用格式为：列表.append(内容)
pop函数：用于移除列表中的一个元素(默认最后一个元素)，并且返回该元素的值。    #使用格式为：变量=列表.pop()

```
## 知识:append函数和pop()函数   
```
#方法一:使用for循环和pop函数
students = ['小明',' 小红'，'小刚' ] 
for. i : in range(3):
student1”=”students. pop(0)
# 运用pop( )函数，将偏移量为0的元素赋值给变量student1, 也就是，把第一个座位的同学提取出来。同时更新了列表
students . append(student1)”。
# append函数，将元素添加到列表尾，将移除的student1安排到最后一个 座位。
print( students)
#打印列表
#方法二:使用while循环和pop函数
students = ['小明','小红','小刚' ] 
i=0
while i<3:
    i=i+1
    student1 = students .pop(0) #运用pop()函数，同时完成提取和删除。
    students.append(student1)   # 将移除的student1安排到最后一个座位。
    print( students )
#》》['小红', '小刚', '小明']
#》》['小刚', '小明', '小红']
#》》['小明', '小红', '小刚']
    
#方法三: for循环和切片
students =['小明','小红','小刚']
for i in range(3):
    student1= students[0]
    students=students[1:]
    students.append( student1)
    print(students)
#》》['小红', '小刚', '小明']
#》》['小刚', '小明', '小红']
#》》['小明', '小红', '小刚']

#方法四: while循环和切片
students = ['小明','小红' ,'小刚']
i=0
while i<3:
    i=i+1
    student1 = students[0]
    students =students[1:]
    students.append( student1)
    print( students)
#》》['小红', '小刚', '小明']
#》》['小刚', '小明', '小红']
#》》['小明', '小红', '小刚']

```
## items()函数语法：   
```


```
```


::dict.items()::

实例：

\`\`\`other
dict = {'老大':'15岁',
        '老二':'14岁',
        '老三':'2岁',
        '老四':'在墙上'
        }
print(dict.items())
for key,values in dict.items():
    print(key + '已经' + values + '了')
    

以上实例输出结果为：

other
dict_items([('老大', '15岁'), ('老二', '14岁'), ('老三', '2岁'), ('老四', '在墙上')])
老大已经15岁了
老二已经14岁了
老三已经2岁了
老四已经在墙上了了


版权声明：本文为CSDN博主「逸少凌仙」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。

原文链接：[https://blog.csdn.net/u012424313/article/details/86499194](https://blog.csdn.net/u012424313/article/details/86499194)



**::切片::**

若要在循环内部修改正在遍历的序列（例如复制某些元素），建议您首先制作副本。在序列上循环不会隐式地创建副本。切片表示法使这尤其方便:

> > words = ['cat', 'window', 'defenestrate']

> > for w in words[:]:  # Loop over a slice copy of the entire list.
...     if len(w) > 6:
...         words.insert(0, w)
print(words)

> > \#》》['defenestrate', 'cat', 'window', 'defenestrate']



```
```


```
## 10、知识: while循环   
```




### 理解: 循环

\`\`\`python
for循环和while循环最大的区别在于【循环的工作量是否确定】，
for循环就像空房间依次办理业务，直到把【所有工作做完】才下班。
while循环就像哨卡放行，【满足条件就一直工作】，直到不满足条件就关闭哨卡

#什么时候需要用到循环?
  ●当发现存在“重复性或规律性”任务的时候，可以用循环来“解决重复劳动”
#什么时候用for循环，什么时候用while循环?
  ●知道循环次数的时候优先用for循环，不知道循环次数的时候用while然后设置“哨兵”
#分析循环:初始化条件? 控制循环的条件? 反复做的事?怎样进入下一个循环?
#for循环的常见用法?
  ●遍历range()函数，如“for i in range(10)”
  ●遍历列表，如“for i in[1,2,3]”
  ●遍历字典(键)，如“for i in {1:1,2:2,3:3}"

#range()函数用法: 
如: range(a,b,c)
a:计数从a开始。不填时，默认从0开始
#例如，range(1,5), 表示从1开始生成
b:计数到b结束，但不包括b
#例如，range(11) ，表示从0开始到11结束，不包括11
c:计数的间隔，不填时默认为1
#例如，range(0, 30, 5)，表示计数的间隔5 
       
#如何跳出while True死循环：
鼠标点一下终端区， 键盘按ctrl+c， 无反应则多按几次。
刷新网页，然后修改代码，将while True改成while False.  或故意写错代码，点击跳过

#例一:
a=0
while a<5:      #只要a<5这个条件成立，就不停地办事（把a+1的结果打印出来），直到条件不成立，办事流程就停止.
    a=a+1
    print(a)
#》》1,2,3,4,5

#例二:
a=0
while a<5:
    print(a)
     a=a+1
#》》0,1,2,3,4

#例三:
a=0
while a<5:
    a=a+1
print(a)
#》》5

#例四:
man = ''  # 注：这个''代表空字符串
while man != '有':
    man = input('有没有愿意为小龙女死的男人？没有的话就不能出古墓。')
print('小龙女可以出古墓门下山啦~')
#》》有没有愿意为小龙女死的男人？没有的话就不能出古墓。没有
#》》有没有愿意为小龙女死的男人？没有的话就不能出古墓。没有
#》》有没有愿意为小龙女死的男人？没有的话就不能出古墓。有
#》》小龙女可以出古墓门下山啦~

#例五:
password = ''  # 变量password用来保存输入的密码
while password != '816':
    password = input('请尝试输入密码：')
print('欢迎回家！')
#》》请尝试输入密码：6456
#》》请尝试输入密码：816
#》》欢迎回家！

```
## 11、知识: for循环   
```
#例一:
for i in [1,2,3,4,5]:
    printi(i*5)            #遍历列表乘以数字5
#》》5,10,15,20,25

#例二: 
for i in range(5):         #遍历5次:0,1,2,3,4
    print('明日复明日')      #循环打印5次 明日复明日
#》》明日复明日,明日复明日,明日复明日,明日复明日,明日复明日

#例三:
for i in range(1,4) :
    print('明日复明日，明日何其多。')   #用for循环把诗句打印3遍
#》》明日复明日，明日何其多。
#》》明日复明日，明日何其多。
#》》明日复明日，明日何其多。

#例四:
j = 1
while j<4 :
    print ('明日何其多，明日何其多。')   #用while循环把诗句打印3遍
    j =j+1
#》》明日复明日，明日何其多。
#》》明日复明日，明日何其多。
#》》明日复明日，明日何其多。

#例五:
for i in range(1,10):
    print(i*5)             #用for循环“1到10分别乘以5”的
#》》 5,10,15,20,25,30,35,40,45

#例六:
d = {'小明':'醋','小红':'油','小白':'盐','小张':'米'}
for i in d:
    print(d[i])
#》》醋,油,盐,米

# 循环之break、continue、exit用法:
1、程序遇到 continue，跳过循环后面，进行下一次循环
2、程序遇到 break，结束循环，之后循环外部的代码
3、程序遇到 exit()，结束程序，不管后面的代码在循环里还是循环外都不执行
#continue 一个是结束本次循环执行下一次
#break 一个是结束循环，执行循环外的内容
   假如一整个循环本来需要循环5次，而实际上可能只需要循环2次就能够得到我们想要的结果，那么后面3次循环就不需要执行，这个时候就可以直接break，后面的3次循环就不执行了。
   如果一次循环本来需要执行5行代码，而实际上可能执行前2行代码就能够得到我们想要的结果了，那后面的3行代码就不需要执行，这个时候就可以直接continue，跳过后面2行代码，进入下一次循环。
那还有就是exit()函数。exit()和break的区别是什么呢？
#break()是结束循环，执行循环外的内容
#exit()是结束程序，这个程序里面不管循环外还是循环内都不执行了。

例如一:
resumes = ['小李','小王','小张','老李','老王','老张']
num = 0 #num表示录取的人数
for i in resumes:
# 如果录取人数大于3人，就停止招聘。
  if num >=3:
    break
# 如果用人部门满意就直接录取，录取人数+1，不确定的话就移交用人部门。
  department_admissin = input('department，你是否非常想要 '+i+':')
  if department_admissin =='yes':
    num = num+1
    print('恭喜'+i+'应聘成功')
    continue
  # 如果hr满意就直接录取，录取人数+1，不确定的话就移交用人部门。
  hr_admissin = input('hr，你是否非常想要t '+i+':')
  if hr_admissin =='yes':
    num = num+1
    print('恭喜'+i+'应聘成功')
    continue
# 如果老板满意就直接录取，录取人数+1，不确定的话就进入待定。
  boss_admissin = input('boss，你是否非常想要 '+i+':')
  if boss_admissin =='yes':
    num = num+1
    print('恭喜'+i+'应聘成功')
    continue  


例如二:
from sys import exit
resumes = ['小李','小王','小张','老李','老王','老张']
num = 0   #num表示录取的人数
for i in resumes:
  department_admissin = input('department，你是否非常想要 ' + i + ':')
  if department_admissin == 'yes':
    num = num + 1
    if num == 3:
      print('enough~')
      exit()
    print('恭喜' + i + '应聘成功')
    continue
  else:
    print(i, '此人不在候选名单')

代码拆解方法:
#总体思路：
#1.1展示随机属性&随机生命值和攻击值
#1.2展示PK过程
#1.3展示每一局的PK结果，并设置三局两胜，就是在每一局外面设置for i in range(1,4)的循环
#1.4展示三局两胜的最后PK结果，借助第三方变量，类似篮球积分
#1.5设置三局两胜在输入某个键时，是否继续循环，也就是while True部分

import time
import random
while True:
    player_victory = 0
    enemy_victory = 0 
    for i in range(1,4):
        time.sleep(1.5)
        print('  \n——————现在是第 %s 局——————' % i)
        player_life = random.randint(100,150)
        player_attack = random.randint(30,50)
        enemy_life = random.randint(100,150)
        enemy_attack = random.randint(30,50)

        print('【玩家】\n血量：%s\n攻击：%s' % (player_life,player_attack))
        print('------------------------')
        time.sleep(1)
        print('【敌人】\n血量：%s\n攻击：%s' % (enemy_life,enemy_attack))
        print('-----------------------')
        time.sleep(1)

        while player_life > 0 and enemy_life > 0:
            player_life = player_life - enemy_attack 
            enemy_life = enemy_life - player_attack
            print('你发起了攻击，【敌人】剩余血量%s' % enemy_life)
            print('敌人向你发起了攻击，【玩家】的血量剩余%s' % player_life)
            print('-----------------------')
            time.sleep(1.2)

        if player_life > 0 and enemy_life <= 0:
            player_victory += 1
            print('敌人死翘翘了，你赢了！')
        elif player_life <= 0 and enemy_life > 0:
            enemy_victory += 1
            print('悲催，敌人把你干掉了！')
        else:
            print('哎呀，你和敌人同归于尽了！')

    if player_victory > enemy_victory :
        time.sleep(1)
        print('\n【最终结果：你赢了！】')
    elif enemy_victory > player_victory:
        print('\n【最终结果：你输了！】')
    else: 
        print('\n【最终结果：平局！】')

    a1 = input('要继续游戏吗，请输入n退出，输入其他继续：')  # 在 while True 循环中设置跳出条件。
    if a1 == 'n':
        break

import random
import time
# 将抽奖程序封装成函数
def choujiang(q,w,e):  # 定义一个抽奖函数，带有3个参数，也就是3位候选人
    luckylist = [q,w,e]  # 定义一个中奖名单的列表
    a = random.choice(luckylist)  # 在中奖名单里面随机选择
    print('开奖倒计时',3)
    time.sleep(1)
    print('开奖倒计时',2)
    time.sleep(1)
    print('开奖倒计时',1)
    time.sleep(1)
    image = '''
    /\_)o<
    |      \\
    | O . O|
    \_____/
    '''
    print(image)
    print('恭喜'+a+'中奖！')
choujiang('虚竹','萧峰','段誉')  # 调用函数

#》》奖倒计时 3
#》》开奖倒计时 2
#》》开奖倒计时 1
#》》  /\_)o<
#》》 |      \
#》  | O . O|
#》》 \_____/
#》》恭喜段誉中奖！

```
## 12理解:自定义函数   
```
#函数
#定义函数的语法
1.def 函数名 (参数) :
2.函数体
3.return语句

#函数是组织好的、可以重复使用的、用来实现单-功能的代码。
定义函数的语法:1、def函数名(参数) ;2、函数体3、return语句
例如:
# 函数名：1. 名字最好能体现函数的功能，一般用小写字母和单下划线、数字等组合
#      2. 不可与内置函数重名（内置函数不需要定义即可直接使用）
def math(x):
# 参数：根据函数功能，括号里可以有多个参数，也可以不带参数，命名规则与函数名相同
# 规范：括号是英文括号，后面的冒号不能丢
    y = 3*x + 5
# 函数体：函数的执行过程，体现函数功能的语句，要缩进，一般是四个空格
    return y
# return语句：后面可以接多种数据类型，如果函数不需要返回值的话，可以省略

#如果要优化上面代码的结构,我们可以创建一个主函数，用来调用几个子函数的方法
#如下所示，我们可以把每个独立的功能封装到每个单独的函数中，然后用一个主函数打包这些单独的函数，最后再调用主函数.
def 函数a():#某个功能独立的函数a
def 函数b() :#某个功能独立的函数b
def 函数c():#某个功能独立的函数c
  .....
     .....
def 主函数() :#将各个功能打包到一起的函数，形成“程序入口”
函数 a() #调用a函数
函数 b() #调用b函数
函数 c() #调用c函数
  .....
主函数 () # 运行主函数，就能让全部代码执行起来

```
## 12.1知识:自定义函数   
```
例一:
def math(x):        #定义函数
    y = x ** 2 + x  #函数主体
    return y
a=math(20)          #函数赋值
b=math(30)          #函数赋值
print(a,b)          #调用并打印函数
#》》420 930

例二:
#直接运行代码即可    
def opening():         #定义函数
    print('总有一种味道能温暖你～')
    print('深夜食堂正式开业啦！')
    print('欢迎来自五湖四海的你前来品尝!')
opening()             #直接运行函数
#》》总有一种味道能温暖你～
#》》深夜食堂正式开业啦！
#》》欢迎来自五湖四海的你前来品尝!

例三:
def menu(appetizer, course):        #定义函数
    print('一份开胃菜：' + appetizer)
    print('一份主食：' + course)
menu('话梅花生','牛肉拉面')
#》》一份开胃菜：话梅花生
#》》一份主食：牛肉拉面

例四:
def  menu(appetizer, course, dessert = '绿豆沙'):
    print('一份开胃菜：' + appetizer)
    print('一份主食：' + course)
    print('一份甜品：' + dessert)
menu('话梅花生','牛肉拉面')
#因为已经默认将'绿豆沙'传递给dessert，调用时无须再传递。
#》》一份开胃菜：话梅花生
#》》一份主食：牛肉拉面
#》》一份甜品：绿豆沙

例五:
import random 
appetizer = ['话梅花生','拍黄瓜','凉拌三丝']
def coupon(money):
    if money < 5:
        a = random.choice(appetizer)   #随机选择 appetizer列表内容
        return a                        #返回到赋值a            
    elif 5 <= money < 10: 
        b = random.choice (appetizer)
        return b, '溏心蛋'
result = coupon(6)         # result是一个元组
print(result[0])
print(result[1])
#》》凉拌三丝
#》》溏心蛋
例六:
#另外一种方式：我们也可以同时定义多个变量，来接收元组中的多个元素（看最后四行代码，直接运行即可）：
import random
appetizer = ['话梅花生', '拍黄瓜', '凉拌三丝']
def coupon(money):
    if money < 5:
        a = random.choice(appetizer)
        return a, ''
    elif 5 <= money < 10:
        b = random.choice(appetizer)
        return b, '溏心蛋'

dish, egg = coupon(7)   # 元组的两个元素分别赋值给变量dish和egg
print(dish)
print(egg)
#》》拍黄瓜
#》》溏心蛋


例七:
rent = 3000
def cost():
    global variable_cost     #定义variable_cost 为全局变量
    utilities = int(input('请输入本月的水电费用'))
    food_cost = int(input('请输入本月的食材费用'))
    variable_cost = utilities + food_cost
    print('本月的变动成本是' + str(variable_cost))

def sum_cost():
    sum = rent + variable_cost
    print('本月的总成本是' + str(sum))
cost()
sum_cost()
#》》请输入本月的水电费用87
#》》请输入本月的食材费用890
#》》本月的变动成本是977
#》》本月的总成本是3977

例八:
#函数嵌套
def div(num1, num2):
    growth = (num1 - num2) / num2
    percent = str(growth * 100) + '%'
    return percent

def warning():
    print('Error: 你确定上个月一毛钱都不赚不亏吗？')

def main():
    while True:
        num1 = float(input('请输入本月所获利润'))
        num2 = float(input('请输入上月所获利润'))
        if num2 == 0:
            warning()
        else:
            print('本月的利润增长率：' + div(num1,num2))
            break

main()
#》》请输入本月所获利润35000
#》》请输入上月所获利润33000
#》》本月的利润增长率：6.0606060606060606%


#简单自定义函数嵌套:思考函数如何有效嵌套?
def yang():
    age=int(input('请输入您的年龄?：'))
    if age>=18:
        print("可以进网吧嗨皮……")
    else:
        print("你还没长大，应该回家写作业！")

def warning():
    print('Error: 你确定您输入的密码正确吗？')

def main():
    for i in range(3):
        tssw=input('请输入登陆密码?')
    if tssw=='861':
       yang()
    else:
          warning()
        
main()

#》》请输入登陆密码?861
#》》请输入您的年龄?：18
#》》可以进网吧嗨皮……

#解决输入不是整数报错的问题
#代码要点有两个：（1）因为不知道用户什么时候才会输入正确，所以设置while循环来接受输入，只要用户输入不是数字就会一直循环，输入了数字就break跳出循环。（2）使用try……except……语句，当用户输错的时候会给予提示。
while True:
    try:
        age = int(input('你今年几岁了？'))
        break
    except ValueError:
        print('你输入的不是数字！')
if age < 18:
    print('不可以喝酒噢')
#》》请输入一个整数：为
#》》要输入整数噢

```
## 编程bug处理:   
```
#自检清单
1.漏了末尾的冒号，如if语句、循环语句、定义函数
2.缩进错误，该缩进的时候没缩进，不该缩进的时候缩进了
3.把英文符号写成中文符号，如:‘’ () : ,
4.字符串拼接的时候，把字符串和数字拼在一起
5.没有定义变量
6. '=='和'=’混用
#解决思路不清bug的三步法          #用来解决思路不清的两个工具:注释和print()函数
1.用“#”把感觉会出问题的代码段注释掉
2.利用print()语句，展示关键步骤的操作结果
3.根据print出来的东西，-步步寻找和解决问题
遇到关键步骤时print出来，看是否达到我们所期望的结果，以此来揪出错误的那一步。
用#号暂时注释部分代码,计算机是不会执行代码中的#号和其之后的内容的。

是try…except…语句，具体用法如下:
try:
    ......
    ......
#尝试执行下列代码
#代码，要缩进
except ***:
    ....
    ....
#除非发生报错，***是报错类型。一旦报错就执行下列代码:
#报错后执行的代码，要缩进

```
## 类的练习   
```
类的创建和调用
类的创建: class 语句
类的属性创建:赋值语句
实例方法的创建: def method1 (self):
类的实例化:实例名=类名()
调用类的属性:实例名.属性
调用类的方法:实例名.方法()


class Computer:               #类的创建: class+类名+冒号，后面语句要缩进
    screen = True            #类的属性创建:通过赋值语句(即定义“是怎样的”)
    def start(self):     #实例方 法的创建: def +方法名(self):  参数self的特殊之处：在定义时不能丢，在调用时要忽略。
        print('电脑正在开机....')         #方法具体的执行过程，即定义“能做什么”
注:
1.在类中赋值的变量叫作属性，类中定义的函数叫作方法(以此和普通函数区分)
2.实例方法是指类中参数带self的函数，是类方法的一种形式，也是最常用的用法。
3.课堂中所讲“类的方法”，均指实例方法，想了解其他方法，可自行查询相关文档。
注:实例方法的创建语句，和函数的定义语句很类似，唯一不同的是：实例方法中有个必须放在首位的参数self。
    
    
    类的实例化
语法:实例名=类名()
例子: my_ computer = Computer()
意义:我们有了一个实例，一个“可调用所属类的所有属性和方法”的实例。调用的语法是实例名.属性和实例名.方法
    
 # 特殊方法：初始化方法（也叫构造函数）
定义初始化方法的格式是def __init__(self)，是由init加左右两边的【双】下划线组成（ initialize “初始化”的缩写）
初始化方法的作用在于：当每个实例对象创建时，该方法内的代码无须调用就会自动运行。
# 阅读代码后直接运行    
class Chinese:

    def __init__(self): 
        print('很高兴遇见你，我是初始化方法')
person = Chinese()
#》》很高兴遇见你，我是初始化方法


#类的继承和定制
广东人属于中国人(继承 了中国人的属性和方法)
A类属于B类(继承了B类的属性和方法)
继承的基础语法
#继承的语法
C lass A (B) :    #注:小括号和冒号都是英文格式
       ▼   ▼
     子类名 ▼
          父类名
#各级实例和各级类间的关系
1.子类创建的实例，同时属于父类;
2.父类创建的实例，不属于子类;
3.所有实例，都属于根类object。

#多层继承:
class B(A) :
class C(B) :
作用:类在纵向上的深度拓展
例子:中国人继承自地球人，广东人又继承自中国人。
特点:子类创建的实例，可调用所有层级的父类的属性和方法。
#多重继承:
class A(B,C,D) :
作用:类在横向上的宽度拓展
例子:在广东定居的江苏人，同时继承了广东人和江苏人的一些特征。
特点:就近原则:在子类调用属性和方法时，优先考虑靠近子类(即靠左)的父类。

例一;
# 类名首字母大写
class Chinese:
    # 用赋值语句，创建类的属性
    eye = 'black'

    # 创建实例方法时，不要漏了 self
    def eat(self):
        print('吃饭，选择用筷子。')
        
例二:        
class Chinese:      # 创建一个类
    eye = 'black'    # 用赋值语句，创建类的属性

    def eat(self):      # 创建实例方法时，不要漏了 self
        print('吃饭，选择用筷子。')

wufeng = Chinese()   # 类的实例化
print(wufeng.eye)   # 实例调用类属性
wufeng.eat()  # 调用类中的方法（传参不用管self）
#》》black
#》》吃饭，选择用筷子。

例题三:
class Chinese:

    name = '吴枫'  # 类属性name

    def say(self):     
        print(self.name + '是中国人')

person = Chinese()   # 创建Chinese的实例person
person.say()         # 调用实例方法

例题三:
class Chinese:
    def __init__ (self):
        self.mouth = 1  # self.不能丢
        self.eye = 2
    
    def body(self):
        print('我有%s张嘴巴' % self.mouth)
        print('我有%s只眼睛' % self.eye)

person = Chinese()
person.body()
#》》我有1张嘴巴
#》》我有2只眼睛

例题三:
class Chinese:

    def __init__(self, name, birth, region):
        self.name = name   # self.name = '吴枫' 
        self.birth = birth  # self.birth = '广东'
        self.region = region  # self.region = '深圳'

    def born(self):
        print(self.name + '出生在' + self.birth)

    def live(self):
        print(self.name + '居住在' + self.region)    

person = Chinese('吴枫','广东','深圳') # 传入初始化方法的参数
person.born()
person.live()

例题三:
class Chinese:  # 类的创建
    eye = 'black'  # 类属性的创建

    def __init__(self,hometown):  # 类的初始化方法
        self.hometown = hometown  # 实例属性的创建
        print('程序持续更新中……')  # 初始化中的语句
    
    def born(self):  # 实例方法的创建
        print('我生在%s。'%(self.hometown))  # 方法的具体语句

wufeng = Chinese('广东')  # 类的实例化
print(wufeng.eye)  # 打印实例的属性（从类传递的）
wufeng.born()  # 实例方法的调用

#类的书籍借阅系统例题:
class Book:
 
    def __init__(self, name, author, comment, state = 0):
        self.name = name
        self.author = author
        self.comment = comment
        self.state = state
 
    def __str__(self):
        status = '未借出'
        if self.state == 1:
            status = '已借出'
        return '名称：《%s》 作者：%s 推荐语：%s\n状态：%s ' % (self.name, self.author, self.comment, status)
 
class BookManager:

    books = []        #存储书籍的列表，每一个元素都是Book的实例对象
    def __init__(self):
        book1 = Book('惶然录','费尔南多·佩索阿','一个迷失方向且濒于崩溃的灵魂的自我启示，一首对默默无闻、失败、智慧、困难和沉默的赞美诗。')
        book2 = Book('以箭为翅','简媜','调和空灵文风与禅宗境界，刻画人间之缘起缘灭。像一条柔韧的绳子，情这个字，不知勒痛多少人的心肉。')
        book3 = Book('心是孤独的猎手','卡森·麦卡勒斯','我们渴望倾诉，却从未倾听。女孩、黑人、哑巴、醉鬼、鳏夫的孤独形态各异，却从未退场。',1)         # 创建三个实例对象
        self.books.append(book1)   # 往列表依次添加元素，注意调用类属性books时，self不能丢
        self.books.append(book2)   # self.books = [book1, book2, book3]  
        self.books.append(book3)  # 上面三行代码，可简化为一行，即直接创建列表。这种情况下，可不用在前面创建空列表。
 
    def menu(self):
        print('欢迎使用流浪图书管理系统，每本沉默的好书都是一座流浪的岛屿，希望你有缘发现并着陆，为精神家园找到一片栖息地。\n')
        while True:
            print('1.查询所有书籍\n2.添加书籍\n3.借阅书籍\n4.归还书籍\n5.退出系统\n')
            choice = int(input('请输入数字选择对应的功能：'))
            if choice == 1:
                self.show_all_book()   # 调用方法show_all_book()
            elif choice == 2: 
                self.add_book()         # 调用方法add_book()
            elif choice == 3:
                self.lend_book()         # 调用方法lend_book()
            elif choice == 4:
                self.return_book()        # 调用方法return_book()
            else:
                print('感谢使用！愿你我成为爱书之人，在茫茫书海里相遇。')
                break
 
    def show_all_book(self):
        print('书籍信息如下：')
        for book in self.books:
            print(book)
            print('')

    def add_book(self):
        new_name = input('请输入书籍名称：')
        new_author =  input('请输入作者名称：')
        new_comment = input('请输入书籍推荐语：')               # 获取书籍相应信息，赋值给属性
        new_book = Book(new_name, new_author, new_comment)  # 传入参数，创建Book类实例new_book 
        self.books.append(new_book)                     # 将new_book添加到列表books里     
        print('书籍录入成功！\n')

    def check_book(self,name):
        for book in self.books:      # 遍历列表的每个元素，即每个Book实例
            if book.name == name:       # 如果存在有实例名称与输入书籍名称是一样的
                 return book            # 返回该实例对象，遇到return语句方法停止执行 
        else:
            return None

    def lend_book(self):
        name = input('请输入书籍的名称：')
        res = self.check_book(name)

        if res != None:
            if res.state == 1:
                print('你来晚了一步，这本书已经被借走了噢')
            else:
                print('借阅成功，借了不看会变胖噢～')
                res.state = 1
        else:
            print('这本书暂时没有收录在系统里呢')
    
    def return_book(self):
        name = input('请输入归还书籍的名称：')
        res = self.check_book(name)      # 调用check_book方法，将返回值赋值给变量res
        if res == None:                # 如果返回的是空值，即这本书的书名不在系统里
            print('没有这本书噢，你恐怕输错了书名～')
        else:                       # 如果返回的是实例对象
            if res.state == 0:      # 如果实例属性state等于0，即这本书的借阅状态为'未借出'
                print('这本书没有被借走，在等待有缘人的垂青呢！')
            else:                # 如果实例属性state等于1，即状态为'已借出'
                print('归还成功！')
                res.state = 0   # 归还后书籍借阅状态为0，重置为'未借出'
 
manager = BookManager()
manager.menu()

```
## open()函数   
```



open('/Users/Ted/Desktop/test/abc.txt')   #绝对路径   #Mac里路径写法
open('abc.txt')    #相对路径
#相对路径也可以写成open('./abc.txt')
#Windows的绝对路径通常要稍作处理，写成以下两种格式
open('C:\\Users\\Ted\\Desktop\\test\\abc.txt')   
#将'\'替换成'\\'
open(r'C:\Users\Ted\Desktop\test\abc.txt')
#在路径前加上字母r
file1 = open('/Users/Ted/Desktop/test/abc.txt','r',encoding='utf-8')   
#这里是字符串 'r'，表示 read，表示我们以读的模式打开了这个文件。
#【第1步-开】使用open()函数打开文件
file1 = open('/Users/Ted/Desktop/test/abc.txt', 'r',encoding='utf-8') 
filecontent = file1.read()  
#【第2步-读】以用read()函数进行读取的操作
file1 = open('/Users/Ted/Desktop/test/abc.txt','r',encoding='utf-8') 
filecontent = file1.read()   
print(filecontent)
#【第3步-关】关闭文件，使用的是close()函数。
file1 = open('/Users/Ted/Desktop/test/abc.txt','r',encoding='utf-8') 
filecontent = file1.read()            
print(filecontent)
file1.close()      



```
## 使用write()函数   
```



file1 = open('/Users/Ted/Desktop/test/abc.txt', 'w',encoding='utf-8') 
file1.write('张无忌\n')   #\n表示另起一行。  
file1.write('宋青书\n')  
'w'写入模式会给你暴力清空掉文件，然后再给你写入。如果你只想增加东西，而不想完全覆盖掉原文件的话，就要使用'a'模式，表示append，你学过，它是追加的意思。
file1 = open('/Users/Ted/Desktop/test/abc.txt', 'a',encoding='utf-8') 
#以追加的方式打开文件abc.txt
file1.write('张无忌\n')     
#把字符串'张无忌'写入文件file1
file1.write('宋青书\n')     
#把字符串'宋青书'写入文件file1
使用close()函数
file1 = open('/Users/Ted/Desktop/test/abc.txt','a',encoding='utf-8') 
file1.write('张无忌\n')     
file1.write('宋青书\n')     
file1.close()     
这里再顺便补充一个用法，为了避免打开文件后忘记关闭，占用资源或当不能确定关闭文件的恰当时机的时候，我们可以用到关键字with，之前的例子可以写成这样：
#写文件的三步法:开一写一关
file1 = open(' /Users/Ted/Desktop/test/abc. txt','a' ,encoding='utf-8')#以追加的方式打开文件"abc. txt"
file1.write( '张无忌\n')   #再把字符串“张无忌’写入文件file1
file1. close()       #关闭文件 
 
# 普通写法
file1 = open('abc.txt','a') 
file1.write('张无忌') 
file1.close()



```
## 使用with关键字的写法   
```


with open('abc.txt','a') as file1:
#with open('文件地址','读写模式') as 变量名:
    #格式：冒号不能丢
    file1.write('张无忌') 
    #格式：对文件的操作要缩进
    #格式：无需用close()关闭

    
#以下是新建名称为scores.txt的文件内容:    
罗恩 23 35 44
哈利 60 77 68 88 90
赫敏 97 99 89 91 95 99
马尔福 100 85 90   
#函数 readlines()，也就是“按行读取”
file1 = open('/Users/Ted/Desktop/scores.txt','r',encoding='utf-8') 
file_lines = file1.readlines()      
file1.close()
print(file_lines)
#》》['罗恩23 35 44\n'，'哈利60 77 68 88 90\n', '赫敏97 99 89 91 95 99\n', '马尔福100 85 90'] 

file1 = open('/Users/Ted/Desktop/scores.txt','r',encoding='utf-8') 
file_lines = file1.readlines()
file1.close()
for i in file_lines:    #用for...in...把每一行的数据遍历
    print(i)            #打印变量i
#》》罗恩 23 35 44
#》》哈利 60 77 68 88 90
#》》赫敏 97 99 89 91 95 99
#》》马尔福 100 85 90

#split()函数把字符串分开
file1 = open('/Users/Ted/Desktop/scores.txt','r',encoding='utf-8') 
file_lines = file1.readlines()
file1.close()
for i in file_lines:   #用for...in...把每一行的数据遍历  
    data =i.split()    #把字符串切分成更细的一个个的字符串
    print(data)        #打印出来看看
#》》['罗恩','23','35','44']
#》》['哈利','60' ,'77','68','88' ,'90']
#》》['赫敏'，'97', '99' ,'89','91','95','99']
#》》['马尔福','100','85','90']

#join()函数，是把字符串合并的。
a=['c','a','t']
b=''
print(b.join(a))
c='-'
print(c.join(a))
#》》cat
#》》c-a-t

#计算他们总成绩的例题:
file1 = open('/Users/Ted/Desktop/scores.txt','r',encoding='utf-8') 
file_lines = file1.readlines()
file1.close()
for i in file_lines:
    data =i.split()    
    sum = 0                    #先把总成绩设为0
    for score in data[1:]:     #遍历列表中第1个数据和之后的数据
        sum = sum + int(score) #然后依次加起来，但分数是字符串，所以要转换    
    result = data[0]+str(sum)  #结果就是学生姓名和总分
    print(result)
#》》罗恩102
#》》哈利383
#》》赫敏570
#》》马尔福275

file = open('/Users/Ted/Desktop/scores.txt','r',encoding='utf-8') 
file_lines = file.readlines()
file.close()
final_scores = [ ]             #新建一个空列表
for i in file_lines:
    data =i.split()    
    sum = 0                    
    for score in data[1:]:     
        sum = sum + int(score)     
    result = data[0]+str(sum)+'\n'     #后面加上换行符，写入的时候更清晰。 
    final_scores.append(result)        #每统计一个学生的总分，就把姓名和总分写入空列表
winner = open('/Users/Ted/Desktop/winner.txt','w',encoding='utf-8') 
#打开一个叫winner.txt的文件。(如果电脑中不存在winner.txt的话，这行代码会帮你自动新建一个空白的winner.txt)
winner.writelines(final_scores)
#final_scores是一个列表，而write()的参数必须是一个字符串，而writelines()可以是序列，所以我们使用writelines()。
winner.close()   #关闭文件。你记得不要把括号丢掉。

```
## py模块   
```
# 模块是最高级别的程序组织单元:模块》》变量》》函数  类 》》 变量 》》 函数
 模块
 ▼ 
 变量》》函数      #模块:“.py”后缀的文 件即模块
 ▼  
 类 》》变量 》》函数       #类:使用class语句封装一个类;  函数:使用def语句封装一个函数; 变量:使用赋值语句赋值一个变量
 ▼   
其他可执行语句 
封装函数需要用def语句，封装类需要用class语句，但封装模块不需要任何语句,之所以不用任何语句，是因为每一份单独的Python代码文件（后缀名是.py的文件）就是一个单独的模块。

          #模块相关语句
import语句 : 
1.使用“import(模块名)”导入模块
2.可以使用“import(模块名)as(别名)”为模块名取别名
3.导入模块后，在调用模块中的变量/函数/类的时候，要加上“模块名.”格式
from .. import ... 语句:
1.from(模块名)impor t(指定的内容)
2.导入模块，并且可以直接使用指定的内容(可以是变量、函数、类)
if _name_ == '_ main_'
1.通常在主模块中使用，表示这是“程序的入口”
2.当该模块作为被导入的模块时，if _name_ == '_ main_'后面的代码不会被运行。
        
        #模块三问
1.这模块有哪些函数可用?(可以通过dir()函数查询)
2.有哪些属性或方法可用?(去网上看文档或找教程) 
3.使用格式是什么?(从文档或教程中搜集案例)
比较小的模块（比如random模块）可以通过这样的方式自学，大型模块的学习就比较困难（除非你有充足的专业背景知识）。
例如数据分析需要用到pandas和NumPy模块，网页开发要用到Django模块等等，这些大型模块最好还是在课程上系统学习，避免散乱的学习形不成知识体系。


# 这是主程序main.py
# 请阅读代码注释
import test  # 导入test模块
print(test.a)  # 使用“模块.变量”调用模块中的变量
test.hi()  # 使用“模块.函数()”调用模块中的函数
A = test.Go2()  # 使用“变量 = 模块.类()”实例化模块中的类
print(A.a)  # 实例化后，不再需要“模块.”
A.do2()  # 实例化后，不再需要“模块.”

例如:
# 【文件：story.py】
sentence = '从前有座山，'
def mountain():
    print('山里有座庙，')
class Temple:
    sentence = '庙里有个老和尚，'
    def reading(self):
        print('在讲一个长长的故事。')

# 【文件：main.py】
import story
for i in range(10):
    print(story.sentence)
    story.mountain()
    A = story.Temple()
    print(A.sentence)
    A.reading()
    print()
#》》庙里有个老和尚，
#》》在讲一个长长的故事。

#》》从前有座山，
#》》山里有座庙，
#》》庙里有个老和尚，
#》》在讲一个长长的故事。
import语句还有一种用法是import…as…。比如我们觉得import story太长，就可以用import story as s语句，意思是为“story”取个别名为“s”。
上面的案例中，main.py文件可以写成这样：
# 文件：main.py
import story as s
for i in range(10):
    print(s.sentence)
    s.mountain()
    A = s.Temple()
    print(A.sentence)
    A.reading()
    print()
#我们需要同时导入多个模块时，可以用逗号隔开。比如import a,b,c可以同时导入“a.py，b.py，c.py”三个文件。


from … import … 语句:
格式如下:
from (模块名) import (指定模块中的变量名/函数名/类名)
效果:
1.导入模块中的指定部分(变量名/函数名/类名)
2，导入后的指定的部分可以直接使用，无需加上“模块。”前缀
如:
# 【文件：test.py】
def hi():
    print('函数“hi”已经运行！')
# 【文件：main.py】
from test import hi  # 从模块test中导入函数“hi”
hi()  # 使用函数“hi”时无需加上“模块.”前缀
#》》函数“hi”已经运行！

if __name__ == '__main__'语句:
【指明】某个py文件是程序的运行入口，我们可以在该py文件中写出这样的代码：  
# 【文件：xx.py】
代码块 ①……
if __name__ == '__main__':   
    代码块 ②……
 #1.当xx.py文件被直接运行时，代码块②将被运行。2.当xx.py文件作为模块是被其他程序导入时，代码块②不被运行。

使用他人的模块:
import time和import random其实就是在导入time和random模块。
如:
import time   
print('第一句话，过两秒出现第二句。')
time.sleep(2)
print('第二句话。')
#》》第一句话，过两秒出现第二句。
#》》第二句话。
import random  
a = random.randint(0,100)  # 随机从0-100（包括0和100）之间抽取一个数字
print(a)
#》》17
#这两个例子中的第一句代码import time和import random其实就是在导入time和random模块。

Python作为一门胶水语言，一个强大的优势就是它拥有许多第三方的模块可以直接拿来使用。
如果是第三方编写的模块，我们需要先从Python的资源管理库下载安装相关的模块文件。
下载安装的方式是打开终端，Windows用户输入pip install + 模块名；苹果电脑输入：pip3 install + 模块名，点击enter即可。（需要预装python解释器和pip）比如说，爬虫时我们会需要用到requests这个库（库是具有相关功能模块的集合），就需要在终端输入pip3 install requests(Mac用户)的指令。
如果内置模块是用Python语言编写的话，就能找到py文件：我们用命令random.__file__找出了random模块的文件路径，就可以去打开查看它的代码：
如何自学模块:学习模块的核心是搞清楚模块的功能，也就是模块中的函数和类方法有什么作用，以及具体使用案例长什么样。
用自学“random”模块为例，如果英文好的同学，可以直接阅读官方文档：https://docs.python.org/3.6/library/random.html
或者也可以直接百度搜索：搜到教程后，我们重点关注的是模块中的函数和类方法有什么作用，然后把使用案例做成笔记.
例如random模块的关键知识（也就是比较有用的函数和类方法），可以做成这样的笔记：
import random  # 调用random模块
a = random.random()  # 随机从0-1之间（包括0不包括1）抽取一个小数
print(a)
#》》0.7262662200235862
a = random.randint(0,100)  # 随机从0-100（包括0和100）之间抽取一个数字
print(a)
#》》82
a = random.choice('abcdefg')  # 随机从字符串，列表等对象中抽取一个元素（可能会重复）
print(a)
#》》b
a = random.sample('abcdefg', 3) # 随机从字符串，列表等对象中抽取多个不重复的元素
print(a)
#》》['f', 'c', 'a']
items = [1, 2, 3, 4, 5, 6]  # “随机洗牌”，比如打乱列表
random.shuffle(items)
print(items)
#》》[1, 3, 6, 4, 5, 2]

使用dir()函数查看一个模块，看看它里面有什么变量、函数、类、类方法。
# 请直接运行并体验代码
import random  # 调用random模块
print(dir(random))
#这就像是查户口一样，可以把模块中的函数（函数和类方法）一览无余地暴露出来。对于查到的结果"__xx__"结构的(如__doc__)，它们是系统相关的函数，我们不用理会，直接看全英文的函数名即可。

import csv
with open('test.csv', newline = '', encoding = 'utf-8')  as f:
    reader=csv.reader(f)
    for row in reader:
        print(row)
    print("读取完毕！")
['\ufeff商品编号', '商品名称', '单价', '库存', '销量']
['1', '猫零食', '12', '3133', '5164']
['2', '普通猫粮', '33', '5055', '2231']
['3', '猫粮四合一', '187', '212', '334']
读取完毕！
用writerow()方法为它追加写入两行列表
mport csv
with open('test.csv','a', newline='',encoding='utf-8') as f:
    writer  = csv.writer(f)
    writer.writerow(['4', '猫砂', '25', '1022', '886'])
    writer.writerow(['5', '猫罐头', '18', '2234', '3121'])

```
## ::异常处理::   
```


通过编程处理选择的异常是可行的。看一下下面的例子：它会一直要求用户输入，直到输入一个合法的整数为止，但允许用户中断这个程序（使用 `Control-C` 或系统支持的任何方法）。注意：用户产生的中断会引发一个 [KeyboardInterrupt](https://docs.python.org/3/library/exceptions.html#KeyboardInterrupt) 异常。

> > while True:
...     try:
...         x = int(input("Please enter a number: "))
...         break
...     except ValueError:
...         print("Oops!  That was no valid number.  Try again...")
... [try](https://docs.python.org/3/reference/compound_stmts.html#try) 语句按如下方式工作。

- 首先，执行 *try* 子句 （在 [try](https://docs.python.org/3/reference/compound_stmts.html#try) 和 [except](https://docs.python.org/3/reference/compound_stmts.html#except) 关键字之间的部分）。
- 如果没有异常发生， *except* 子句 在 [try](https://docs.python.org/3/reference/compound_stmts.html#try) 语句执行完毕后就被忽略了。
- 如果在 try 子句执行过程中发生了异常，那么该子句其余的部分就会被忽略。

   如果异常匹配于 [except](https://docs.python.org/3/reference/compound_stmts.html#except) 关键字后面指定的异常类型，就执行对应的except子句。然后继续执行 [try](https://docs.python.org/3/reference/compound_stmts.html#try) 语句之后的代码。

- 如果发生了一个异常，在 [except](https://docs.python.org/3/reference/compound_stmts.html#except) 子句中没有与之匹配的分支，它就会传递到上一级 [try](https://docs.python.org/3/reference/compound_stmts.html#try) 语句中。

   如果最终仍找不到对应的处理语句，它就成为一个 *未处理异常*，终止程序运行，显示提示信息。

一个 [try](https://docs.python.org/3/reference/compound_stmts.html#try) 语句可能包含多个 except 子句，分别指定处理不同的异常。至多只会有一个分支被执行。异常处理程序只会处理对应的 try 子句中发生的异常，在同一个 [try](https://docs.python.org/3/reference/compound_stmts.html#try) 语句中，其他子句中发生的异常则不作处理。一个 except 子句可以在括号中列出多个异常的名字，例如:

... except (RuntimeError, TypeError, NameError):

...     pass

最后一个 except 子句可以省略异常名称，以作为通配符使用。你需要慎用此法，因为它会轻易隐藏一个实际的程序错误！可以使用这种方法打印一条错误信息，然后重新抛出异常（允许调用者处理这个异常):

import sys

try:
f = open('myfile.txt')
s = f.readline()
i = int(s.strip())

except OSError as err:
print("OS error: {0}".format(err))

except ValueError:
print("Could not convert data to an integer.")

except:
print("Unexpected error:", sys.exc_info()[0])
raise

[try](https://docs.python.org/3/reference/compound_stmts.html#try) … [except](https://docs.python.org/3/reference/compound_stmts.html#except) 语句可以带有一个 *else子句*，该子句只能出现在所有 except 子句之后。当 try 语句没有抛出异常时，需要执行一些代码，可以使用这个子句。例如:

for arg in sys.argv[1:]:
try:
f = open(arg, 'r')
except IOError:
print('cannot open', arg)
else:
print(arg, 'has', len(f.readlines()), 'lines')
f.close()

使用 [else](https://docs.python.org/3/reference/compound_stmts.html#else) 子句比在 [try](https://docs.python.org/3/reference/compound_stmts.html#try) 子句中附加代码要好，因为这样可以避免 [try](https://docs.python.org/3/reference/compound_stmts.html#try) … [except](https://docs.python.org/3/reference/compound_stmts.html#except) 意外的截获本来不属于它们保护的那些代码抛出的异常。

发生异常时，可能会有一个附属值，作为异常的 *参数* 存在。这个参数是否存在、是什么类型，依赖于异常的类型。

在异常名（列表）之后，也可以为 except 子句指定一个变量。这个变量绑定于一个异常实例，它存储在 `instance.args` 的参数中。为了方便起见，异常实例定义了 [**str**()](https://docs.python.org/3/reference/datamodel.html#object.__str__) ，这样就可以直接访问过打印参数而不必引用 `.args`。这种做法不受鼓励。相反，更好的做法是给异常传递一个参数（如果要传递多个参数，可以传递一个元组），把它绑定到 message 属性。一旦异常发生，它会在抛出前绑定所有指定的属性。

> > try:
...    raise Exception('spam', 'eggs')
... except Exception as inst:
...    print(type(inst))    # the exception instance
...    print(inst.args)     # arguments stored in .args
...    print(inst)          # **str** allows args to be printed directly,
...                         # but may be overridden in exception subclasses
...    x, y = inst.args     # unpack args
...    print('x =', x)
...    print('y =', y)
...
<class 'Exception'>
('spam', 'eggs')
('spam', 'eggs')
x = spam
y = eggs
对于那些未处理的异常，如果一个它们带有参数，那么就会被作为异常信息的最后部分（“详情”）打印出来。
异常处理器不仅仅处理那些在 try 子句中立刻发生的异常，也会处理那些 try 子句中调用的函数内部发生的异常。例如:

> > def this_fails():
...     x = 1/0
...

> > try:
...     this_fails()
... except ZeroDivisionError as err:
...     print('Handling run-time error:', err)
...
Handling run-time error: int division or modulo by zero

## 13.1 抛出异常

[raise](https://docs.python.org/3/reference/simple_stmts.html#raise) 语句允许程序员强制抛出一个指定的异常。例如:

raise NameError('HiThere') Traceback (most recent call last): File "", line 1, in ? NameError: HiThere 要抛出的异常由 [raise](https://docs.python.org/3/reference/simple_stmts.html#raise) 的唯一参数标识。它必需是一个异常实例或异常类（继承自 [Exception](https://docs.python.org/3/library/exceptions.html#Exception) 的类）。 如果你需要明确一个异常是否抛出，但不想处理它，[raise](https://docs.python.org/3/reference/simple_stmts.html#raise) 语句可以让你很简单的重新抛出该异常:

try: ... raise NameError('HiThere') ... except NameError: ... print('An exception flew by!') ... raise ... An exception flew by! Traceback (most recent call last): File "", line 2, in ? NameError: HiThere

## 13.2用户自定义异常

在程序中可以通过创建新的异常类型来命名自己的异常（Python 类的内容请参见 [类](http://www.pythondoc.com/pythontutorial3/classes.html#tut-classes) ）。异常类通常应该直接或间接的从 [Exception](https://docs.python.org/3/library/exceptions.html#Exception) 类派生，例如:

> > class MyError(Exception):
...     def **init**(self, value):
...         self.value = value
...     def **str**(self):
...         return repr(self.value)
...

> > try:
...     raise MyError(2*2)
... except MyError as e:
...     print('My exception occurred, value:', e.value)
...
My exception occurred, value: 4

raise MyError('oops!') Traceback (most recent call last): File "", line 1, in ? **main**.MyError: 'oops!' 在这个例子中，[Exception](https://docs.python.org/3/library/exceptions.html#Exception) 默认的 [**init**()](https://docs.python.org/3/reference/datamodel.html#object.__init__) 被覆盖。新的方式简单的创建 *value* 属性。这就替换了原来创建 *args* 属性的方式。 异常类中可以定义任何其它类中可以定义的东西，但是通常为了保持简单，只在其中加入几个属性信息，以供异常处理句柄提取。如果一个新创建的模块中需要抛出几种不同的错误时，一个通常的作法是为该模块定义一个异常基类，然后针对不同的错误类型派生出对应的异常子类: class Error(Exception): """Base class for exceptions in this module.""" pass class InputError(Error): """Exception raised for errors in the input. Attributes: expression–input expression in which the error occurred message -- explanation of the error """ def **init**(self, expression, message): self.expression = expression self.message = message class TransitionError(Error): """Raised when an operation attempts a state transition that's not allowed. Attributes: previous–state at beginning of transition next -- attempted new state message -- explanation of why the specific transition is not allowed """ def **init**(self, previous, next, message): self.previous = previous self.next = next self.message = message 与标准异常相似，大多数异常的命名都以 “Error” 结尾。 很多标准模块中都定义了自己的异常，用以报告在他们所定义的函数中可能发生的错误。关于类的进一步信息请参见 [类](http://www.pythondoc.com/pythontutorial3/classes.html#tut-classes) 一章。

## 13.4定义清理行为

[try](https://docs.python.org/3/reference/compound_stmts.html#try) 语句还有另一个可选的子句，目的在于定义在任何情况下都一定要执行的功能。例如:

try: ... raise KeyboardInterrupt ... finally: ... print('Goodbye, world!') ... Goodbye, world! KeyboardInterrupt Traceback (most recent call last): File "", line 2, in ? 不管有没有发生异常，*finally子句* 在程序离开 [try](https://docs.python.org/3/reference/compound_stmts.html#try) 后都一定会被执行。当 [try](https://docs.python.org/3/reference/compound_stmts.html#try) 语句中发生了未被 [except](https://docs.python.org/3/reference/compound_stmts.html#except) 捕获的异常（或者它发生在 [except](https://docs.python.org/3/reference/compound_stmts.html#except) 或 [else](https://docs.python.org/3/reference/compound_stmts.html#else) 子句中），在 [finally](https://docs.python.org/3/reference/compound_stmts.html#finally) 子句执行完后它会被重新抛出。 [try](https://docs.python.org/3/reference/compound_stmts.html#try) 语句经由 [break](https://docs.python.org/3/reference/simple_stmts.html#break) ，[continue](https://docs.python.org/3/reference/simple_stmts.html#continue) 或 [return](https://docs.python.org/3/reference/simple_stmts.html#return) 语句退 出也一样会执行 [finally](https://docs.python.org/3/reference/compound_stmts.html#finally) 子句。以下是一个更复杂些的例子:

> > def divide(x, y):
...     try:
...         result = x / y
...     except ZeroDivisionError:
...         print("division by zero!")
...     else:
...         print("result is", result)
...     finally:
...         print("executing finally clause")
...

> > divide(2, 1)
result is 2
executing finally clause

> > divide(2, 0)
division by zero!
executing finally clause

divide("2", "1") executing finally clause Traceback (most recent call last): File "", line 1, in ? File "", line 3, in divide TypeError: unsupported operand type(s) for /: 'str' and 'str' 如你所见， [finally](https://docs.python.org/3/reference/compound_stmts.html#finally) 子句在任何情况下都会执行。[TypeError](https://docs.python.org/3/library/exceptions.html#TypeError) 在两个字符串相除的时候抛出，未被 except 子句捕获，因此在 [finally](https://docs.python.org/3/reference/compound_stmts.html#finally) 子句执行完毕后重新抛出。 在真实场景的应用程序中，[finally](https://docs.python.org/3/reference/compound_stmts.html#finally) 子句用于释放外部资源（文件 或网络连接之类的），无论它们的使用过程中是否出错。

## 13.5预定义清理行为

有些对象定义了标准的清理行为，无论对象操作是否成功，不再需要该对象的时候就会起作用。以下示例尝试打开文件并把内容打印到屏幕上。

for line in open("myfile.txt"):
print(line)

这段代码的问题在于在代码执行完后没有立即关闭打开的文件。这在简单的脚本里没什么，但是大型应用程序就会出问题。[with](https://docs.python.org/3/reference/compound_stmts.html#with) 语句使得文件之类的对象可以 确保总能及时准确地进行清理。

with open("myfile.txt") as f:
for line in f:
print(line)

语句执行后，文件 *f* 总会被关闭，即使是在处理文件中的数据时出错也一样。其它对象是否提供了预定义的清理行为要查看它们的文档。




```
## 9.py类   
```

Python 的类机制通过最小的新语法和语义在语言中实现了类。它是 C++ 或者 Modula-3 语言中类机制的混合。就像模块一样，Python 的类并没有在用户和定义之间设立绝对的屏障，而是依赖于用户不去“强行闯入定义”的优雅。另一方面，类的大多数重要特性都被完整的保留下来：类继承机制允许多重继承，派生类可以覆盖（override）基类中的任何方法或类，可以使用相同的方法名称调用基类的方法。对象可以包含任意数量的私有数据。

用 C++ 术语来讲，所有的类成员（包括数据成员）都是公有（ *public* ）的（其它情况见下文 [私有变量](http://www.pythondoc.com/pythontutorial3/classes.html#tut-private)），所有的成员函数都是虚（ *virtual* ）的。用 Modula-3 的术语来讲，在成员方法中没有简便的方式引用对象的成员：方法函数在定义时需要以引用的对象做为第一个参数，调用时则会隐式引用对象。像在 Smalltalk 中一个，类也是对象。这就提供了导入和重命名语义。不像 C++ 和 Modula-3 中那样，大多数带有特殊语法的内置操作符（算法运算符、下标等）都可以针对类的需要重新定义。

在讨论类时，没有足够的得到共识的术语，我会偶尔从 Smalltalk 和 C++ 借用一些。我比较喜欢用 Modula-3 的用语，因为比起 C++，Python 的面向对象语法更像它，但是我想很少有读者听过这个。

## 9.1. 术语相关

对象具有特性，并且多个名称（在多个作用域中）可以绑定在同一个对象上。在其它语言中被称为别名。在对 Python 的第一印象中这通常会被忽略，并且当处理不可变基础类型（数字，字符串，元组）时可以被放心的忽略。但是，在调用列表、字典这类可变对象，或者大多数程序外部类型（文件，窗体等）描述实体时，别名对 Python 代码的语义便具有（有意而为）影响。这通常有助于程序的优化，因为在某些方面别名表现的就像是指针。例如，你可以轻易的传递一个对象，因为通过继承只是传递一个指针。并且如果一个方法修改了一个作为参数传递的对象，调用者可以接收这一变化——这消除了两种不同的参数传递机制的需要，像 Pascal 语言。

## 9.2. Python 作用域和命名空间

在介绍类之前，我首先介绍一些有关 Python 作用域的规则。类的定义非常巧妙的运用了命名空间，要完全理解接下来的知识，需要先理解作用域和命名空间的工作原理。另外，这一切的知识对于任何高级 Python 程序员都非常有用。

让我们从一些定义说起。

*命名空间* 是从命名到对象的映射。当前命名空间主要是通过 Python 字典实现的，不过通常不关心具体的实现方式（除非出于性能考虑），以后也有可能会改变其实现方式。以下有一些命名空间的例子：内置命名（像 [abs()](https://docs.python.org/3/library/functions.html#abs) 这样的函数，以及内置异常名）集，模块中的全局命名，函数调用中的局部命名。某种意义上讲对象的属性集也是一个命名空间。关于命名空间需要了解的一件很重要的事就是不同命名空间中的命名没有任何联系，例如两个不同的模块可能都会定义一个名为 `maximize` 的函数而不会发生混淆－用户必须以模块名为前缀来引用它们。

顺便提一句，我称 Python 中任何一个“.”之后的命名为 *属性* －－例如，表达式 `z.real` 中的 `real` 是对象 `z` 的一个属性。严格来讲，从模块中引用命名是引用属性：表达式 `modname.funcname` 中，`modname` 是一个模块对象，`funcname` 是它的一个属性。因此，模块的属性和模块中的全局命名有直接的映射关系：它们共享同一命名空间！[[1]](http://www.pythondoc.com/pythontutorial3/classes.html#id27)

属性可以是只读过或写的。后一种情况下，可以对属性赋值。你可以这样作： `modname.the_answer = 42` 。可写的属性也可以用 [del](https://docs.python.org/3/reference/simple_stmts.html#del) 语句删除。例如： `del modname.the_answer` 会从 `modname` 对象中删除 `the_answer` 属性。

不同的命名空间在不同的时刻创建，有不同的生存期。包含内置命名的命名空间在 Python 解释器启动时创建，会一直保留，不被删除。模块的全局命名空间在模块定义被读入时创建，通常，模块命名空间也会一直保存到解释器退出。由解释器在最高层调用执行的语句，不管它是从脚本文件中读入还是来自交互式输入，都是 [**main**](https://docs.python.org/3/library/__main__.html#module-__main__) 模块的一部分，所以它们也拥有自己的命名空间（内置命名也同样被包含在一个模块中，它被称作 [builtins](https://docs.python.org/3/library/builtins.html#module-builtins) ）。

当调用函数时，就会为它创建一个局部命名空间，并且在函数返回或抛出一个并没有在函数内部处理的异常时被删除。（实际上，用遗忘来形容到底发生了什么更为贴切。）当然，每个递归调用都有自己的局部命名空间。

*作用域* 就是一个 Python 程序可以直接访问命名空间的正文区域。这里的直接访问意思是一个对名称的错误引用会尝试在命名空间内查找。尽管作用域是静态定义，在使用时他们都是动态的。每次执行时，至少有三个命名空间可以直接访问的作用域嵌套在一起：

- 包含局部命名的使用域在最里面，首先被搜索；其次搜索的是中层的作用域，这里包含了同级的函数；

   最后搜索最外面的作用域，它包含内置命名。

- 首先搜索最内层的作用域，它包含局部命名任意函数包含的作用域，是内层嵌套作用域搜索起点，包含非局部，但是也非全局的命名
- 接下来的作用域包含当前模块的全局命名
- 最外层的作用域（最后搜索）是包含内置命名的命名空间

如果一个命名声明为全局的，那么对它的所有引用和赋值会直接搜索包含这个模块全局命名的作用域。如果要重新绑定最里层作用域之外的变量，可以使用 [nonlocal](https://docs.python.org/3/reference/simple_stmts.html#nonlocal) 语句；如果不声明为 nonlocal，这些变量将是只读的（对这样的变量赋值会在最里面的作用域创建一个新的局部变量，外部具有相同命名的那个变量不会改变）。

通常，局部作用域引用当前函数的命名。在函数之外，局部作用域与全局使用域引用同一命名空间：模块命名空间。类定义也是局部作用域中的另一个命名空间。

重要的是作用域决定于源程序的意义：一个定义于某模块中的函数的全局作用域是该模块的命名空间，而不是该函数的别名被定义或调用的位置，了解这一点非常重要。另一方面，命名的实际搜索过程是动态的，在运行时确定的——然而，Python 语言也在不断发展，以后有可能会成为静态的“编译”时确定，所以不要依赖动态解析！（事实上，局部变量已经是静态确定了。）

Python 的一个特别之处在于：如果没有使用 [global](https://docs.python.org/3/reference/simple_stmts.html#global) 语法，其赋值操作总是在最里层的作用域。赋值不会复制数据，只是将命名绑定到对象。删除也是如此：`del x` 只是从局部作用域的命名空间中删除命名 `x` 。事实上，所有引入新命名的操作都作用于局部作用域。特别是 [import](https://docs.python.org/3/reference/simple_stmts.html#import) 语句和函数定义将模块名或函数绑定于局部作用域（可以使用 [global](https://docs.python.org/3/reference/simple_stmts.html#global) 语句将变量引入到全局作用域）。

[global](https://docs.python.org/3/reference/simple_stmts.html#global) 语句用以指明某个特定的变量为全局作用域，并重新绑定它。[nonlocal](https://docs.python.org/3/reference/simple_stmts.html#nonlocal) 语句用以指明某个特定的变量为封闭作用域，并重新绑定它。

### 9.2.1. 作用域和命名空间示例

以下是一个示例，演示了如何引用不同作用域和命名空间，以及 [global](https://docs.python.org/3/reference/simple_stmts.html#global) 和 [nonlocal](https://docs.python.org/3/reference/simple_stmts.html#nonlocal) 如何影响变量绑定:

def scope_test():
def do_local():
spam = "local spam"
def do_nonlocal():
nonlocal spam
spam = "nonlocal spam"
def do_global():
global spam
spam = "global spam"
spam = "test spam"
do_local()
print("After local assignment:", spam)
do_nonlocal()
print("After nonlocal assignment:", spam)
do_global()
print("After global assignment:", spam)

scope_test()

print("In global scope:", spam)

以上示例代码的输出为:

After local assignment: test spam

After nonlocal assignment: nonlocal spam

After global assignment: nonlocal spam

In global scope: global spam

注意：*local* 赋值语句是无法改变 *scope_test* 的 *spam* 绑定。[nonlocal](https://docs.python.org/3/reference/simple_stmts.html#nonlocal) 赋值语句改变了 *scope_test* 的 *spam* 绑定，并且 [global](https://docs.python.org/3/reference/simple_stmts.html#global) 赋值语句从模块级改变了 spam 绑定。

你也可以看到在 [global](https://docs.python.org/3/reference/simple_stmts.html#global) 赋值语句之前对 *spam* 是没有预先绑定的。

## 9.3. 初识类

类引入了一些新语法：三种新的对象类型和一些新的语义。

### 9.3.1. 类定义语法

类定义最简单的形式如下:

class ClassName: . . .

类的定义就像函数定义（ [def](https://docs.python.org/3/reference/compound_stmts.html#def) 语句），要先执行才能生效。（你当然可以把它放进 [if](https://docs.python.org/3/reference/compound_stmts.html#if) 语句的某一分支，或者一个函数的内部。）

习惯上，类定义语句的内容通常是函数定义，不过其它语句也可以，有时会很有用，后面我们再回过头来讨论。类中的函数定义通常包括了一个特殊形式的参数列表，用于方法调用约定——同样我们在后面讨论这些。

进入类定义部分后，会创建出一个新的命名空间，作为局部作用域。因此，所有的赋值成为这个新命名空间的局部变量。特别是函数定义在此绑定了新的命名。

类定义完成时（正常退出），就创建了一个 *类对象*。基本上它是对类定义创建的命名空间进行了一个包装；我们在下一节进一步学习类对象的知识。原始的局部作用域（类定义引入之前生效的那个）得到恢复，类对象在这里绑定到类定义头部的类名（例子中是 `ClassName` ）。

### 9.3.2. 类对象

类对象支持两种操作：属性引用和实例化。

*属性引用* 使用和 Python 中所有的属性引用一样的标准语法：`obj.name`。类对象创建后，类命名空间中所有的命名都是有效属性名。所以如果类定义是这样:

class MyClass:
"""A simple example class"""
i = 12345
def f(self):
return 'hello world'

那么 `MyClass.i` 和 `MyClass.f` 是有效的属性引用，分别返回一个整数和一个方法对象。也可以对类属性赋值，你可以通过给 `MyClass.i` 赋值来修改它。 `__doc__` 也是一个有效的属性，返回类的文档字符串：`"A simple example class"`。

类的 *实例化* 使用函数符号。只要将类对象看作是一个返回新的类实例的无参数函数即可。例如（假设沿用前面的类）:

x = MyClass()

以上创建了一个新的类 *实例* 并将该对象赋给局部变量 `x`。

这个实例化操作（“调用”一个类对象）来创建一个空的对象。很多类都倾向于将对象创建为有初始状态的。因此类可能会定义一个名为 `__init__()` 的特殊方法，像下面这样:

def **init**(self):
self.data = []

类定义了 `__init__()` 方法的话，类的实例化操作会自动为新创建的类实例调用 `__init__()` 方法。所以在下例中，可以这样创建一个新的实例:

x = MyClass()

当然，出于弹性的需要，`__init__()` 方法可以有参数。事实上，参数通过 `__init__()` 传递到类的实例化操作上。例如，

> > class Complex:
...     def **init**(self, realpart, imagpart):
...         self.r = realpart
...         self.i = imagpart
...

> > x = Complex(3.0, -4.5)

> > x.r, x.i
(3.0, -4.5)

### 9.3.3. 实例对象

现在我们可以用实例对象作什么？实例对象唯一可用的操作就是属性引用。有两种有效的属性名。

*数据属性* 相当于 Smalltalk 中的“实例变量”或 C++ 中的“数据成员”。和局部变量一样，数据属性不需要声明，第一次使用时它们就会生成。例如，如果 `x` 是前面创建的 `MyClass` 实例，下面这段代码会打印出 16 而在堆栈中留下多余的东西:

x.counter = 1

while x.counter < 10:
x.counter = x.counter * 2

print(x.counter)

del x.counter

另一种为实例对象所接受的引用属性是 *方法*。方法是“属于”一个对象的函数。（在 Python 中，方法不止是类实例所独有：其它类型的对象也可有方法。例如，链表对象有 append，insert，remove，sort 等等方法。然而，在后面的介绍中，除非特别说明，我们提到的方法特指类方法）

实例对象的有效名称依赖于它的类。按照定义，类中所有（用户定义）的函数对象对应它的实例中的方法。所以在我们的例子中，`x.f` 是一个有效的方法引用，因为 `MyClass.f` 是一个函数。但 `x.i` 不是，因为 `MyClass.i` 不是函数。不过 `x.f` 和 `MyClass.f` 不同，它是一个 *方法对象* ，不是一个函数对象。

### 9.3.4. 方法对象

通常，方法通过右绑定方式调用:

x.f()

在 `MyClass` 示例中，这会返回字符串 `'hello world'`。然而，也不是一定要直接调用方法。 `x.f` 是一个方法对象，它可以存储起来以后调用。例如:

xf = x.f

while True:
print(xf())

会不断的打印 `hello world`。

调用方法时发生了什么？你可能注意到调用 `x.f()` 时没有引用前面标出的变量，尽管在 `f()` 的函数定义中指明了一个参数。这个参数怎么了？事实上如果函数调用中缺少参数，Python 会抛出异常－－甚至这个参数实际上没什么用……

实际上，你可能已经猜到了答案：方法的特别之处在于实例对象作为函数的第一个参数传给了函数。在我们的例子中，调用 `x.f()` 相当于 `MyClass.f(x)` 。通常，以 *n* 个参数的列表去调用一个方法就相当于将方法的对象插入到参数列表的最前面后，以这个列表去调用相应的函数。

如果你还是不理解方法的工作原理，了解一下它的实现也许有帮助。引用非数据属性的实例属性时，会搜索它的类。如果这个命名确认为一个有效的函数对象类属性，就会将实例对象和函数对象封装进一个抽象对象：这就是方法对象。以一个参数列表调用方法对象时，它被重新拆封，用实例对象和原始的参数列表构造一个新的参数列表，然后函数对象调用这个新的参数列表。

### 9.3.5. 类和实例变量

一般来说，实例变量用于对每一个实例都是唯一的数据，类变量用于类的所有实例共享的属性和方法:

class Dog:
kind = 'canine'         # class variable shared by all instances
def **init**(self, name): [self.name](http://self.name) = name    # instance variable unique to each instance

> > d = Dog('Fido')

> > e = Dog('Buddy')

> > d.kind                  # shared by all dogs
'canine'

> > e.kind                  # shared by all dogs
'canine'

> > [d.name](http://d.name)                  # unique to d
'Fido'

> > [e.name](http://e.name)                  # unique to e
'Buddy'
正如在 [术语相关](http://www.pythondoc.com/pythontutorial3/classes.html#tut-object) 讨论的， [可变](https://docs.python.org/3/glossary.html#term-mutable) 对象，例如列表和字典，的共享数据可能带来意外的效果。例如，下面代码中的 *tricks* 列表不应该用作类变量，因为所有的 *Dog* 实例将共享同一个列表:
class Dog:
tricks = []             # mistaken use of a class variable
def **init**(self, name): [self.name](http://self.name) = name
def add_trick(self, trick):
self.tricks.append(trick)

> > d = Dog('Fido')

> > e = Dog('Buddy')

> > d.add_trick('roll over')

> > e.add_trick('play dead')

> > d.tricks                # unexpectedly shared by all dogs
['roll over', 'play dead']
这个类的正确设计应该使用一个实例变量:
class Dog:
def **init**(self, name): [self.name](http://self.name) = name
self.tricks = []    # creates a new empty list for each dog
def add_trick(self, trick):
self.tricks.append(trick)

> > d = Dog('Fido')

> > e = Dog('Buddy')

> > d.add_trick('roll over')

> > e.add_trick('play dead')

> > d.tricks
['roll over']

> > e.tricks
['play dead']

## 9.4. 一些说明

数据属性会覆盖同名的方法属性。为了避免意外的名称冲突，这在大型程序中是极难发现的 Bug，使用一些约定来减少冲突的机会是明智的。可能的约定包括：大写方法名称的首字母，使用一个唯一的小字符串（也许只是一个下划线）作为数据属性名称的前缀，或者方法使用动词而数据属性使用名词。

数据属性可以被方法引用，也可以由一个对象的普通用户（客户）使用。换句话说，类不能用来实现纯净的数据类型。事实上，Python 中不可能强制隐藏数据——一切基于约定（如果需要，使用 C 编写的 Python 实现可以完全隐藏实现细节并控制对象的访问。这可以用来通过 C 语言扩展 Python）。

客户应该谨慎的使用数据属性——客户可能通过践踏他们的数据属性而使那些由方法维护的常量变得混乱。注意：只要能避免冲突，客户可以向一个实例对象添加他们自己的数据属性，而不会影响方法的正确性——再次强调，命名约定可以避免很多麻烦。

从方法内部引用数据属性（或其他方法）并没有快捷方式。我觉得这实际上增加了方法的可读性：当浏览一个方法时，在局部变量和实例变量之间不会出现令人费解的情况。

一般，方法的第一个参数被命名为 `self`。这仅仅是一个约定：对 Python 而言，名称 `self` 绝对没有任何特殊含义。（但是请注意：如果不遵循这个约定，对其他的 Python 程序员而言你的代码可读性就会变差，而且有些 *类查看器* 程序也可能是遵循此约定编写的。）

类属性的任何函数对象都为那个类的实例定义了一个方法。函数定义代码不一定非得定义在类中：也可以将一个函数对象赋值给类中的一个局部变量。例如:

# Function defined outside the class

def f1(self, x, y):
return min(x, x+y)

class C:
f = f1
def g(self):
return 'hello world'
h = g

现在 `f`， `g` 和 `h` 都是类 `C` 的属性，引用的都是函数对象，因此它们都是 `C` 实例的方法－－ `h` 严格等于 `g` 。要注意的是这种习惯通常只会迷惑程序的读者。

通过 `self` 参数的方法属性，方法可以调用其它的方法:

class Bag:
def **init**(self):
self.data = []
def add(self, x):
self.data.append(x)
def addtwice(self, x):
self.add(x)
self.add(x)

方法可以像引用普通的函数那样引用全局命名。与方法关联的全局作用域是包含类定义的模块。（类本身永远不会做为全局作用域使用。）尽管很少有好的理由在方法 中使用全局数据，全局作用域确有很多合法的用途：其一是方法可以调用导入全局作用域的函数和方法，也可以调用定义在其中的类和函数。通常，包含此方法的类也会定义在这个全局作用域，在下一节我们会了解为何一个方法要引用自己的类。

每个值都是一个对象，因此每个值都有一个 类( *class* ) （也称为它的 类型( *type* ) ），它存储为 `object.__class__` 。

## 9.5. 继承

当然，如果一种语言不支持继承就，“类”就没有什么意义。派生类的定义如下所示:

class DerivedClassName(BaseClassName): . . .

命名 `BaseClassName` （示例中的基类名）必须与派生类定义在一个作用域内。除了类，还可以用表达式，基类定义在另一个模块中时这一点非常有用:

class DerivedClassName(modname.BaseClassName):

派生类定义的执行过程和基类是一样的。构造派生类对象时，就记住了基类。这在解析属性引用的时候尤其有用：如果在类中找不到请求调用的属性，就搜索基类。如果基类是由别的类派生而来，这个规则会递归的应用上去。

派生类的实例化没有什么特殊之处： `DerivedClassName()` （示列中的派生类）创建一个新的类实例。方法引用按如下规则解析：搜索对应的类属性，必要时沿基类链逐级搜索，如果找到了函数对象这个方法引用就是合法的。

派生类可能会覆盖其基类的方法。因为方法调用同一个对象中的其它方法时没有特权，基类的方法调用同一个基类的方法时，可能实际上最终调用了派生类中的覆盖方法。（对于 C++ 程序员来说，Python 中的所有方法本质上都是 `虚` 方法。）

派生类中的覆盖方法可能是想要扩充而不是简单的替代基类中的重名方法。有一个简单的方法可以直接调用基类方法，只要调用： `BaseClassName.methodname(self, arguments)`。有时这对于客户也很有用。（要注意只有 `BaseClassName` 在同一全局作用域定义或导入时才能这样用。）

Python 有两个用于继承的函数：

- 函数 [isinstance()](https://docs.python.org/3/library/functions.html#isinstance) 用于检查实例类型： `isinstance(obj, int)` 只有在 `obj.__class__` 是 [int](https://docs.python.org/3/library/functions.html#int) 或其它从 [int](https://docs.python.org/3/library/functions.html#int) 继承的类型
- 函数 [issubclass()](https://docs.python.org/3/library/functions.html#issubclass) 用于检查类继承： `issubclass(bool, int)` 为 `True`，因为 [bool](https://docs.python.org/3/library/functions.html#bool) 是 [int](https://docs.python.org/3/library/functions.html#int) 的子类。

   然而， `issubclass(float, int)` 为 `False`，因为 [float](https://docs.python.org/3/library/functions.html#float) 不是 [int](https://docs.python.org/3/library/functions.html#int) 的子类。

### 9.5.1. 多继承

Python 同样有限的支持多继承形式。多继承的类定义形如下例:

class DerivedClassName(Base1, Base2, Base3): . . .

在大多数情况下，在最简单的情况下，你能想到的搜索属性从父类继承的深度优先，左到右，而不是搜索两次在同一个类层次结构中，其中有一个重叠。因此，如果在 `DerivedClassName` （示例中的派生类）中没有找到某个属性，就会搜索 `Base1`，然后（递归的）搜索其基类，如果最终没有找到，就搜索 `Base2`，以此类推。

实际上，[super()](https://docs.python.org/3/library/functions.html#super) 可以动态的改变解析顺序。这个方式可见于其它的一些多继承语言，类似 call-next-method，比单继承语言中的 super 更强大 。

动态调整顺序十分必要的，因为所有的多继承会有一到多个菱形关系（指有至少一个祖先类可以从子类经由多个继承路径到达）。例如，所有的 new-style 类继承自 [object](https://docs.python.org/3/library/functions.html#object) ，所以任意的多继承总是会有多于一条继承路径到达 [object](https://docs.python.org/3/library/functions.html#object) 。

为了防止重复访问基类，通过动态的线性化算法，每个类都按从左到右的顺序特别指定了顺序，每个祖先类只调用一次，这是单调的（意味着一个类被继承时不会影响它祖先的次序）。总算可以通过这种方式使得设计一个可靠并且可扩展的多继承类成为可能。进一步的内容请参见 [http://www.python.org/download/releases/2.3/mro/](http://www.python.org/download/releases/2.3/mro/) 。

## 9.6. 私有变量

只能从对像内部访问的“私有”实例变量，在 Python 中不存在。然而，也有一个变通的访问用于大多数 Python 代码：以一个下划线开头的命名（例如 `_spam` ）会被处理为 API 的非公开部分（无论它是一个函数、方法或数据成员）。它会被视为一个实现细节，无需公开。

因为有一个正当的类私有成员用途（即避免子类里定义的命名与之冲突），Python 提供了对这种结构的有限支持，称为 *name mangling* （命名编码） 。任何形如 `__spam` 的标识（前面至少两个下划线，后面至多一个），被替代为 `_classname__spam` ，去掉前导下划线的 `classname` 即当前的类名。此语法不关注标识的位置，只要求在类定义内。

名称重整是有助于子类重写方法，而不会打破组内的方法调用。例如:

class Mapping:
def **init**(self, iterable):
self.items_list = []
self.__update(iterable)
def update(self, iterable):
for item in iterable:
self.items_list.append(item)
__update = update   # private copy of original update() method

class MappingSubclass(Mapping):
def update(self, keys, values):
# provides new signature for update()
# but does not break **init**()
for item in zip(keys, values):
self.items_list.append(item)

需要注意的是编码规则设计为尽可能的避免冲突，被认作为私有的变量仍然有可能被访问或修改。在特定的场合它也是有用的，比如调试的时候。

要注意的是代码传入 `exec()`， `eval()` 时不考虑所调用的类的类名，视其为当前类，这类似于 `global` 语句的效应，已经按字节编译的部分也有同样的限制。这也同样作用于 `getattr()`， `setattr()` 和 `delattr()`，像直接引用 `__dict__` 一样。

## 9.7. 补充

有时类似于 Pascal 中“记录（record）”或 C 中“结构（struct）”的数据类型很有用，它将一组已命名的数据项绑定在一起。一个空的类定义可以很好的实现它:

class Employee:
pass

john = Employee() # Create an empty employee record

# Fill the fields of the record

[john.name](http://john.name) = 'John Doe'

john.dept = 'computer lab'

john.salary = 1000

某一段 Python 代码需要一个特殊的抽象数据结构的话，通常可以传入一个类，事实上这模仿了该类的方法。例如，如果你有一个用于从文件对象中格式化数据的函数，你可以定义一个带有 `read()` 和 `readline()` 方法的类，以此从字符串缓冲读取数据，然后将该类的对象作为参数传入前述的函数。

实例方法对象也有属性：`m.__self__` 是一个实例方法所属的对象，而 `m.__func__` 是这个方法对应的函数对象。

## 9.8. 异常也是类

用户自定义异常也可以是类。利用这个机制可以创建可扩展的异常体系。

以下是两种新的，有效的（语义上的）异常抛出形式，使用 [raise](https://docs.python.org/3/reference/simple_stmts.html#raise) 语句:

raise Class

raise Instance

第一种形式中，`Class` 必须是 [type](https://docs.python.org/3/library/functions.html#type) 或其派生类的一个实例。第二种形式是以下形式的简写:

raise Class()

发生的异常其类型如果是 [except](https://docs.python.org/3/reference/compound_stmts.html#except) 子句中列出的类，或者是其派生类，那么它们就是相符的（反过来说－－发生的异常其类型如果是异常子句中列出的类的基类，它们就不相符）。例如，以下代码会按顺序打印 B，C，D:

class B(Exception):
pass

class C(B):
pass

class D(C):
pass

for cls in [B, C, D]:
try:
raise cls()
except D:
print("D")
except C:
print("C")
except B:
print("B")

要注意的是如果异常子句的顺序颠倒过来（ `execpt B` 在最前），它就会打印 B，B，B－－第一个匹配的异常被触发。

打印一个异常类的错误信息时，先打印类名，然后是一个空格、一个冒号，然后是用内置函数 [str()](https://docs.python.org/3/library/stdtypes.html#str) 将类转换得到的完整字符串。

## 9.9. 迭代器

现在你可能注意到大多数容器对象都可以用 [for](https://docs.python.org/3/reference/compound_stmts.html#for) 遍历:

for element in [1, 2, 3]:
print(element)

for element in (1, 2, 3):
print(element)

for key in {'one':1, 'two':2}:
print(key)

for char in "123":
print(char)

for line in open("myfile.txt"):
print(line, end='')

这种形式的访问清晰、简洁、方便。迭代器的用法在 Python 中普遍而且统一。在后台， [for](https://docs.python.org/3/reference/compound_stmts.html#for) 语句在容器对象中调用 [iter()](https://docs.python.org/3/library/functions.html#iter) 。该函数返回一个定义了 [**next**()](https://docs.python.org/3/library/stdtypes.html#iterator.__next__) 方法的迭代器对象，它在容器中逐一访问元素。没有后续的元素时， [**next**()](https://docs.python.org/3/library/stdtypes.html#iterator.__next__) 抛出一个 [StopIteration](https://docs.python.org/3/library/exceptions.html#StopIteration) 异常通知 [for](https://docs.python.org/3/reference/compound_stmts.html#for) 语句循环结束。你可以是用内建的 [next()](https://docs.python.org/3/library/functions.html#next) 函数调用 [**next**()](https://docs.python.org/3/library/stdtypes.html#iterator.__next__) 方法；以下是其工作原理的示例:

> > s = 'abc'

> > it = iter(s)

> > it
<iterator object at 0x00A1DB50>

> > next(it)
'a'

> > next(it)
'b'

> > next(it)
'c'

next(it) Traceback (most recent call last): File "", line 1, in ? next(it) StopIteration 了解了迭代器协议的后台机制，就可以很容易的给自己的类添加迭代器行为。定义一个 [**iter**()](https://docs.python.org/3/reference/datamodel.html#object.__iter__) 方法，使其返回一个带有 [**next**()](https://docs.python.org/3/library/stdtypes.html#iterator.__next__) 方法的对象。如果这个类已经定义了 [**next**()](https://docs.python.org/3/library/stdtypes.html#iterator.__next__) ，那么 [**iter**()](https://docs.python.org/3/reference/datamodel.html#object.__iter__) 只需要返回 `self`: class Reverse: """Iterator for looping over a sequence backwards.""" def **init**(self, data): self.data = data self.index = len(data) def **iter**(self): return self def **next**(self): if self.index == 0: raise StopIteration self.index = self.index - 1 return self.data[self.index]

> > rev = Reverse('spam')

> > iter(rev)
<**main**.Reverse object at 0x00A1DB50>

> > for char in rev:
...     print(char)
...
m
a
p
s

## 9.10. 生成器

[Generator](https://docs.python.org/3/glossary.html#term-generator) 是创建迭代器的简单而强大的工具。它们写起来就像是正规的函数，需要返回数据的时候使用 [yield](https://docs.python.org/3/reference/simple_stmts.html#yield) 语句。每次 [next()](https://docs.python.org/3/library/functions.html#next) 被调用时，生成器回复它脱离的位置（它记忆语句最后一次执行的位置和所有的数据值）。以下示例演示了生成器可以很简单的创建出来:

def reverse(data):
for index in range(len(data)-1, -1, -1):
yield data[index]

> > for char in reverse('golf'):
...     print(char)
...
f
l
o
g
前一节中描述了基于类的迭代器，它能作的每一件事生成器也能作到。因为自动创建了 [**iter**()](https://docs.python.org/3/reference/datamodel.html#object.__iter__) 和 [**next**()](https://docs.python.org/3/reference/expressions.html#generator.__next__) 方法，生成器显得如此简洁。
另一个关键的功能在于两次执行之间，局部变量和执行状态都自动的保存下来。这使函数很容易写，而且比使用 `self.index` 和 `self.data` 之类的方式更清晰。
除了创建和保存程序状态的自动方法，当发生器终结时，还会自动抛出 [StopIteration](https://docs.python.org/3/library/exceptions.html#StopIteration) 异常。综上所述，这些功能使得编写一个正规函数成为创建迭代器的最简单方法。

## 9.11. 生成器表达式

有时简单的生成器可以用简洁的方式调用，就像不带中括号的链表推导式。这些表达式是为函数调用生成器而设计的。生成器表达式比完整的生成器定义更简洁，但是没有那么多变，而且通常比等价的链表推导式更容易记。

例如:

> > sum(i*i for i in range(10))                 # sum of squares
285

> > xvec = [10, 20, 30]

> > yvec = [7, 5, 3]

> > sum(x*y for x,y in zip(xvec, yvec))         # dot product
260

> > from math import pi, sin

> > sine_table = {x: sin(x*pi/180) for x in range(0, 91)}

> > unique_words = set(word  for line in page  for word in line.split())

> > valedictorian = max((student.gpa, [student.name](http://student.name)) for student in graduates)

> > data = 'golf'

> > list(data[i] for i in range(len(data)-1, -1, -1))
['f', 'l', 'o', 'g']

          


```
## 10. Python 标准库概览库概览   
```
            

## 10.1. 操作系统接口

[os](https://docs.python.org/3/library/os.html#module-os) 模块提供了很多与操作系统交互的函数:

> > import os

> > os.getcwd()      # Return the current working directory
'C:\Python35'

> > os.chdir('/server/accesslogs')   # Change current working directory

> > os.system('mkdir today')   # Run the command mkdir in the system shell
0
应该用 `import os` 风格而非 `from os import *`。这样可以保证随操作系统不同而有所变化的 [os.open()](https://docs.python.org/3/library/os.html#os.open) 不会覆盖内置函数 [open()](https://docs.python.org/3/library/functions.html#open)。
在使用一些像 [os](https://docs.python.org/3/library/os.html#module-os) 这样的大型模块时内置的 [dir()](https://docs.python.org/3/library/functions.html#dir) 和 [help()](https://docs.python.org/3/library/functions.html#help) 函数非常有用:

> > import os

dir(os)

> > help(os)
<returns an extensive manual page created from the module's docstrings>
针对日常的文件和目录管理任务，[shutil](https://docs.python.org/3/library/shutil.html#module-shutil) 模块提供了一个易于使用的高级接口:

> > import shutil

> > shutil.copyfile('data.db', 'archive.db')
'archive.db'

> > shutil.move('/build/executables', 'installdir')
'installdir'

## 10.2. 文件通配符

[glob](https://docs.python.org/3/library/glob.html#module-glob) 模块提供了一个函数用于从目录通配符搜索中生成文件列表:

> > import glob

> > glob.glob('*.py')
['[primes.py](http://primes.py)', '[random.py](http://random.py)', '[quote.py](http://quote.py)']

## 10.3. 命令行参数

通用工具脚本经常调用命令行参数。这些命令行参数以链表形式存储于 [sys](https://docs.python.org/3/library/sys.html#module-sys) 模块的 *argv* 变量。例如在命令行中执行 `python demo.py one two three` 后可以得到以下输出结果:

> > import sys

> > print(sys.argv)
['[demo.py](http://demo.py)', 'one', 'two', 'three'] [getopt](https://docs.python.org/3/library/getopt.html#module-getopt) 模块使用 Unix [getopt()](https://docs.python.org/3/library/getopt.html#module-getopt) 函数处理 *sys.argv*。更多的复杂命令行处理由 [argparse](https://docs.python.org/3/library/argparse.html#module-argparse) 模块提供。

## 10.4. 错误输出重定向和程序终止

[sys](https://docs.python.org/3/library/sys.html#module-sys) 还有 *stdin*， *stdout* 和 *stderr* 属性，即使在 *stdout* 被重定向时，后者也可以用于显示警告和错误信息:

> > sys.stderr.write('Warning, log file not found starting a new one\n')
Warning, log file not found starting a new one
大多脚本的直接终止都使用 `sys.exit()`。



```
## 10.5. 字符串正则匹配   
```

[re](https://docs.python.org/3/library/re.html#module-re) 模块为高级字符串处理提供了正则表达式工具。对于复杂的匹配和处理，正则表达式提供了简洁、优化的解决方案:

> > import re

> > re.findall(r'\bf[a-z]*', 'which foot or hand fell fastest')
['foot', 'fell', 'fastest']

> > re.sub(r'(\b[a-z]+) \1', r'\1', 'cat in the the hat')
'cat in the hat'
只需简单的操作时，字符串方法最好用，因为它们易读，又容易调试:

> > 'tea for too'.replace('too', 'two')
'tea for two'

## 10.6. 数学

[math](https://docs.python.org/3/library/math.html#module-math) 模块为浮点运算提供了对底层C函数库的访问:

> > import math

> > math.cos(math.pi / 4.0)
0.70710678118654757

> > math.log(1024, 2)
10.0 [random](https://docs.python.org/3/library/random.html#module-random) 提供了生成随机数的工具:

> > import random

> > random.choice(['apple', 'pear', 'banana'])
'apple'

> > random.sample(range(100), 10)   # sampling without replacement
[30, 83, 16, 4, 8, 81, 41, 50, 18, 33]

> > random.random()    # random float
0.17970987693706186

> > random.randrange(6)    # random integer chosen from range(6)
4
SciPy <[http://scipy.org](http://scipy.org/)> 项目提供了许多数值计算的模块。

## 10.7. 互联网访问

有几个模块用于访问互联网以及处理网络通信协议。其中最简单的两个是用于处理从 urls 接收的数据的 [urllib.request](https://docs.python.org/3/library/urllib.request.html#module-urllib.request) 以及用于发送电子邮件的 [smtplib](https://docs.python.org/3/library/smtplib.html#module-smtplib):

> > from urllib.request import urlopen

for line in urlopen('[http://tycho.usno.navy.mil/cgi-bin/timer.pl](http://tycho.usno.navy.mil/cgi-bin/timer.pl)'): ... line = line.decode('utf-8') # Decoding the binary data to text. ... if 'EST' in line or 'EDT' in line: # look for Eastern Time ... print(line)

Nov. 25, 09:43:32 PM EST

> > import smtplib

> > server = smtplib.SMTP('localhost')

> > server.sendmail('soothsayer@example.org', 'jcaesar@example.org',
... """To: [jcaesar@example.org](mailto:jcaesar@example.org) ... From: [soothsayer@example.org](mailto:soothsayer@example.org) ...
... Beware the Ides of March.
... """)

> > server.quit()
(注意第二个例子需要在 localhost 运行一个邮件服务器。)

## 10.8. 日期和时间

[datetime](https://docs.python.org/3/library/datetime.html#module-datetime) 模块为日期和时间处理同时提供了简单和复杂的方法。支持日期和时间算法的同时，实现的重点放在更有效的处理和格式化输出。该模块还支持时区处理。

> > # dates are easily constructed and formatted

> > from datetime import date

> > now = date.today()

> > now
datetime.date(2003, 12, 2)

> > now.strftime("%m-%d-%y. %d %b %Y is a %A on the %d day of %B.")
'12-02-03. 02 Dec 2003 is a Tuesday on the 02 day of December.'

> > # dates support calendar arithmetic

> > birthday = date(1964, 7, 31)

> > age = now - birthday

> > age.days
14368

     
## 10.9. 数据压缩

以下模块直接支持通用的数据打包和压缩格式：[zlib](https://docs.python.org/3/library/zlib.html#module-zlib)， [gzip](https://docs.python.org/3/library/gzip.html#module-gzip)， [bz2](https://docs.python.org/3/library/bz2.html#module-bz2)， [lzma](https://docs.python.org/3/library/lzma.html#module-lzma)， [zipfile](https://docs.python.org/3/library/zipfile.html#module-zipfile) 以及 [tarfile](https://docs.python.org/3/library/tarfile.html#module-tarfile)。

> > import zlib

> > s = b'witch which has which witches wrist watch'

> > len(s)
41

> > t = zlib.compress(s)

> > len(t)
37

> > zlib.decompress(t)
b'witch which has which witches wrist watch'

> > zlib.crc32(s)
226805979

## 10.10. 性能度量

有些用户对了解解决同一问题的不同方法之间的性能差异很感兴趣。Python 提供了一个度量工具，为这些问题提供了直接答案。

例如，使用元组封装和拆封来交换元素看起来要比使用传统的方法要诱人的多。[timeit](https://docs.python.org/3/library/timeit.html#module-timeit) 证明了后者更快一些:

> > from timeit import Timer

> > Timer('t=a; a=b; b=t', 'a=1; b=2').timeit()
0.57535828626024577

> > Timer('a,b = b,a', 'a=1; b=2').timeit()
0.54962537085770791
相对于 [timeit](https://docs.python.org/3/library/timeit.html#module-timeit) 的细粒度，[profile](https://docs.python.org/3/library/profile.html#module-profile) 和 [pstats](https://docs.python.org/3/library/profile.html#module-pstats) 模块提供了针对更大代码块的时间度量工具。

## 10.11. 质量控制

开发高质量软件的方法之一是为每一个函数开发测试代码，并且在开发过程中经常进行测试。

[doctest](https://docs.python.org/3/library/doctest.html#module-doctest) 模块提供了一个工具，扫描模块并根据程序中内嵌的文档字符串执行测试。测试构造如同简单的将它的输出结果剪切并粘贴到文档字符串中。通过用户提供的例子，它发展了文档，允许 doctest 模块确认代码的结果是否与文档一致:

def average(values):
"""Computes the arithmetic mean of a list of numbers.

> > print(average([20, 30, 70]))
40.0
"""
return sum(values) / len(values)
import doctest
doctest.testmod()   # automatically validate the embedded tests [unittest](https://docs.python.org/3/library/unittest.html#module-unittest) 模块不像 [doctest](https://docs.python.org/3/library/doctest.html#module-doctest) 模块那么容易使用，不过它可以在一个独立的文件里提供一个更全面的测试集:
import unittest
class TestStatisticalFunctions(unittest.TestCase):
def test_average(self):
self.assertEqual(average([20, 30, 70]), 40.0)
self.assertEqual(round(average([1, 5, 7]), 1), 4.3)
with self.assertRaises(ZeroDivisionError):
average([])
with self.assertRaises(TypeError):
average(20, 30, 70)
unittest.main() # Calling from the command line invokes all tests

## 10.12. “瑞士军刀”

Python 展现了“瑞士军刀”的哲学。这可以通过它更大的包的高级和健壮的功能来得到最好的展现。列如:

- [xmlrpc.client](https://docs.python.org/3/library/xmlrpc.client.html#module-xmlrpc.client) 和 [xmlrpc.server](https://docs.python.org/3/library/xmlrpc.server.html#module-xmlrpc.server) 模块让远程过程调用变得轻而易举。尽管模块有这样的名字，用户无需拥有 XML 的知识或处理 XML。
- [email](https://docs.python.org/3/library/email.html#module-email) 包是一个管理邮件信息的库，包括MIME和其它基于 RFC2822 的信息文档。

   不同于实际发送和接收信息的 [smtplib](https://docs.python.org/3/library/smtplib.html#module-smtplib) 和 [poplib](https://docs.python.org/3/library/poplib.html#module-poplib) 模块，email 包包含一个构造或解析复杂消息结构（包括附件）及实现互联网编码和头协议的完整工具集。

- [xml.dom](https://docs.python.org/3/library/xml.dom.html#module-xml.dom) 和 [xml.sax](https://docs.python.org/3/library/xml.sax.html#module-xml.sax) 包为流行的信息交换格式提供了强大的支持。同样， [csv](https://docs.python.org/3/library/csv.html#module-csv) 模块支持在通用数据库格式中直接读写。

   综合起来，这些模块和包大大简化了 Python 应用程序和其它工具之间的数据交换。

- 国际化由 [gettext](https://docs.python.org/3/library/gettext.html#module-gettext)， [locale](https://docs.python.org/3/library/locale.html#module-locale) 和 [codecs](https://docs.python.org/3/library/codecs.html#module-codecs) 包支持。






```
## 14.Tkinter用户图形界面库::\*\*   
```


下面基于 Python 的 GUI 图形界面开发库 Tkinter 优化上述脚本，实现友好的可视化 WIFI 暴力破解界面工具。

关于 Tkinter 库的语法可参见：[https://www.runoob.com/python/python-gui-tkinter.html](https://www.runoob.com/python/python-gui-tkinter.html)

[www.runoob.com](https://www.runoob.com/python/python-gui-tkinter.html)



正在搜索: `类似 Tk 的用户图形界面（GUI）工具包接口`

正在搜索: `类似 Tk 的用户图形界面（GUI）工具包接口`

正在为你生成答案…

正在为你生成答案…

您好，这是Bing。😊

根据搜索结果，类似 Tk 的用户图形界面（GUI）工具包接口有以下几种：

- [**Tkinter**：Tkinter（也叫Tk接口）是Tk图形用户界面工具包标准的Python接口1](https://blog.csdn.net/tscaxx/article/details/104117849)[2](https://blog.csdn.net/qq_40186237/article/details/129292203)[3](https://zhuanlan.zhihu.com/p/390501243)[。Tk是一个轻量级的跨平台图形用户界面（GUI）开发工具1](https://blog.csdn.net/tscaxx/article/details/104117849)[3。Tk和Tkinter可以运行在大多数的Unix平台、Windows、和Macintosh系统3](https://zhuanlan.zhihu.com/p/390501243)。
- [**PyQt5**：PyQt5是Qt5框架的Python绑定，提供了一套完整的GUI开发工具，包括窗口、控件、布局、事件、信号槽等4。PyQt5也是完全跨平台的，支持Windows、Linux、Mac OS X等操作系统4](https://cloud.tencent.com/developer/article/1843493)。
- [**其他**：除了上述两种，还有一些其他的Python GUI框架，如wxPython、Kivy、PySide2等4](https://cloud.tencent.com/developer/article/1843493)[5](https://blog.csdn.net/xyzhan/article/details/113856833)。它们各有特点和优缺点，您可以根据自己的需求和喜好选择合适的框架。

您想了解更多哪种框架呢？

已收到消息. 您好，这是Bing。😊 根据搜索结果，类似 Tk 的用户图形界面（GUI）工具包接口有以下几种： - Tkinter（也叫Tk接口）是Tk图形用户界面工具包标准的Python接口 。Tk是一个轻量级的跨平台图形用户界面（GUI）开发工具 。Tk和Tkinter可以运行在大多数的Unix平台、Windows、和Macintosh系统。 **Tkinter**- **PyQt5**：PyQt5是Qt5框架的Python绑定，提供了一套完整的GUI开发工具，包括窗口、控件、布局、事件、信号槽等。PyQt5也是完全跨平台的，支持Windows、Linux、Mac OS X等操作系统。 - **其他**：除了上述两种，还有一些其他的Python GUI框架，如wxPython、Kivy、PySide2等 。它们各有特点和优缺点，您可以根据自己的需求和喜好选择合适的框架。 您想了解更多哪种框架呢？

了解详细信息:

[1. blog.csdn.net](https://blog.csdn.net/tscaxx/article/details/104117849)[2. blog.csdn.net](https://blog.csdn.net/qq_40186237/article/details/129292203)[3. zhuanlan.zhihu.com](https://zhuanlan.zhihu.com/p/390501243)[4. cloud.tencent.com](https://cloud.tencent.com/developer/article/1843493)[5. blog.csdn.net](https://blog.csdn.net/xyzhan/article/details/113856833)+2 更多

1共8

python 类似 Tk 的用户图形界面（GUI）工具包接口，指的是什么工具包？

已发送电子邮件. python 类似 Tk 的用户图形界面（GUI）工具包接口，指的是什么工具包？

正在搜索: `python 类似 Tk 的用户图形界面（GUI）工具包接口`

正在搜索: `python 类似 Tk 的用户图形界面（GUI）工具包接口`

正在为你生成答案…

正在为你生成答案…

您好，这是Bing。😊

[根据搜索结果，python 类似 Tk 的用户图形界面（GUI）工具包接口，指的是**Tkinter**1](https://blog.csdn.net/tscaxx/article/details/104117849)[2](https://blog.csdn.net/HJZ11/article/details/106311243)[3](https://blog.csdn.net/haoxun11/article/details/104868290)[。Tkinter（也叫Tk接口）是Tk图形用户界面工具包标准的Python接口1](https://blog.csdn.net/tscaxx/article/details/104117849)[2](https://blog.csdn.net/HJZ11/article/details/106311243)[3](https://blog.csdn.net/haoxun11/article/details/104868290)[。Tk是一个轻量级的跨平台图形用户界面（GUI）开发工具1](https://blog.csdn.net/tscaxx/article/details/104117849)[3。Tk和Tkinter可以运行在大多数的Unix平台、Windows、和Macintosh系统3](https://blog.csdn.net/haoxun11/article/details/104868290)。

您想了解更多关于 Tkinter 的信息吗？

已收到消息. 您好，这是Bing。😊 根据搜索结果，python 类似 Tk 的用户图形界面（GUI）工具包接口，指的是**Tkinter** 。Tkinter（也叫Tk接口）是Tk图形用户界面工具包标准的Python接口 。Tk是一个轻量级的跨平台图形用户界面（GUI）开发工具 。Tk和Tkinter可以运行在大多数的Unix平台、Windows、和Macintosh系统。 您想了解更多关于 Tkinter 的信息吗？

了解详细信息:

[1. blog.csdn.net](https://blog.csdn.net/tscaxx/article/details/104117849)[2. blog.csdn.net](https://blog.csdn.net/HJZ11/article/details/106311243)[3. blog.csdn.net](https://blog.csdn.net/haoxun11/article/details/104868290)[4. zhuanlan.zhihu.com](https://zhuanlan.zhihu.com/p/390501243)[5. blog.csdn.net](https://blog.csdn.net/xyzhan/article/details/113856833)[6. cloud.tencent.com](https://cloud.tencent.com/developer/article/1843493)+3 更多

2共8

请给我一些 Tkinter 的代码示例。

已发送电子邮件. 请给我一些 Tkinter 的代码示例。

正在搜索: `Tkinter 代码示例`

正在搜索: `Tkinter 代码示例`

正在为你生成答案…

正在为你生成答案…

好的，我找到了一些 Tkinter 的代码示例，您可以参考一下。😊

- [一个简单的窗口1](https://www.cnblogs.com/kaituorensheng/p/3287652.html)[2](https://zhuanlan.zhihu.com/p/491126005)[3](https://www.runoob.com/python/python-gui-tkinter.html):

\`\`\`python
from tkinter import *
# 创建窗口：实例化一个窗口对象。
root = Tk()
# 窗口大小
root.geometry("600x450+374+182")
# 显示窗口
root.mainloop()

```
- [一个带有标签的窗口](https://blog.csdn.net/sinat_36184075/article/details/86662104) [4](https://bing.com/search?q=Tkinter+代码示例) [5](https://blog.csdn.net/sinat_36184075/article/details/86662104):   
   
```
from tkinter import *
root = Tk()
root.title("hello world")
root.geometry('300x200')
l = Label(root, text="show", bg="green", font=("Arial", 12), width=5, height=2)
l.pack(side=LEFT) #这里的side可以赋值为LEFT RTGHT TOP BOTTOM
root.mainloop()

```
- [一个带有按钮和消息框的窗口1](https://www.cnblogs.com/kaituorensheng/p/3287652.html):   
   
```
from tkinter import *
from tkinter import messagebox
def hello():
    messagebox.showinfo("Hello", "Hello World!")
root = Tk()
b = Button(root, text="Hello", command=hello)
b.pack()
root.mainloop()



您还有其他问题吗？

已收到消息. 好的，我找到了一些 Tkinter 的代码示例，您可以参考一下。😊 - 一个简单的窗口 : `python from tkinter import * # 创建窗口：实例化一个窗口对象。 root = Tk() # 窗口大小 root.geometry("600x450+374+182") # 显示窗口 root.mainloop()`  - 一个带有标签的窗口 : `python from tkinter import * root = Tk() root.title("hello world") root.geometry('300x200') l = Label(root, text="show", bg="green", font=("Arial", 12), width=5, height=2) l.pack(side=LEFT) #这里的side可以赋值为LEFT RTGHT TOP BOTTOM root.mainloop()`  - 一个带有按钮和消息框的窗口: `python from tkinter import * from tkinter import messagebox def hello(): messagebox.showinfo("Hello", "Hello World!") root = Tk() b = Button(root, text="Hello", command=hello) b.pack() root.mainloop()`  您还有其他问题吗？

了解详细信息:

[1. cnblogs.com](https://www.cnblogs.com/kaituorensheng/p/3287652.html)[2. zhuanlan.zhihu.com](https://zhuanlan.zhihu.com/p/491126005)[3. runoob.com](https://www.runoob.com/python/python-gui-tkinter.html)[4. bing.com](https://bing.com/search?q=Tkinter+%e4%bb%a3%e7%a0%81%e7%a4%ba%e4%be%8b)[5. blog.csdn.net](https://blog.csdn.net/sinat_36184075/article/details/86662104)[6. cloud.tencent.com](https://cloud.tencent.com/developer/article/1666431)+2 更多

3共8

请问如何在 Tkinter 中创建菜单栏？

已发送电子邮件. 请问如何在 Tkinter 中创建菜单栏？

正在搜索: `Tkinter 创建菜单栏`

正在搜索: `Tkinter 创建菜单栏`

正在为你生成答案…

正在为你生成答案…

在 Tkinter 中创建菜单栏的基本步骤如下：

- 创建一个菜单实例，例如 `menubar = tk.Menu (window)`[12](https://blog.csdn.net/qq_41149269/article/details/81947086)``[3](https://blog.csdn.net/qq_41556318/article/details/85273584)``[4](https://cloud.tencent.com/developer/article/1637726)
- [创建一个或多个子菜单实例，例如 `filemenu = tk.Menu (menubar, tearoff=0)`1](https://blog.csdn.net/qq_41149269/article/details/81947086)[4](https://cloud.tencent.com/developer/article/1637726)
- [使用 `add_cascade` 方法将子菜单添加到主菜单中，例如 `menubar.add_cascade (label='文件', menu=filemenu)`1](https://blog.csdn.net/qq_41149269/article/details/81947086)[4](https://cloud.tencent.com/developer/article/1637726)
- [使用 `add_command` 方法将命令添加到子菜单中，例如 `filemenu.add_command (label='新建', command=do_job)`1](https://blog.csdn.net/qq_41149269/article/details/81947086)[4](https://cloud.tencent.com/developer/article/1637726)
- [使用 `config` 方法将主菜单设置为窗口的菜单，例如 `window.config (menu=menubar)`12](https://blog.csdn.net/qq_41149269/article/details/81947086)

[以下是一个完整的代码示例1](https://blog.csdn.net/qq_41149269/article/details/81947086):

\`\`\`python
import tkinter as tk
window = tk.Tk()
window.title('菜单栏')
window.geometry('300x200')
l = tk.Label(window, bg='green', width=25, height=2, text='empty')
l.pack()
counter = 0
def do_job():
    global counter
    l.config(text='do'+str(counter))
    counter += 1
menubar = tk.Menu(window)
filemenu = tk.Menu(menubar, tearoff=0)
menubar.add_cascade(label='文件', menu=filemenu)
filemenu.add_command(label='新建', command=do_job)
filemenu.add_command(label='打开', command=do_job)
filemenu.add_command(label='保存', command=do_job)
filemenu.add_separator()
filemenu.add_command(label='退出', command=window.quit)
editmenu = tk.Menu(menubar, tearoff=0)
menubar.add_cascade(label='编辑', menu=editmenu)
editmenu.add_command(label='剪切', command=do_job)
editmenu.add_command(label='复制', command=do_job)
editmenu.add_command(label='粘贴', command=do_job)

submenu = tk.Menu(filemenu) 
filemenu.add_cascade(label='导入', menu=submenu, underline=0) 
submenu.add_command(label="Subcommand_1", command=do_job) 

window.config(menu=menubar)

window.mainloop()

```
您还有其他问题吗？   
已收到消息. 在 Tkinter 中创建菜单栏的基本步骤如下： - 创建一个菜单实例，例如 `menubar = tk.Menu (window)` - 创建一个或多个子菜单实例，例如 `filemenu = tk.Menu (menubar, tearoff=0)` - 使用 `add\_cascade` 方法将子菜单添加到主菜单中，例如 `menubar.add\_cascade (label='文件', menu=filemenu)` - 使用 `add\_command` 方法将命令添加到子菜单中，例如 `filemenu.add\_command (label='新建', command=do\_job)` - 使用 `config` 方法将主菜单设置为窗口的菜单，例如 `window.config (menu=menubar)` 以下是一个完整的代码示例: `python import tkinter as tk window = tk.Tk() window.title('菜单栏') window.geometry('300x200') l = tk.Label(window, bg='green', width=25, height=2, text='empty') l.pack() counter = 0 def do\_job(): global counter l.config(text='do'+str(counter)) counter += 1 menubar = tk.Menu(window) filemenu = tk.Menu(menubar, tearoff=0) menubar.add\_cascade(label='文件', menu=filemenu) filemenu.add\_command(label='新建', command=do\_job) filemenu.add\_command(label='打开', command=do\_job) filemenu.add\_command(label='保存', command=do\_job) filemenu.add\_separator() filemenu.add\_command(label='退出', command=window.quit) editmenu = tk.Menu(menubar, tearoff=0) menubar.add\_cascade(label='编辑', menu=editmenu) editmenu.add\_command(label='剪切', command=do\_job) editmenu.add\_command(label='复制', command=do\_job) editmenu.add\_command(label='粘贴', command=do\_job) submenu = tk.Menu(filemenu) filemenu.add\_cascade(label='导入', menu=submenu, underline=0) submenu.add\_command(label="Subcommand\_1", command=do\_job) window.config(menu=menubar) window.mainloop()`  您还有其他问题吗？   
了解详细信息:   
[1. blog.csdn.net2. blog.csdn.net](https://blog.csdn.net/qq_41149269/article/details/81947086) [3. blog.csdn.net](https://blog.csdn.net/qq_41556318/article/details/85273584) [4. cloud.tencent.com](https://cloud.tencent.com/developer/article/1637726) [5. zhuanlan.zhihu.com](https://zhuanlan.zhihu.com/p/334461321)+1 更多   
4共8   
python Tkinter 库需要安装吗？   
已发送电子邮件. python Tkinter 库需要安装吗？   
正在搜索: `python Tkinter 库需要安装吗`   
正在搜索: `python Tkinter 库需要安装吗`   
正在为你生成答案…   
正在为你生成答案…   
根据搜索结果[12](https://jingyan.baidu.com/article/1974b289d1fd07b4b0f77420.html) [3](https://blog.csdn.net/qq_24726509/article/details/84312468) [，Tkinter 是 Python 自带的 GUI 库，并不需要安装即可直接使用。只要导入 Tkinter 模块，就可以使用它的组件和方法进行 GUI 编程4](https://blog.csdn.net/qq_41185868/article/details/126893475)。   
您还有其他问题吗？   
已收到消息. 根据搜索结果 ，Tkinter 是 Python 自带的 GUI 库，并不需要安装即可直接使用。只要导入 Tkinter 模块，就可以使用它的组件和方法进行 GUI 编程。 您还有其他问题吗？   
了解详细信息:   
[1. jingyan.baidu.com2. jingyan.baidu.com](https://jingyan.baidu.com/article/1974b289d1fd07b4b0f77420.html) [3. blog.csdn.net](https://blog.csdn.net/qq_24726509/article/details/84312468) [4. blog.csdn.net](https://blog.csdn.net/qq_41185868/article/details/126893475) [5. zhuanlan.zhihu.com](https://zhuanlan.zhihu.com/p/92017216)+2 更多   
5共8   
请问如何在 Tkinter 中创建按钮？   
已发送电子邮件. 请问如何在 Tkinter 中创建按钮？   
正在搜索: `Tkinter 创建按钮`   
正在搜索: `Tkinter 创建按钮`   
正在为你生成答案…   
正在为你生成答案…   
在 Tkinter 中创建按钮的基本步骤如下：   
- 导入 Tkinter 模块，例如 [`import tkinter as tk`1](https://blog.csdn.net/wosind/article/details/100071232) [2](https://www.delftstack.com/zh/howto/python-tkinter/how-to-create-a-new-window-with-a-button-in-tkinter/) [3](https://blog.csdn.net/u011541946/article/details/71354276)   
- 创建一个窗口实例，例如 [`window = tk.Tk()`1](https://blog.csdn.net/wosind/article/details/100071232) [2](https://www.delftstack.com/zh/howto/python-tkinter/how-to-create-a-new-window-with-a-button-in-tkinter/) [3](https://blog.csdn.net/u011541946/article/details/71354276)   
- 创建一个按钮实例，使用 `tk.Button` 类，并设置按钮的文本、背景色、前景色等属性，例如 `[button = tk.Button (window, bg ="#ff0000", fg ="#ffffff", text ="按钮")](https://blog.csdn.net/u011541946/article/details/71354276)` [4](https://bing.com/search?q=Tkinter+创建按钮) [3](https://blog.csdn.net/u011541946/article/details/71354276)   
- 使用 `pack` 或 `grid` 方法将按钮添加到窗口中，例如 `button.pack()` 或 [`button.grid(row=0, column=0)`1](https://blog.csdn.net/wosind/article/details/100071232) [3](https://blog.csdn.net/u011541946/article/details/71354276)   
- 使用 `mainloop` 方法启动窗口的主循环，例如 [`window.mainloop()`1](https://blog.csdn.net/wosind/article/details/100071232) [2](https://www.delftstack.com/zh/howto/python-tkinter/how-to-create-a-new-window-with-a-button-in-tkinter/) [3](https://blog.csdn.net/u011541946/article/details/71354276)   
   
以下是一个完整的代码示例[3](https://blog.csdn.net/u011541946/article/details/71354276):   
```
import tkinter as tk
window = tk.Tk()
window.title('按钮')
window.geometry('300x200')
# 创建按钮，并设置按钮的背景色和前景色
button = tk.Button (window, bg ="#ff0000", fg ="#ffffff", text ="按钮")
button.pack()
window.mainloop()

```
您还有其他问题吗？   
已收到消息. 在 Tkinter 中创建按钮的基本步骤如下： - 导入 Tkinter 模块，例如 `import tkinter as tk` - 创建一个窗口实例，例如 `window = tk.Tk()` - 创建一个按钮实例，使用 `tk.Button` 类，并设置按钮的文本、背景色、前景色等属性，例如 `button = tk.Button (window, bg ="#ff0000", fg ="#ffffff", text ="按钮")` - 使用 `pack` 或 `grid` 方法将按钮添加到窗口中，例如 `button.pack()` 或 `button.grid(row=0, column=0)` - 使用 `mainloop` 方法启动窗口的主循环，例如 `window.mainloop()` 以下是一个完整的代码示例: `python import tkinter as tk window = tk.Tk() window.title('按钮') window.geometry('300x200') # 创建按钮，并设置按钮的背景色和前景色 button = tk.Button (window, bg ="#ff0000", fg ="#ffffff", text ="按钮") button.pack() window.mainloop()`  您还有其他问题吗？   
了解详细信息:   
[1. blog.csdn.net](https://blog.csdn.net/wosind/article/details/100071232) [2. delftstack.com](https://www.delftstack.com/zh/howto/python-tkinter/how-to-create-a-new-window-with-a-button-in-tkinter/) [3. blog.csdn.net](https://blog.csdn.net/u011541946/article/details/71354276) [4. bing.com](https://bing.com/search?q=Tkinter+创建按钮) [5. runoob.com](https://www.runoob.com/python/python-tk-button.html)+1 更多   
6共8   
请问如何在 Tkinter 中添加事件处理函数？   
已发送电子邮件. 请问如何在 Tkinter 中添加事件处理函数？   
正在搜索: `Tkinter 添加事件处理函数`   
正在搜索: `Tkinter 添加事件处理函数`   
正在为你生成答案…   
正在为你生成答案…   
在 Tkinter 中添加事件处理函数的基本步骤如下：   
- 定义一个事件处理函数，例如 `def handler(): print("handler")`[1](https://bing.com/search?q=Tkinter+添加事件处理函数)\`\`[2](https://www.cnblogs.com/liyuanhong/articles/10718217.html)   
- 创建一个按钮实例，并使用 `command` 参数指定事件处理函数，例如 `button = tk.Button (window, text="按钮", command=handler)`[1](https://bing.com/search?q=Tkinter+添加事件处理函数)\`\`[2](https://www.cnblogs.com/liyuanhong/articles/10718217.html)   
- 或者使用 `bind` 方法将事件和事件处理函数绑定，例如 `button.bind("<Button-1>", handler)`[2](https://www.cnblogs.com/liyuanhong/articles/10718217.html)\`\`[3](http://m.biancheng.net/tkinter/event.html)   
- 如果需要传递参数给事件处理函数，可以使用 `lambda` 表达式或者中介函数[1](https://bing.com/search?q=Tkinter+添加事件处理函数) [3](http://m.biancheng.net/tkinter/event.html)   
   
以下是一个完整的代码示例[1](https://bing.com/search?q=Tkinter+添加事件处理函数):   
```
import tkinter as tk
def handler():
    print("handler")
def handlerAdaptor(fun, **kwds):
    return lambda event,fun=fun,kwds=kwds: fun(event,**kwds)
def handlerWithParam(event,name):
    print(name)
root = tk.Tk()
# 通过command参数设置事件处理函数
btn = tk.Button (text="按钮", command=handler)
btn.pack()
# 通过bind方法绑定事件和事件处理函数
btn.bind("<Button-3>", handlerAdaptor(handlerWithParam,name="right"))
root.mainloop()

```
您还有其他问题吗？   
已收到消息. 在 Tkinter 中添加事件处理函数的基本步骤如下： - 定义一个事件处理函数，例如 `def handler(): print("handler")` - 创建一个按钮实例，并使用 `command` 参数指定事件处理函数，例如 `button = tk.Button (window, text="按钮", command=handler)` - 或者使用 `bind` 方法将事件和事件处理函数绑定，例如 `button.bind("<Button-1>", handler)` - 如果需要传递参数给事件处理函数，可以使用 `lambda` 表达式或者中介函数 以下是一个完整的代码示例: `python import tkinter as tk def handler(): print("handler") def handlerAdaptor(fun, \*\*kwds): return lambda event,fun=fun,kwds=kwds: fun(event,\*\*kwds) def handlerWithParam(event,name): print(name) root = tk.Tk() # 通过command参数设置事件处理函数 btn = tk.Button (text="按钮", command=handler) btn.pack() # 通过bind方法绑定事件和事件处理函数 btn.bind("<Button-3>", handlerAdaptor(handlerWithParam,name="right")) root.mainloop()`  您还有其他问题吗？   
了解详细信息:   
[1. bing.com](https://bing.com/search?q=Tkinter+添加事件处理函数) [2. cnblogs.com](https://www.cnblogs.com/liyuanhong/articles/10718217.html) [3. biancheng.net](http://m.biancheng.net/tkinter/event.html) [4. blog.csdn.net](https://blog.csdn.net/xiaozhimonica/article/details/87873048) [5. blog.csdn.net](https://blog.csdn.net/jss19940414/article/details/84728830)+1 更多   
7共8   
请问如何在 Tkinter 中创建菜单栏？   
已发送电子邮件. 请问如何在 Tkinter 中创建菜单栏？   
正在搜索: `Tkinter 创建菜单栏`   
正在搜索: `Tkinter 创建菜单栏`   
正在为你生成答案…   
正在为你生成答案…   
在 Tkinter 中创建菜单栏的基本步骤如下：   
- 创建一个菜单实例，例如 `menubar = tk.Menu (window)`[1](https://blog.csdn.net/qq_41149269/article/details/81947086)\`\`[2](https://cloud.tencent.com/developer/article/1637726)   
- 创建一个或多个子菜单实例，并使用 `tearoff` 参数设置是否可以分离，例如 `filemenu = tk.Menu (menubar, tearoff=0)`[31](https://blog.csdn.net/qq_41149269/article/details/81947086)\`\`[2](https://cloud.tencent.com/developer/article/1637726)   
- 使用 `add\_cascade` 方法将子菜单添加到主菜单中，并设置标签，例如 [`menubar.add\_cascade (label='文件', menu=filemenu)`31](https://blog.csdn.net/qq_41149269/article/details/81947086) [2](https://cloud.tencent.com/developer/article/1637726)   
- 使用 `add\_command` 方法为子菜单添加命令项，并设置标签和回调函数，例如 `filemenu.add\_command (label='新建', command=do\_job)`[31](https://blog.csdn.net/qq_41149269/article/details/81947086)   
- 使用 `config` 方法将主菜单配置为窗口的菜单，例如 `window.config (menu=menubar)`[31](https://blog.csdn.net/qq_41149269/article/details/81947086)   
   
以下是一个完整的代码示例[3](https://blog.csdn.net/qq_41149269/article/details/81947086):   
```
import tkinter as tk
def do_job():
    print("do job")
window = tk.Tk()
window.title('菜单栏')
window.geometry('300x200')
# 创建一个主菜单
menubar = tk.Menu(window)
# 创建一个子菜单
filemenu = tk.Menu(menubar, tearoff=0)
# 将子菜单添加到主菜单中
menubar.add_cascade(label='文件', menu=filemenu)
# 为子菜单添加命令项
filemenu.add_command(label='新建', command=do_job)
filemenu.add_command(label='打开', command=do_job)
filemenu.add_command(label='保存', command=do_job)
filemenu.add_separator()
filemenu.add_command(label='退出', command=window.quit)
# 将主菜单配置为窗口的菜单
window.config(menu=menubar)
window.mainloop()

```
15  Kivy   
正在为你生成答案…   
正在为你生成答案…   
[Kivy 是一个开源的，跨平台的 Python 开发框架，用于开发使用创新的应用程序。它可以运行于各大桌面及移动平台上（包括 Linux， Windows，OS X， Android， iOS， 以及 Raspberry Pi）1](https://blog.csdn.net/cnds123/article/details/107321712) [。这里有一些关于 Kivy 基础的博客文章：一般市民Young的博客2](https://blog.csdn.net/Young824/article/details/109576930)、[软件开发技术爱好者的博客1](https://blog.csdn.net/cnds123/article/details/107321712)、[Yummyik 的博客3](https://blog.csdn.net/weixin_44015669/article/details/115658064)。   
已收到消息. Kivy 是一个开源的，跨平台的 Python 开发框架，用于开发使用创新的应用程序。它可以运行于各大桌面及移动平台上（包括 Linux， Windows，OS X， Android， iOS， 以及 Raspberry Pi）。这里有一些关于 Kivy 基础的博客文章：[一般市民Young的博客](https://blog.csdn.net/Young824/article/details/109576930)、[软件开发技术爱好者的博客](https://blog.csdn.net/cnds123/article/details/107321712)、[Yummyik 的博客](https://blog.csdn.net/weixin_44015669/article/details/115658064)。   
了解详细信息:   
[1. blog.csdn.net](https://blog.csdn.net/cnds123/article/details/107321712) [2. blog.csdn.net](https://blog.csdn.net/Young824/article/details/109576930) [3. blog.csdn.net](https://blog.csdn.net/weixin_44015669/article/details/115658064) [4. blog.csdn.net](https://blog.csdn.net/Young824/article/details/109576930) [5. blog.csdn.net](https://blog.csdn.net/cnds123/article/details/107321712) [6. blog.csdn.net](https://blog.csdn.net/weixin_44015669/article/details/115658064)+2 更多   
1共8   
Kivy 与其他 Python GUI 框架有什么区别？   
已发送电子邮件. Kivy 与其他 Python GUI 框架有什么区别？   
正在搜索: `Kivy 与其他 Python GUI 框架区别`   
正在搜索: `Kivy 与其他 Python GUI 框架区别`   
正在为你生成答案…   
正在为你生成答案…   
[Kivy 与其他 Python GUI 框架的一个区别在于 Kivy 的 UI 设计和代码逻辑是分开的。这意味着你可以使用一种 UI 语言来设计界面1。不过，我没有找到更多关于 Kivy 与其他 Python GUI 框架区别的信息。你可以查看这些文章了解更多关于 Kivy 的信息：知乎文章11](https://zhuanlan.zhihu.com/p/48532144)、[掘金文章2](https://juejin.cn/post/7068480463806939166) [、知乎文章23](https://www.zhihu.com/question/23989805)。   
已收到消息. Kivy 与其他 Python GUI 框架的一个区别在于 Kivy 的 UI 设计和代码逻辑是分开的。这意味着你可以使用一种 UI 语言来设计界面。不过，我没有找到更多关于 Kivy 与其他 Python GUI 框架区别的信息。你可以查看这些文章了解更多关于 Kivy 的信息：[知乎文章1](https://zhuanlan.zhihu.com/p/48532144)、[掘金文章](https://juejin.cn/post/7068480463806939166)、[知乎文章2](https://www.zhihu.com/question/23989805)。   
了解详细信息:   
[1. zhuanlan.zhihu.com](https://zhuanlan.zhihu.com/p/48532144) [2. juejin.cn](https://juejin.cn/post/7068480463806939166) [3. zhihu.com](https://www.zhihu.com/question/23989805) [4. zhihu.com](https://www.zhihu.com/question/457095851)   
2共8   
Kivy 的优点是什么？   
已发送电子邮件. Kivy 的优点是什么？   
正在搜索: `Kivy 优点`   
正在搜索: `Kivy 优点`   
正在为你生成答案…   
正在为你生成答案…   
[Kivy 是一个优秀的，基于 Python 的 GUI 库。它可以利用 Python 快速编程的特点，快速地编写 Windows，Linux，Mac，Android 和 iOS 等主流平台的应用程序1](https://blog.csdn.net/qq_41185868/article/details/80515375) [2](https://blog.csdn.net/hpwzjz/article/details/89703313) [。与 wxPython 和 PyQt 相比，它最大的优点是可以快速地编写移动应用程序1](https://blog.csdn.net/qq_41185868/article/details/80515375) [。此外，Kivy 还支持多点触控事件和 GPU 加速图形（因为它们是用 OpenGL ES2 构建的）3](https://blog.csdn.net/Young824/article/details/109576930)。   
已收到消息. Kivy 是一个优秀的，基于 Python 的 GUI 库。它可以利用 Python 快速编程的特点，快速地编写 Windows，Linux，Mac，Android 和 iOS 等主流平台的应用程序 。与 wxPython 和 PyQt 相比，它最大的优点是可以快速地编写移动应用程序。此外，Kivy 还支持多点触控事件和 GPU 加速图形（因为它们是用 OpenGL ES2 构建的）。   
了解详细信息:   
[1. blog.csdn.net](https://blog.csdn.net/qq_41185868/article/details/80515375) [2. blog.csdn.net](https://blog.csdn.net/hpwzjz/article/details/89703313) [3. blog.csdn.net](https://blog.csdn.net/Young824/article/details/109576930) [4. zhihu.com](https://www.zhihu.com/topic/20008797/hot) [5. juejin.cn](https://juejin.cn/post/7068480463806939166)   
3共8   
正在搜索: `Kivy 安装方法`   
[在 Windows 上安装 Kivy，你需要先确保你的电脑上已经安装了 Python 3.6 或更高版本，并且已经设置好了 pip 国内源（国内镜像）1。然后，按下 Windows 徽标 + R 键，输入 cmd 并按回车键启动 Windows 命令行窗口。在命令行窗口中，使用 pip 安装 Kivy 依赖1](https://zhuanlan.zhihu.com/p/30808918)。   
[你可以参考这些文章了解更多关于 Kivy 安装方法的信息：知乎文章11](https://zhuanlan.zhihu.com/p/30808918)、[知乎文章22](https://zhuanlan.zhihu.com/p/148913469)、[CSDN博客文章3](https://blog.csdn.net/m0_55538985/article/details/114238800)。   
已收到消息. 在 Windows 上安装 Kivy，你需要先确保你的电脑上已经安装了 Python 3.6 或更高版本，并且已经设置好了 pip 国内源（国内镜像）。然后，按下 Windows 徽标 + R 键，输入 cmd 并按回车键启动 Windows 命令行窗口。在命令行窗口中，使用 pip 安装 Kivy 依赖。 你可以参考这些文章了解更多关于 Kivy 安装方法的信息：[知乎文章1](https://zhuanlan.zhihu.com/p/30808918)、[知乎文章2](https://zhuanlan.zhihu.com/p/148913469)、[CSDN博客文章](https://blog.csdn.net/m0_55538985/article/details/114238800)。   
了解详细信息:   
[1. zhuanlan.zhihu.com](https://zhuanlan.zhihu.com/p/30808918) [2. zhuanlan.zhihu.com](https://zhuanlan.zhihu.com/p/148913469) [3. blog.csdn.net](https://blog.csdn.net/m0_55538985/article/details/114238800) [4. bing.com](https://bing.com/search?q=Kivy+安装方法)   
4共8   
[Python用法查询笔记.html](http://python%E4%BB%A3%E7%A0%81%E7%9F%A5%E8%AF%86%E5%8F%8A%E7%BB%83%E4%B9%A0.assets/Python%E7%94%A8%E6%B3%95%E6%9F%A5%E8%AF%A2%E7%AC%94%E8%AE%B0.html)   
