# Pylen   
### tages:
    - py
    - pylen
    - 练习

```

##文件名：python练习
##姓  名：Ryan6981
##日  期：2020.12.17

```
## 1-15基础练习   
```


# 练习1:print输出
print('hello Word!')  

# 练习2:
name='SGFang10000'
print(name)

# 练习3:
name='王添发'
age=42
print("我叫%s,今你年%d岁了"%(name,age))

# 练习4:
for name in ['Bart', 'Lisa', 'Adam']:
    print('Hello,',name)

# 练习5:1000元以下商品打9.5折,1000-5000元之间的商品打9折，其他情况打8.5折。请编写程序代码:实现对任意输入一件商品售价，能够输出其优惠价格与最终价格。

amount = int(input("请输入金额: "))
if amount < 1000:
   discount = amount*0.05
   print ("折扣",discount)
elif amount < 5000:
   discount = amount*0.10
   print ("折扣",discount)
else:
   discount = amount*0.15
   print ("折扣",discount)
print ("优惠金额:",amount-discount)




# 练习6:
x='Hello'
y='Chanel'
# Line feed output
print(x)
print(y)
#Print a dividing line
print('-'*20)
#Do not wrap output
print(x,end=" ")
print(y,end=" ")
print(x+y,end=" ")


# 练习7:
name ='Zhang'
position ='讲师'
address ='北京市'
print("---------------------------------------------")
print("姓名: %s" % name)
print("职位: %s" % position)
print("公司地址: %s" % address)
print("-------------------------------------------")


# 练习8:计算体重bmi值
height = float(input("请输入您的身高(单位为米):"))
print("您的身高:",height)
weight = float(input("请输入您的体重(单位千克):"))
print("您的体重:", weight)
bmi = weight / (height * height)         # bim值=身高/体重的平方
print("您的BMI指数:",bmi)
if bmi>=32:
    print("严重肥胖")
elif bmi>=28:
    print("肥胖")
elif bmi>=25:
    print("过重")
elif bmi>=18.5:
    print("正常")
else: 
    print("过轻")



# 练习9:小明的成绩从去年的72分提升到了今年的85分，请计算小明成绩提升的百分点，并用字符串格式化显示出'xx.x%'，只保留小数点后1位，请用代码实现
last_score = 72
newscore = 85
point = (newscore - last_score) * 100.0 / 72
print(point)
print('提升百分点：%.1f%%' % point)



# 练习10:if嵌套语句练习
historyscore=90
if historyscore>=60:
    print('你已经及格')
    if historyscore>=80:
        print('你很优秀')
    else:
        print('你只是一般般')
else:
    print('不及格')
    #增加额外条件if...
    if historyscore<30:
        print('学渣')
    else:
        print('还能抢救一下')



#练习11:iinput()函数结果的强制转换的用法:
age = int(input('猜一猜巫师的『法定成年年龄』是几岁，请输入：'))
#将输入的岁数(字符串)，强制转换为整数

if age > 17:
#当年龄(整数)大于17(整数）时
    print('哈哈，居然比这个年龄还要小呢！')
#打印if条件下的结果

elif age == 17:
#当年龄(整数)等于17(整数）时
    print('正确！我猜你是个巫师啦～')
#打印if条件下的结果

else:
#当年龄(整数)小于17(整数)时
    print('呜呜，这个年龄～我还是个宝宝呢，正确答案是17岁哦')
#打印else条件下的结果



#练习12:input()函数结果的强制转换的用法实例二:
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




#练习13:if嵌套循环语句:
money=3000
if money<=500:
    print('欢迎进入史塔克穷人帮前三名')
    if money<=100:
        print('恭喜您荣获“美元队长”称号!')
    else:
        print('请找弗瑞队长加薪')
elif 500<money<=1000:
    print('祝贺您至少可以温饱了。')
else:
    print('经济危机都难不倒您！')
    if money<=2000:
        print('您快比钢铁侠有钱了！')
    elif money>2000:
        print('您是不是来自于瓦坎达国')
print('程序结束')


#练习14:综合练习

print('您好，欢迎来到古灵阁，请问您需要帮助吗？')
choice=input('需要or不需要？请选择:')
if choice=='需要':
    need=int(input('请问您需要什么帮助呢？1.存取款；2.货币兑换；3.咨询:'))
    if need==2:
        amount=input('金加隆和人民币的兑换率1:51.3,请问您需要兑换多少金加隆呢?')
        print('请问您要兑换'+amount+'金加隆吗?')
        print('您需要付给我'+str(int(amount)*51.3)+'人民币')    
    elif need==1:
        print('请您去存取款窗口.') 
    else:
        print('请您去咨询窗口.')        
else:
    print('好的，再见。')

#while语句密码的练习
password = ''  # 变量password用来保存输入的密码

while password != '816':
    password = input('请尝试输入密码：')

print('欢迎回家！')

#循环语句练习
while True:
    a = input('A，你认罪吗？请回答认罪或者不认：')
    b = input('B，你认罪吗？请回答认罪或者不认：')
    if a == '认罪' and b == '认罪':
        print('两人都得判10年，唉')
        break
    elif a == '不认' and b == '认罪':
        print('A判20年，B判1年，唉')
        break
    elif a == '认罪' and b == '不认':
        print('A判1年，B判20年')
        break
    elif a == '不认' and b == '不认':
        print('都判3年，太棒了') 
        break   
    else:
        print('别捣乱，只能回答“认罪”或“不认”！')


```
## 五几个小游戏案例   
```


#用循环语句做小游戏的练习

import time,random

player_victory = 0
enemy_victory = 0

for i in range(1,4):
    time.sleep(2)  # 让局与局之间有较明显的有时间间隔
    print(' \n——————现在是第'+str(i)+'局——————')  # 作为局的标记
 
    player_life = random.randint(100,150)
    player_attack = random.randint(30,50)
    enemy_life = random.randint(100,150)
    enemy_attack = random.randint(30,50)

    # 展示双方角色的属性
    print('【玩家】\n'+'血量：'+str(player_life)+'\n攻击：'+str(player_attack))
    print('------------------------')
    time.sleep(1)
    print('【敌人】\n'+'血量：'+str(enemy_life)+'\n攻击：'+str(enemy_attack))
    print('------------------------')
    time.sleep(1)

    # 双方PK
    while player_life > 0 and enemy_life > 0:
        player_life = player_life - enemy_attack
        enemy_life = enemy_life - player_attack
        print('你发起了攻击，【敌人】剩余血量'+str(enemy_life))
        print('敌人向你发起了攻击，【玩家】剩余血量'+str(player_life))
        print('-----------------------')
        time.sleep(1.5)

    #打印最终战果
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
    print('【最终结果：你赢了！】')
elif enemy_victory > player_victory:
    print('【最终结果：你输了！】')
else: 
    print('【最终结果：平局！】')


#猜硬币小游戏第一种;
import random
guess = ''

while guess not in [0,1]:
    print('------猜硬币游戏------')
    print('猜一猜硬币是正面还是反面？')
    guess = int(input('“正面”请输入0,“反面”请输入1：'))
    #注意要用int()将字符串类型转换为数字类型

toss = random.randint(0,1)

if toss == guess:
    print('猜对了！你真棒')
else:
    print('没猜对，再给你一次机会。')
    guess = int(input('再输一次（“正面”请输入0,“反面”请输入1）：'))
    if toss == guess:
        print('你终于猜对了！')
    else:
        print('大失败！')


#》》------猜硬币游戏------
#》》猜一猜硬币是正面还是反面？
#》》请输入“0.正面”或“1.反面”：1
#》》猜对了！你真棒
#》》你终于猜对了！

#猜硬币小游戏第种二;
import random

all = ['正面','反面']
guess = ''

while guess not in all:
    print('------猜硬币游戏------')
    print('猜一猜硬币是正面还是反面？')
    guess = input('请输入“正面”或“反面”：')

toss = all[random.randint(0,1)]
# 随机抛硬币，all[0]取出正面，all[1]取出反面

if toss == guess:
    print('猜对了！你真棒')
else:
    print('没猜对，再给你一次机会。')
    guess = input('再输一次“正面”或“反面”：')
    if toss == guess:
        print('你终于猜对了！')
    else:
        print('大失败！')




#猜拳小游戏

import  random
#电脑
computer=str(random.randint(0,2))

#玩家
playter=input('请出拳:0--【石头】  1--【剪刀】 2--【布】')
print('电脑出的是:',computer)
print('玩家出的是:',playter)
#玩家获胜
if (playter=='0' and computer=='1') or (playter=='1' and computer=='2') or (playter=='2' and computer=='0'):
    print('玩家获胜')
#平局
elif playter==computer:
      print('平局')
#电脑获胜
else:
     print('电脑获胜')



#猜拳游戏函数版
import  random
def init():
    # 声明两个个全局变量
    global playter
    global computer

playter=input('请出拳:0--【石头】  1--【剪刀】 2--【布】')    #玩家出拳

def computer1():                                            #电脑出拳
    computer=str(random.randint(0,2))
    return computer
computer=computer1()

print('电脑出的是:',computer)
print('玩家出的是:',playter)

#玩家获胜
def punches():
    if (playter=='0' and computer=='1') or (playter=='1' and computer=='2') or (playter=='2' and computer=='0'):
        print('玩家获胜')
    elif playter==computer:
        print('平局')      #平局
    else:
        print('电脑获胜')   #电脑获胜

punches()




```
## 登录及菜单案例   
```

#自定义登录密码函数
def password():
    n=0
    while n<3:
        username = input("请输入用户名：")
        password = input("请输入密码：")
        if username == 'abc' and password == '123':
            print("登录成功")
            break
        else:
            n=n+1
            print("输入有误")
    else:
        print("你输错了三次，登录失败")
password()
#》》输入用户名：abc
#》》请输入密码：123
#》》登录成功



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


#练习22
def win():
    a=0
    while a <3:
        a+=1
        print('--------------- 第'+str(a)+'局WIN-----------------')
win()

print('=====================================================')
print('分割线')
print('=====================================================')
   
def win2():
    for i in range(3):
        print('--------------- 第'+str(i+1)+'局WIN-----------------')
win2()

#用for循环呢取出字典内容
movie = {
'妖猫传':['黄轩','染谷将太'],
'无问西东':['章子怡','王力宏','祖峰'],
'超时空同居':['雷佳音','佟丽娅'],
}

name = input('你想查询哪个演员？')
for i in movie:
    actors = movie[i]
    #取出字典的值
    if name in actors:
        print(name+'出演了电影'+i)



#格式化字符串
a='张山这小子和'
b='李四一起'
c='去买香烟'
print('{} {} {}'.format(a,b,c))
#》》张山这小子 和李四一起 去买香烟


#练习题:帮你做选择之我要吃什么?
import random 
def dbcai():
    dbcai={1:'锅包肉',2:'尖椒干豆腐',3:'大棒骨',4:'酱骨架',5:'酸菜白菜猪肉炖粉条',6:'小鸡炖蘑菇',7:'葱烧鲤鱼'} #菜单用字典
    for x1 in random.sample(dbcai.keys(),len(dbcai)):  #随机生成不重复的菜品
        v1=dbcai[x1]
        a1=input(v1+'选择Y,否则选择N:')
        if a1=='Y':
            print('您的选择是'+v1)
            break            
def xcai():
    xcai={1:'剁椒鱼头',2:'辣椒炒肉',3:'板栗烧鸡',4:'蒜香腊鸡腿',5:'麻辣小龙虾',6:'剁椒萝卜皮'}
    for x2 in random.sample(xcai.keys(),len(xcai)):
        v2=xcai[x2]
        a2=input(v2+'选择Y,否则选择N:')
        if a2=='Y':
            print('您的选择是'+v2)
            break
def chicai():
    chicai={1:'四川辣子鸡',2:'水煮面',3:'四川麻辣鸡',4:'干煸牛肉丝',5:'豆豉蒸排骨',6:'川味水煮鱼'}
    for x3 in random.sample(chicai.keys(),len(chicai)):
        v3=chicai[x3]
        a3=input(v3+'选择Y,否则选择N:')
        if a3=='Y':
            print('您的选择是'+v3)
            break
      
def main():
   
    while True:
        print('请选择饭店?:「1」大明东北菜馆;「2」毛家饭店湘菜馆;「3」辣不怕川菜馆')
        choice=input('请输入饭店名称(如果退出请按 N ):')
      
        if choice=='1':
            dbcai()
            print('感谢惠顾！欢迎您下次光临!')
            continue
        elif choice=='2':
            xcai()
            print('感谢惠顾！欢迎您下次光临!')
            continue
        elif choice=='3':
            chicai()
            print('感谢惠顾！欢迎您下次光临!')
            continue 
        elif choice=='N':
            print('感谢惠顾！欢迎您下次光临!')
            break 
        else:
            print('您输入有误,请重新输入')
            continue

main()

#第二种情况
# 练习题:帮你做选择之我要吃什么
import random

# 将需要用到的表格和变量放在开头
list_food = ['KFC', '蒸菜馆', '楼下快餐店', '桂林米粉', '东北饺子', '金牌猪脚饭', '三及第汤饭']  # 备选菜单，可自定义。
list_choice = []

# 由于两个原因都包含判断过程，所以，为了让代码更简洁，可将其封装成函数。
def choose(list):
    while True:
        food = random.choice(list)
        judgement = input('去吃【%s】好不好啊？同意的话输入y，不想吃直接回车即可。'%(food))
        if judgement == 'y':
            print('去吃【%s】！就这么愉快地决定啦！'%(food)) 
            break

# 判断环节
reason = int(input('你不知道吃什么的原因是：1.完全不知道吃什么；2.在几家店之间徘徊（请输入1或2）：'))
if reason == 1:
    choose(list_food)
elif reason == 2:
    add = True
    while add:
        choice = input('请输入让你犹豫的店名（注：一家一家输，完成后输入y）：')
        if choice != 'y':  # 这个判断语句，是为了不将 y 也添加到菜单里。
            list_choice.append(choice)
        if choice == 'y':
            add = False
    choose(list_choice)          
else:
    print('抱歉，目前还不支持第三种情况——不过，你可以加代码哦。')


#滾動屏幕廣告效果
import os, time

def main():  # 用函数封装，可复用性会高一些（可在其他的.py文件里调用该函数。）
    content = ' 我愛你董春華...'  # 广告词可自定义。
    while True:
        # linux/os x系统【清除屏幕】代码（线上使用本代码）
        os.system('clear')  # 清屏和打印结合起来，形成滚动效果。
        # windows系统【清除屏幕】代码
        '''
        os.system('cls') 
        '''
   
        content = content[1:] + content[0]
        print(content)# 这行代码相当于：将字符串中第一个元素移到了最后一个。
        time.sleep(0.25)  # 你可以改下时间，体会“循环周期”和“滚动速度”之间的关联。

if __name__ == '__main__':  # 类里面学到的检测方法，在函数中其实也可以用。
    main()



```
## 101例函数式编程测卦系统等   
```

#例题101：
lsg=['乾天刚建，自强不息','坤地方直，厚德载物','水积雷响，屯积助长','山下流水，启蒙德育','水在天上，需等饮食','天升水落，讼兴不争','地下藏水，师出有名','水漫于地，密交亲比','风行天上，小畜积雨','天下有泽，和悦慎履','地天相交，和谐通泰','天地相悖，闭塞成否','天火同燃，同人团结','火燃天上，大有收获','地中隐山，谨慎为谦','雷响于地，豫乐自警','泽中有雷，随机应变','山下有风，蛊惑横行','地高于泽，居高临下','风拂大地，遍观通达','火闪雷鸣，噬嗑威刑','山脚火焰，贲饰文美','高山附地，剥蚀去伪','地下雷鸣，刚阳复兴','天降暴雷，守道无妄','山中有天，大畜能容','山下有雷，养志颐情','泽淹风木，大过之征','习坎为水，守信克险','附离为火，柔顺亨通','泽山相应，咸感贞吉','雷响风行，识道守恒','天下藏山，退遁避险','雷震天上，识礼大壮','火出地上，晋升明德','地压潜火，明夷避祸','风熊火里，家人同乐','上火下泽，睽违少和','水漫山路，蹇滞艰难','雷鸣水降，解除旱象','高山低泽，损下益上','风激雷荡，益下损上','泽与天上，夬决坚刚','天下微风，阴生姤合','泽汇于地，萃英聚众','地平风扬，贤能萌升','泽中漏水，知困早悟','水盛风木，井收勿幕','泽中起火，改制旧革','火燃风木，鼎新之物','震雷压惊，反思内省','艮为山止，知止当止','风木依山，循序渐进','雷震泽上，归妹依礼','雷鸣火电，丰茂光明','火烧山外，旅途亨通','巽为风顺，大人齐物','兑为泽悦，修德和睦','风行水面，离析涣散','水溢泽岸，节制礼数','风吹泽面，中孚信诚','雷惊山上，小过无妨','水火相融，既济功成','火水离错，未济大江']
import random
input('请输入任意字符或回车')
a = random.choice(lsg)
for i in range(1,2):
    print(a)



#例题102初版：

import random
lsg1=['1','2','3','4','5','6','7','8']
a=random.choice(lsg1)
b=random.choice(lsg1)
mo={'乾为天（乾卦)自强不息':'11','坤为地（坤卦）厚德载物':'88','水雷屯（屯卦）起始维艰':'64','山水蒙（蒙卦）启蒙奋发':'76','水天需（需卦）守正待机':'61','天水讼（讼卦）慎争戒讼':'16','地水师（师卦）行险而顺':'86','水地比（比卦）诚信团结':'68','风天小畜（小畜卦）蓄养待进':'51','天泽履（履卦）脚踏实地':'12','地天泰（泰卦）应时而变':'81','天地否(pǐ)（否卦）不交不通':'18','天火同人（同人卦）上下和同':'13','火天大有（大有卦）顺天依时':'31','地山谦（谦卦）内高外低':'87','雷地豫（豫卦）顺时依势':'48','泽雷随（随卦）随时变通':'24','山风蛊（蛊卦）振疲起衰':'75','地泽临（临卦）教民保民':'82','风地观（观卦）观下瞻上':'58','火雷噬嗑（噬嗑卦）刚柔相济':'34','山火贲（贲卦）饰外扬质':'73','山地剥（剥卦）顺势而止':'78','地雷复（复卦）寓动于顺':'84','天雷无妄（无妄卦）无妄而得':'14','山天大畜（大畜卦）止而不止':'71','山雷颐（颐卦）纯正以养':'74','泽风大过（大过卦）非常行动':'25','坎为水（坎卦）行险用险':'66','离为火（离卦）附和依托':'33','泽山咸（咸卦）相互感应':'27','雷风恒（恒卦）恒心有成':'45','天山遁（遁卦）遁世救世':'17','雷天大壮（大壮卦）壮勿妄动':'41','火地晋（晋卦）求进发展':'38','地火明夷（明夷卦）晦而转明':'83','风火家人（家人卦）诚威治业':'53','火泽睽（睽卦）异中求同':'32','水山蹇（蹇卦）险阻在前':'67','雷水解（解卦）柔道致治':'46','山泽损（损卦）损益制衡':'72','风雷益（益卦）损上益下':'54','泽天夬（夬卦）决而能和':'21','天风姤（姤卦）天下有风':'16','泽地萃（萃卦）荟萃聚集':'28','地风升（升卦）柔顺谦虚':'85','泽水困（困卦）困境求通':'26','水风井（井卦）求贤若渴':'65','泽火革（革卦）顺天应人':'23','火风鼎（鼎卦）稳重图变':'35','震为雷（震卦）临危不乱':'44','艮为山（艮卦）动静适时':'77','风山渐（渐卦）渐进蓄德':'58','雷泽归妹（归妹卦）立家兴业':'42','雷火丰（丰卦）日中则斜':'43','火山旅（旅卦）依义顺时':'37','巽为风（巽卦）谦逊受益':'55','兑为泽（泽卦）刚内柔外':'22','风水涣（涣卦）拯救涣散':'56','水泽节（节卦）万物有节':'62','风泽中孚（中孚卦）诚信立身':'52','雷山小过（小过卦）行动有度':'47','水火既济（既济卦）盛极将衰':'63','火水未济（未济卦）事业未竟':'36'}
name =a+b
for i in mo:
    ac=mo[i]
    if name in ac:
        print('['+name+'卦像]:'+i)

  





#例题函数式103第二次升级版：
import random
def zylsg():
    lsg1=['1','2','3','4','5','6','7','8']
    a=random.choice(lsg1)
    b=random.choice(lsg1)
    name=a+b
    mo={'乾为天（乾卦)自强不息':'11','坤为地（坤卦）厚德载物':'88','水雷屯（屯卦）起始维艰':'64','山水蒙（蒙卦）启蒙奋发':'76','水天需（需卦）守正待机':'61','天水讼（讼卦）慎争戒讼':'16','地水师（师卦）行险而顺':'86','水地比（比卦）诚信团结':'68','风天小畜（小畜卦）蓄养待进':'51','天泽履（履卦）脚踏实地':'12','地天泰（泰卦）应时而变':'81','天地否(pǐ)（否卦）不交不通':'18','天火同人（同人卦）上下和同':'13','火天大有（大有卦）顺天依时':'31','地山谦（谦卦）内高外低':'87','雷地豫（豫卦）顺时依势':'48','泽雷随（随卦）随时变通':'24','山风蛊（蛊卦）振疲起衰':'75','地泽临（临卦）教民保民':'82','风地观（观卦）观下瞻上':'58','火雷噬嗑（噬嗑卦）刚柔相济':'34','山火贲（贲卦）饰外扬质':'73','山地剥（剥卦）顺势而止':'78','地雷复（复卦）寓动于顺':'84','天雷无妄（无妄卦）无妄而得':'14','山天大畜（大畜卦）止而不止':'71','山雷颐（颐卦）纯正以养':'74','泽风大过（大过卦）非常行动':'25','坎为水（坎卦）行险用险':'66','离为火（离卦）附和依托':'33','泽山咸（咸卦）相互感应':'27','雷风恒（恒卦）恒心有成':'45','天山遁（遁卦）遁世救世':'17','雷天大壮（大壮卦）壮勿妄动':'41','火地晋（晋卦）求进发展':'38','地火明夷（明夷卦）晦而转明':'83','风火家人（家人卦）诚威治业':'53','火泽睽（睽卦）异中求同':'32','水山蹇（蹇卦）险阻在前':'67','雷水解（解卦）柔道致治':'46','山泽损（损卦）损益制衡':'72','风雷益（益卦）损上益下':'54','泽天夬（夬卦）决而能和':'21','天风姤（姤卦）天下有风':'16','泽地萃（萃卦）荟萃聚集':'28','地风升（升卦）柔顺谦虚':'85','泽水困（困卦）困境求通':'26','水风井（井卦）求贤若渴':'65','泽火革（革卦）顺天应人':'23','火风鼎（鼎卦）稳重图变':'35','震为雷（震卦）临危不乱':'44','艮为山（艮卦）动静适时':'77','风山渐（渐卦）渐进蓄德':'58','雷泽归妹（归妹卦）立家兴业':'42','雷火丰（丰卦）日中则斜':'43','火山旅（旅卦）依义顺时':'37','巽为风（巽卦）谦逊受益':'55','兑为泽（泽卦）刚内柔外':'22','风水涣（涣卦）拯救涣散':'56','水泽节（节卦）万物有节':'62','风泽中孚（中孚卦）诚信立身':'52','雷山小过（小过卦）行动有度':'47','水火既济（既济卦）盛极将衰':'63','火水未济（未济卦）事业未竟':'36'}
    for i in mo:
        ac=mo[i]
        if name in ac:
            print('['+name+'卦像]:'+i)
            print('继续请选择')
        
def main():
    for i in range(6):
        shuru=input('请输入数字1测卦，否者选q:')
        if shuru=='1':
            zylsg()
        elif  shuru in ['q','Q','Quit','quit']:
            print("下次再会~\n")
            break
        else:
            print('你输入的有误，请重新输入')
    
main()


#函数式103第3次升级版本：
import random
def zylsg():
    code = ''
    for i in range(6):
        c = str(random.randint(0,1))
        b = random.choice(c)
        code += b
    mo={'乾为天（乾卦)自强不息':'111111','坤为地（坤卦）厚德载物':'000000','水雷屯（屯卦）起始维艰':'010001','山水蒙（蒙卦）启蒙奋发':'100010','水天需（需卦）守正待机':'010111','天水讼（讼卦）慎争戒讼':'111010','地水师（师卦）行险而顺':'000010','水地比（比卦）诚信团结':'010000','风天小畜（小畜卦）蓄养待进':'110111','天泽履（履卦）脚踏实地':'111011','地天泰（泰卦）应时而变':'000111','天地否(pǐ)（否卦）不交不通':'111000','天火同人（同人卦）上下和同':'111101','火天大有（大有卦）顺天依时':'101111','地山谦（谦卦）内高外低':'000100','雷地豫（豫卦）顺时依势':'001000','泽雷随（随卦）随时变通':'011001','山风蛊（蛊卦）振疲起衰':'100110','地泽临（临卦）教民保民':'000011','风地观（观卦）观下瞻上':'110000','火雷噬嗑（噬嗑卦）刚柔相济':'101001','山火贲（贲卦）饰外扬质':'100101','山地剥（剥卦）顺势而止':'100000','地雷复（复卦）寓动于顺':'000001','天雷无妄（无妄卦）无妄而得':'111001','山天大畜（大畜卦）止而不止':'100111','山雷颐（颐卦）纯正以养':'100001','泽风大过（大过卦）非常行动':'011110','坎为水（坎卦）行险用险':'010010','离为火（离卦）附和依托':'101101','泽山咸（咸卦）相互感应':'011100','雷风恒（恒卦）恒心有成':'001110','天山遁（遁卦）遁世救世':'111100','雷天大壮（大壮卦）壮勿妄动':'001111','火地晋（晋卦）求进发展':'101000','地火明夷（明夷卦）晦而转明':'000101','风火家人（家人卦）诚威治业':'110101','火泽睽（睽卦）异中求同':'101011','水山蹇（蹇卦）险阻在前':'010100','雷水解（解卦）柔道致治':'001010','山泽损（损卦）损益制衡':'100011','风雷益（益卦）损上益下':'110001','泽天夬（夬卦）决而能和':'011111','天风姤（姤卦）天下有风':'111010','泽地萃（萃卦）荟萃聚集':'011000','地风升（升卦）柔顺谦虚':'000110','泽水困（困卦）困境求通':'011010','水风井（井卦）求贤若渴':'010110','泽火革（革卦）顺天应人':'011101','火风鼎（鼎卦）稳重图变':'101110','震为雷（震卦）临危不乱':'001001','艮为山（艮卦）动静适时':'100100','风山渐（渐卦）渐进蓄德':'110000','雷泽归妹（归妹卦）立家兴业':'001011','雷火丰（丰卦）日中则斜':'001101','火山旅（旅卦）依义顺时':'101100','巽为风（巽卦）谦逊受益':'110110','兑为泽（泽卦）刚内柔外':'011011','风水涣（涣卦）拯救涣散':'110010','水泽节（节卦）万物有节':'010011','风泽中孚（中孚卦）诚信立身':'110011','雷山小过（小过卦）行动有度':'001100','水火既济（既济卦）盛极将衰':'010101','火水未济（未济卦）事业未竟':'101010'}
    for i in mo:
        ac=mo[i]
        if code in ac:
            print('['+code+'卦像]:'+i)
            print('继续请选择')
        
def main():
    for i in range(6):
        shuru=input('请输入数字1测卦，否者选q:')
        if shuru=='1':
            zylsg()
        elif  shuru in ['q','Q','Quit','quit']:
            print("下次再会~\n")
            break
        else:
            print('你输入的有误，请重新输入')
main()


#函数式104第4次升级版本20230303最终版：
import random

def get_trigram():
    trigram = []
    for i in range(3):
        coin_tosses = [random.randint(0, 1) for _ in range(3)]
        trigram.append(sum(coin_tosses) % 2)
    return trigram

def get_hexagram():
    lower_trigram = get_trigram()
    upper_trigram = get_trigram()
    return upper_trigram + lower_trigram




def main_hexagram():
    hexagram = get_hexagram()
    result = ''.join(map(str, hexagram))
    exp_hexagram={'乾为天（乾卦)自强不息':'111111','坤为地（坤卦）厚德载物':'000000','水雷屯（屯卦）起始维艰':'010001','山水蒙（蒙卦）启蒙奋发':'100010','水天需（需卦）守正待机':'010111','天水讼（讼卦）慎争戒讼':'111010','地水师（师卦）行险而顺':'000010','水地比（比卦）诚信团结':'010000','风天小畜（小畜卦）蓄养待进':'110111','天泽履（履卦）脚踏实地':'111011','地天泰（泰卦）应时而变':'000111','天地否(pǐ)（否卦）不交不通':'111000','天火同人（同人卦）上下和同':'111101','火天大有（大有卦）顺天依时':'101111','地山谦（谦卦）内高外低':'000100','雷地豫（豫卦）顺时依势':'001000','泽雷随（随卦）随时变通':'011001','山风蛊（蛊卦）振疲起衰':'100110','地泽临（临卦）教民保民':'000011','风地观（观卦）观下瞻上':'110000','火雷噬嗑（噬嗑卦）刚柔相济':'101001','山火贲（贲卦）饰外扬质':'100101','山地剥（剥卦）顺势而止':'100000','地雷复（复卦）寓动于顺':'000001','天雷无妄（无妄卦）无妄而得':'111001','山天大畜（大畜卦）止而不止':'100111','山雷颐（颐卦）纯正以养':'100001','泽风大过（大过卦）非常行动':'011110','坎为水（坎卦）行险用险':'010010','离为火（离卦）附和依托':'101101','泽山咸（咸卦）相互感应':'011100','雷风恒（恒卦）恒心有成':'001110','天山遁（遁卦）遁世救世':'111100','雷天大壮（大壮卦）壮勿妄动':'001111','火地晋（晋卦）求进发展':'101000','地火明夷（明夷卦）晦而转明':'000101','风火家人（家人卦）诚威治业':'110101','火泽睽（睽卦）异中求同':'101011','水山蹇（蹇卦）险阻在前':'010100','雷水解（解卦）柔道致治':'001010','山泽损（损卦）损益制衡':'100011','风雷益（益卦）损上益下':'110001','泽天夬（夬卦）决而能和':'011111','天风姤（姤卦）天下有风':'111010','泽地萃（萃卦）荟萃聚集':'011000','地风升（升卦）柔顺谦虚':'000110','泽水困（困卦）困境求通':'011010','水风井（井卦）求贤若渴':'010110','泽火革（革卦）顺天应人':'011101','火风鼎（鼎卦）稳重图变':'101110','震为雷（震卦）临危不乱':'001001','艮为山（艮卦）动静适时':'100100','风山渐（渐卦）渐进蓄德':'110000','雷泽归妹（归妹卦）立家兴业':'001011','雷火丰（丰卦）日中则斜':'001101','火山旅（旅卦）依义顺时':'101100','巽为风（巽卦）谦逊受益':'110110','兑为泽（泽卦）刚内柔外':'011011','风水涣（涣卦）拯救涣散':'110010','水泽节（节卦）万物有节':'010011','风泽中孚（中孚卦）诚信立身':'110011','雷山小过（小过卦）行动有度':'001100','水火既济（既济卦）盛极将衰':'010101','火水未济（未济卦）事业未竟':'101010'}
    for  key, value in exp_hexagram.items():
            if value==result:
                print(value+'卦辞为：'+key)
                print('继续请选择')


def main():
    for i in range(6):
        hex_inp=input('请输入数字1测卦，否者选q:')
        if hex_inp=='1':
            main_hexagram()

        elif  shuru in ['q','Q','Quit','quit']:
            print("下次再会~\n")
        #break
        else:
            print('你输入的有误，请重新输入')
main()





```
## 类的练习,借书系统及超级便签   
```

#类的练习,借书系统:
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

    authors = []
    def __init__(self):
        book1 = Book('撒哈拉的故事','三毛','我每想你一次，天上便落下一粒沙，从此便有了撒哈拉。')
        book2 = Book('梦里花落知多少','三毛','人人都曾拥有荷西，虽然他终会离去。')
        book3 = Book('月亮与六便士','毛姆','满地都是六便士，他却抬头看见了月亮。')
        self.books = [book1,book2,book3]
        self.authors.append(book1.author)
        self.authors.append(book2.author)
        self.authors.append(book3.author)
 
    def menu(self):
        while True:
            print('1.查询书籍')
            choice = int(input('请输入数字选择对应的功能：'))
            if choice == 1:
                self.show_author_book()
            else:
                print('感谢使用！')
                break
 
    def show_author_book(self):
        author = input('请输入想查询作家的名称：')
        if author in self.authors:
            print(author + '的作品有：')
            for book in self.books:
                if book.author == author:
                    print(book)
        else:
            print('很可惜，我们暂时没有收录这位作者的作品')

manager = BookManager()
manager.menu()            
'''
一个思路：
1. 先用条件判断语句判断该作者在不在列表authors里，如果不在就打印'很可惜，我们暂时没有收录这位作者的作品'
2. 如果在，就遍历列表books的每个实例，当实例属性author与输入的作者名相等，就打印该实例      
'''





#练习 超级便捷:

class List:
 
    def __init__(self, number, item,status):
        self.number = number
        self.item = item
        self.status= status
       

 
    def __str__(self):
        return '序号：「%s」 事项：%s 重要等级：%s' % (self.number,self.item,self.status)

class ListManager:

    lists = []
    def __init__(self):
        list1 = List('ID','今日事项','级别')
        self.lists.append(list1)
    
 
    def menu(self):
        print('欢迎使用超级便笺系统，希望你有缘，为精神家园找到一片栖息地。\n')
        while True:
            print('1.查询所有便笺\n2.添加便笺\n3.清空所有\n4.退出系统\n')
            choice = int(input('请输入数字选择对应的功能：'))
            if choice == 1:
                self.show_all_list()
            elif choice == 2:
                self.add_list()
            elif choice == 3:
                self.return_list()
            elif choice == 4:
                print('感谢使用！愿你我成为好朋友，在茫茫人海里相遇。')
                break
 
    def show_all_list(self):
        print('便笺信息如下：')
        for list in self.lists:
            print(list)
            print('')

    def add_list(self):
        new_number = input('请输入序列号：')
        new_item = input('请输入事项内容：')
        new_status=  input('请输入重要等级：')
       
        new_list = List(new_number, new_item,new_status)
        self.lists.append(new_list)
        print('便笺录入成功！\n')

    def check_list(self,number):
        for list in self.lists:
            if list.number == number:
                 return list 
        else:
            return None
        
    def return_list(self):
        number = input('请输入序列号：')
        res = self.check_list(number)
        # 调用check_list方法，将返回值赋值给变量res

        if res == None:
        # 如果返回的是空值，即这本书的书名不在系统里

            print('没有这个序列号，您恐怕输错了～')
        else:
        # 如果返回的是实例对象

            for number in self.lists:
                self.lists.clear()
                
                print('已经清全部空便笺记录！')
            else:
           
                print('欢迎您继续添加新的便笺！')
        

   
 
manager = ListManager()
manager.menu()


```
## 背单词案例   
```


#50行代码背单词


import random


# 存放单词的列表(可以自己填写需要背诵的单词)
words = ['print', 'int','str','len', 'input', 'format', 'if','for','def']

#初始化信息↓↓↓↓↓↓↓
def init():
    # 声明三个全局变量
    global word
    global tips
    global ranList

    #随机获取单词列表里的一个单词
    word = list(words[random.randint(0, len(words) - 1)])

    #随机数列表，存放着与单词长度一致的随机数（不重复）
    ranList = random.sample(range(0, len(word)), len(word))

    #存放提示信息
    tips = list()
    #初始化提示信息
    #存放跟单词长度一致的下划线
    for i in range(len(word)):
        tips.append(_)
    #随机提示两个字母
    tips[ranList[0]] = word[ranList[0]]
    tips[ranList[1]] = word[ranList[1]]

#函数部分↓↓↓↓↓

#展示菜单
def showMenu():
    print('需要提示请输入?')
    print('结束游戏请输入quit!')


#显示提示信息
def showtips():
    for i in tips:
        print(i, end='' )
    print(i)


#需要提示
def needTips(tipsSize):
    #至少有两个未知字母
    if tipsSize <= len(word)-3:
        tips[ranList[tipsSize]] = word[ranList[tipsSize]]
        tipsSize += 1
        return tipsSize
    else:
        print('已没有提示!')


#主要运行函数↓↓↓↓↓↓
def run():
    print('------python关键字版本-------')
    init()
    tipsSize = 2
    showMenu()
    
    while True:
        print('提示：',end='')
        showtips()
        guessWord = input('猜一下这个单词：')
        # ''.join(word)>把word列表的内容转换成字符串
        if guessWord == ''.join(word):
            print('恭喜你，猜对了！','就是%s!'%(''.join(word)))
            print('再猜一次')
            init()
            
        elif guessWord == '?':
            tipsSize = needTips(tipsSize)
        elif guessWord == 'quit!':
            break
        else:
            print('猜错了！')
            continue
run()


#随机背单词立例题二:
import random as t
#创建单词序列
words=("easy","difficult","answer","continue")
zi=("容易","困难","回答","继续")
hanzi={ "easy":"容易", "difficult":"困难","answer":"回答", "continue":"继续","blue":"蓝色"}
yin={"容易":"easy","困难":"difficult","回答":"answer","继续":"continue","蓝色":"blue"}
def jiemian():
    print("""
                     欢迎来到背单词
        根据English回答汉语或者根据汉语回答English
        -------------------------------------------
                    1.English——>汉语
                    
                    2.汉语——>English
                    
                    3.单词列表
                    
                    4.退出系统
""")
#######Zhang######  English——>汉语   ################################
    
def yyihan(): 
    n=0
    m=0
    su=0
    iscontinue="y"
    while iscontinue=="y" or iscontinue=="Y":
        word=t.choice(words)
        print("随机生成在单词:")
        print(">------>   "+word)
        guess=input("\n输入汉语: ").strip()# 防止用户误操作录入空白
        while guess!=hanzi[word]:
            print("对不起，不正确。")
            n=n+1
            print('\n——>正确率：%.2f'%(m/(n+m)))
            guess=input("继续输入：").strip()
        if guess==hanzi[word]:
             print("真棒！答对了！！")
             m=m+1
             print('\n——>正确率：%.2f'%(m/(n+m)))
        iscontinue=input("\nn\是否继续（Y/N）：")
        
###############  汉语——>English   #########wei####################

def hanyiy():
    n=0;
    m=0;
    su=0;
    iscontinue="y"
    while iscontinue=="y" or iscontinue=="Y":
        hz=t.choice(zi)
        print("随机生成在汉语:")
        print(">------>   "+hz)
        guess=input("\n输入Ehglish: ").strip()
        while guess!=yin[hz]:
            print("对不起，不正确。")
            n=n+1
            print('\n——>正确率：%.2f'%(m/(n+m)))
            guess=input("继续输入：").strip()
        if guess==yin[hz]:
            print("真棒！答对了！！")
            m=m+1
            print('\n——>正确率：%.2f'%(m/(n+m)))
        iscontinue=input("\nn\是否继续（Y/N）：")

####bu##########################################################

def lib():
    print("************************")
    print("\n")
    for i in range (len(words)):
        print(words[i],"   ",zi[i],"\n")
    print("\n")
    print("************************")
    a=input("输入 1 背诵单词结束——>: ")


###################################################################
        
while True:
    jiemian()
    a=int(input("\n\n\n\选择需要进行的操作（1、2、3、4）："))
    if(a==1):
        yyihan()
    elif a==2:
        hanyiy()
    elif a==3:
        lib()
    elif a==4:
        exit()
    else:
        print("输入格式错误，重新输入！！")




```
## 纸牌游戏案例   
```

import  random
#print(f'幻影来到《十一点》游戏场地'.center(100，'-'))


poke_num_list=[i for i in range(1,14)]
poke_color_list=['黑桃','红桃','方块','梅花']
total_poke_list=[[color,num] for num in poke_num_list for color in poke_color_list]+[['小王',14],['大王',15]]
print(total_poke_list)
print(f'洗牌'.center(100,'='))
random.shuffle(total_poke_list)
print(total_poke_list)

print(f'欢迎来到《十一点》游戏场地'.center(100,'-'))   
while True:
    count=input('请输入参与游戏人数：')
    if not count.isdecimal():
        print('输入的必须是纯数字，兄弟！！')
        continue
    
    user_count=int(count)
    print('参与的人数是{}'.format(user_count))
    if user_count<1:
        print('参与人数必须大于1，你这个二货！！')
        continue
    break

total_user_score={}

for i in range(1,user_count+1):
    print(user_count)
          
    random_index=random.randint(0,len(total_poke_list)-1)
    card=total_poke_list.pop(random_index)
    score=0
    value=0.5 if card[1]>10 else card[1]
    
    score+=value
    print(f'给用户{i}发的牌是{card}得分情况是:{score}')
    
    while True:
        choice=input('您是否还继续要牌：(Y/N)'.upper())
        if choice not in {'Y','N'}:
            print('你这个大笨蛋，你能好好输入吗？只能是Y或N')
            continue
        if choice=='N':
            print('本帅哥不要了，88！！')
            break
        random_index=random.randint(0,len(total_poke_list)-1)
        card=total_poke_list.pop(random_index)
        value=0.5 if card[1]>10 else card[1]
        score+=value  
        print(f'给用户{i}发的牌是{card}得分情况是:{score}')
        if score>11:
            print('您经超过11点，回家洗洗睡吧，我要裂开了'.center(60,'—'))
            score=0
            break
    total_user_score[f'用户{i}']=score
    print(total_user_score)
   



```
## 员工抽奖案例及 数据库版便笺   
```
#幸运员工

import  random
user_list=[f'幸运员工{i}' for i in range(1,31)]
print(user_list)
bonuns_list=[['三等奖 笔记本一个',3],['二等奖 50元红包一个',2],['一等奖 笔记本一个',1]]
for text,count in bonuns_list:
   winner_list=random.sample(user_list,count)
for user in winner_list:
    user_list.remove(user)
print(f'赢家是:{winner_list}'.center(86,'*'))
print(f'奖品是:{text},赢家是:{winner_list}')

print(92*'*')



#幸运员工开奖另一种写法

import  random
staff_list=[]
for i in range (1,301):
    staff_list.append(f'员工{i}')

print(staff_list)
print('+'*151)
level=[30,6,3]
count=0

for j in range(3):
    winnList=random.sample(staff_list,level[j])
   
    count+=1
    for winner in winnList:
        staff_list.remove(winner)
    print(f'获得{3-j}等奖的员工是:{winnList}')
    print(f'还剩{(len(staff_list))}个未中奖')




#ChatGPT源代码
import os
import openai

openai.api_key =' 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'
start_sequence='\nA:'
restart_requence='\n\nQ:'
restart_requence='\n\nQ:'
while 1==1:
  prompt=input(restart_requence)
  if prompt=='quit':
    break
  else:
    response = openai.Completion.create(
      model="text-davinci-003",
      prompt=prompt,
      temperature=0.7,
      max_tokens=256,
      top_p=1,
      frequency_penalty=0,
      presence_penalty=0
    )
    print(response['choices'][0]['text'].strip())


#ChatYuan源码
import clueai
# initialize the Clueai Client with an API Key
cl = clueai.Client('gUf5Yh-WXUluN3YE-hC38101001011011', check_api_key=True)
start_sequence='\nA:'
restart_requence='\n\nQ:'
restart_requence='\n\nQ:'
while 1==1:
  prompt=input(restart_requence)
  if prompt=='quit':
    break
  else:
    response =cl.generate(
            model_name='ChatYuan-large',
            prompt=prompt)
    print('元语Ai: {}'.format(response.generations[0].text)) 




#超级行事历初版本

import sys
import time
#reload(sys)
#sys.setdefaultencoding('utf-8')


class List():
    #number=0
 
   # def __init__(self):
    #    self.Supercal_list=[]
   #     self.Suoercal_dict={}
      
    #定义行事属性，初始化方法
    def __init__(self,date,item,content,status):
        self.date = date
        self.item = item
        self.content=content
        self.status= status
        #Supercal.number=Supercal.number+1

    def __str__(self):
        return "Date:{}.Item:{}.Content:{}.Status".format(self.date,self.item,self.content,self.status)


class Supercal():
    def __init__(self):
        self.Supercal_list=[]
        self.Suoercal_dict={}

    #定义行事历菜单
    def menu(self):
        print('欢迎使用超级行事历系统，希望你有缘，为精神家园找到一片栖息地。\n')
        while True:
            print('1.查询所有行事历\n2.添加行事历\n3.修改行事历\n4.保存事历\n5.退出系统\n')
            choice = int(input('请输入数字选择对应的功能：'))
            if choice == 1:
                #self.show()
                self.read_file()
                self.show()
            elif choice == 2:
                self.add()

            elif choice == 3:
                self.return_list()
            elif choice == 4:
                self.add_file()
            elif choice == 5:
                print('感谢使用！愿你我成为好朋友，在茫茫人海里相遇。')
                break



    #添加行事历
    def add(self):
        date=input("请输入日期:")
        item=input("请输入事项类别:")
        content=input("请输入具体内容:")
        status=input("请输入重要等级:")
    
 
        self.Supercal_dict1={"date":date,"item":item,"content":content,"status":status}
 
        self.Supercal_list.append(self.Supercal_dict1)
        print()
        print("-----添加行事历信息界面-----")
        print()
        print("日期\t\t","事项\t\t","内容\t\t\t\t","等级\t\t")
        for Supercal_dict_1 in self.Supercal_list:
            print("%s\t\t%s\t\t%s\t\t\t\t%s\t\t" %(Supercal_dict_1["date"],
                                                   Supercal_dict_1["item"],
                                                Supercal_dict_1["content"],
                                                 Supercal_dict_1["status"],))
        print()
        print("录入成功!")
        print()

    #staticmethod
    def show(self):
        list1=self.Supercal_list
        print()
        print("-----行事历信息界面-----")
        print()
        print("日期\t\t","事项\t\t","内容\t\t\t\t","等级\t\t")
        for list1 in self.Supercal_list:
            print("%s\t\t%s\t\t%s\t\t\t\t%s\t\t" %(list1["date"],
                                                   list1["item"],
                                                   list1["content"],
                                                   list1["status"],))
        print()
        print("查询行事历成功!")
        print()
        #print('行事历息如下：')
        #print("Date:{}.Item:{}.Content:{}.Status".format(self.date,self.item,self.content,self.status))


        
 
    #保存数据至文件中
    def save_file(self):
 
        f = open("Supercal2.txt", 'a', encoding='utf-8')
        f.write(str(self.Supercal_list))
        f.close()
        print("数据保存至Supercal2.txt文件成功！")


    #新增加数据至文件中
    def add_file(self):
        filename='Supercal2.txt'
        with open(filename,'r+', encoding='utf-8') as f:
            content=f.read()
            if content:
                f.write('\n'+str(self.Supercal_list))







#list1.append(['aa', 'bb'])
#print(list1) 


 
    #将数据读取至变量中
    def read_file(self):
 
         #if os.path.exists('Supercal2.txt'):
        f = open('Supercal2.txt', 'r', encoding='utf-8')
        ret = f.read()
 
        self.Supercal_list=eval(ret)
        f.close()
        print("数据读取成功!")
  
manager = Supercal()
manager.menu()


#第二版修改后

import sys
import time
import os
#reload(sys)
#sys.setdefaultencoding('utf-8')


class List():
    #number=0
 
   # def __init__(self):
    #    self.Supercal_list=[]
   #     self.Suoercal_dict={}
      
    #定义行事属性，初始化方法
    def __init__(self,date,item,content,status):
        self.date = date
        self.item = item
        self.content=content
        self.status= status
        #Supercal.number=Supercal.number+1

   # def __str__(self):
    #    return "Date:{}.Item:{}.Content:{}.Status".format(self.date,self.item,self.content,self.status)

class Supercal():
    def __init__(self):
        self.Supercal_list=[]
        self.Suoercal_dict={}

    #定义行事历菜单
    def menu(self):
        print('欢迎使用超级行事历系统，希望你有缘为精神家园找到一片栖息地！\n')
        while True:
            #print('1.查询所有行事历\n2.添加行事历\n3.清除行事历\n4.保存行事历\n5.添加行事历\n6.退出系统\n')
            print("-------------------------------")
            print("         行事历系统 V2.0"        )
            print("                             ")
            print("         1:查询行事历"            )
            print("         2:写入行事历"            )
            print("         3:增加行事历"            )
            print("         4:清除行事历"            )
            print("         5:保存行事历"          )
            print("         6:退出系统"            )
            print("                           ")
            print("-------------------------------")
            choice = int(input('请输入您的选择：'))
            if choice == 1:
                #self.show()
                self.read_file()
                self.show()
            elif choice == 2:
                self.add()
            elif choice == 3:
                 self.add_file()
            elif choice == 4:
                 self.dell_file()
            elif choice == 5:
                self.save_file()
            elif choice == 6:
                print('感谢使用！愿你我成为好朋友，在茫茫人海里相遇。')
                break

    #添加行事历
    def add(self):
        date=input("请输入日期:")
        item=input("请输入事项类别:")
        content=input("请输入具体内容:")
        status=input("请输入重要等级:")
        self.Supercal_dict1={"date":date,"item":item,"content":content,"status":status}
        self.Supercal_list.append(self.Supercal_dict1)
        print()
        print("-----添加行事历信息界面-----")
        print()
        print("日期\t\t","事项\t\t","内容\t\t\t\t","等级\t\t")
        for Supercal_dict_1 in self.Supercal_list:
            print("%s\t\t%s\t\t%s\t\t\t\t%s\t\t" %(Supercal_dict_1["date"],
                                                   Supercal_dict_1["item"],
                                                Supercal_dict_1["content"],
                                                 Supercal_dict_1["status"],))
        print()
        print("录入成功!")
        print()

    #staticmethod
    def show(self):
        list1=self.Supercal_list
        print()
        print("-----行事历信息界面-----")
        print()
        print("日期\t\t","事项\t\t","内容\t\t\t\t","等级\t\t")
        for list1 in self.Supercal_list:
            print("%s\t\t%s\t\t%s\t\t\t\t%s\t\t" %(list1["date"],
                                                   list1["item"],
                                                   list1["content"],
                                                   list1["status"],))
        print()
        print("查询行事历成功!")
        print()
        #print('行事历息如下：')
        #print("Date:{}.Item:{}.Content:{}.Status".format(self.date,self.item,self.content,self.status))


    #保存数据至文件中
    def save_file(self):
        f = open("Supercal2.txt", 'w+', encoding='utf-8')
        f.write(str(self.Supercal_list))
        f.close()
 
        #f = open("Supercal2.txt", 'a', encoding='utf-8')
       # f.write(str(self.Supercal_list))
        #f.close()
        print("数据保存至Supercal2.txt文件成功！")


    #新增加数据至文件中
    def add_file(self):
        self.add()
        self.save_file()
    
    def dell_file(self):
        os.remove("Supercal2.txt")
        print("File removed successfully")

#list1.append(['aa', 'bb'])
#print(list1) 

    #将数据读取至变量中
    def read_file(self):
 
         #if os.path.exists('Supercal2.txt'):
        f = open('Supercal2.txt', 'r', encoding='utf-8')
        ret = f.read()
 
        self.Supercal_list=eval(ret)
        f.close()
        print("数据读取成功!")
  
manager = Supercal()
manager.menu()



```
## 炸金花游戏示例   
```


import random
def alex():
    poke_types=['♥','♠','♣','♦']
    poke_nums=[2,3,4,5,6,7,8,9,10,'J','Q','K','A']
    poke_list=[]
    for p_type in poke_types:
        count=2
        for p_num in poke_nums:
            card=[f'{p_type}{p_num}',count]
            poke_list.append(card)
            count+=1
    #print(poke_list)
    return poke_list
pokeList=alex()
print(pokeList)

#发牌
players=['Man','忙里偷闲','龙哥','平安']
def blackGirl(pl,pk,pn):
    player_dic={}
    for p_name in pl:
        p_cards=random.sample(pk,pn)
        for card in p_cards:
            pk.remove(card)
        player_dic[p_name]=p_cards
        print(f"为玩家【{p_name}】生成了牌：{p_cards}")
    return player_dic


print('^'*125)
playerDic=blackGirl(players,pokeList,3)
#print(playerDic)

#冒泡排序
def sortList(dataList):
    length=len(dataList)
    for i in range(length):
        for j in range(length-i-1):
            if dataList[j][1]>dataList[j+1][1]:
                dataList[j],dataList[j+1]=dataList[j+1],dataList[j]
    return dataList


#计算单牌得分
def calculate_single(p_cards,score):
    #初始化得分
    score=0
    p_cards=sortList(p_cards)
#计算
    weight_val=[0.1,1,10]
    count=0
    for card in p_cards:
        score+=card[1]*weight_val[count]
        count+=1
    print(f"计算单牌的结果是：{score}")
    return score 
print('&'*125)


#计算对子
def calculate_pair(p_cards,score):
    p_cards=sortList(p_cards)
    card_val=[i[1] for i in p_cards]
    if len(set(card_val))==2:
        if card_val[0]==card_val[1]:
            score=(card_val[0]+card_val[1])*50+card_val[2]   #aab
        else: #abb
            score=(card_val[1]+card_val[2])*50+card_val[0] 
    print(f"计算对子的结果是：{score}")
    return score

#顺子
def calculate_straight(p_cards,score):
   
    p_cards=sortList(p_cards)
    card_val=[i[1] for i in p_cards]
    a,b,c = card_val
    if b-a == 1 and c-b == 1:
        score*=100
    print(f"计算顺子的结果是：{score}") 
    return score


#同花
def calculate_same_color(p_cards,score):
   
    color_val = [i[0] for i in p_cards]
    if len(set(color_val)) == 1:
        score*=1000
    print(f"计算同花的结果是：{score}")
    return score


#同花顺
def calculate_same_color_straight(p_cards,score):
   
   #同花
    color_val = [i[0] for i in p_cards]
    if len(set(color_val)) == 1:
    #顺子
        p_cards=sortList(p_cards)
        card_val=[i[1] for i in p_cards]
        a,b,c = card_val
        if b-a == 1 and c-b == 1:
            score*=10000
    print(f"计算同花顺的结果是：{score}")
    return score

#豹子
def calculate_leopard(p_cards,score):
    card_val = {i[1] for i in p_cards}
    if len(card_val) == 1:
        score*=100000
    print(f"计算豹子结果是：{score}")
    return score

## 比对逻辑
calc_fun_orders = [
    calculate_single,
    calculate_pair,
    calculate_straight,
    calculate_same_color,
    calculate_same_color_straight,
    calculate_leopard
]

player_score = []   # 需要提前定义列表
for p_name, p_cards in playerDic.items():
    print(f"开始计算玩家【{p_name}】的牌：{p_cards}")
    score = 0
    for calc_func in calc_fun_orders:
        score = calc_func(p_cards,score)  # 移除不必要的score参数
    player_score.append([p_name, score])  # 添加计算结果到列表中

winner = sortList(player_score)[-1]
print(f"恭喜最后获胜的玩家是:【{winner[0]}】,得分是：{winner[1]}")



#行事历更新数据库版本
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
        db.close

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
    db.close

# 定义删除功能函数
def delete_data(sequence_number):
    with shelve.open('my_supercal') as db:
        mydate = db['cal']
        for i, item in enumerate(mydate):
            if item['sequence_number']==str(sequence_number):
                mydate.pop(i)
                db['cal']=mydate
        #print(mydate)
        db.close
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

# 关闭shelve文件
    db.close()

    

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
    db.close

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
        elif hoice == 6:
            print("感谢使用！")
            break
# 主程序
while True:
    menu()




```
## 线程池及装饰器案例   
```


#线程池应用例子：
import time 
from concurrent.futures import ThreadPoolExecutor

#线程池map()函数案例
def  func(name):
    for i  in range(100):
        print(name,i)

if __name__=='__main__':
    with ThreadPoolExecutor(10) as t:
        for i in range(10000):
            results=t.map(func,['张三','李四','王二麻子','傻蛋','不嘻嘻熬过'])
            for result  in results:
                print(result)



##线程池submit()函数案例
def  func(name):
    for i  in range(100):
        print(name,i)


if __name__=='__main__':
    with ThreadPoolExecutor(10) as t:
        for i in range(10000):
            t.submit(func,f'任务{i}')

    



 #@staticmethod装饰器传递多参数案例
class Mathtil:
    @staticmethod
    def add(x,y):
        return x*y
    
nnunb11=Mathtil.add(45,8)
print(nnunb11)



# @staticmethod装饰器传递字典数据案例：
class supper:
    @staticmethod
    def add(datect:dict):
        return  datect
    

def insert_data():
    updates={}
    number=input("请输入序号：")
    date=input("请输入日期：")
    contents=input("请输入内容：")
    grade=input("请输入级别：")
    dates={'number':number,'date': date,'contents': contents,'grade': grade}
    updates.update(dates)
    return updates

test11=insert_data()
csxg=supper.add(test11)

print("序号\t\t", "日期\t\t", "内容\t\t\t\t", "等级\t\t")
for key,value in  test11.items():
    print(f'{value}',end='    ')





```
## 实例化Dash应用   
```

#实例化Dash应用:
import dash
from dash import html
import feffery_antd_components as fac
from dash.dependencies import Input, Output

# 实例化Dash应用对象
app = dash.Dash(__name__)

# 添加初始化页面内容
app.layout = html.Div(
    [
        fac.AntdTitle('你好！Dash!',level=3),
        fac.AntdText('Dash版本%s' % dash.__version__),
        fac.AntdDivider(),
        fac.AntdText('fac版本%s' % fac.__version__)

    ]
)


if __name__ == '__main__':
    app.run(debug=False)


'''
https://fac.feffery.tech/
环境搭建
在基于dash和fac进行应用开发之前，我们需要先搭建好所需的环境，推荐使用conda作为环境管理工具，这里以Python 3.7版本为例，在终端执行下列命令进行相关环境的创建及激活：
注：由于国内pypi相关镜像的更新延迟，通过其进行相关库的安装，版本可能滞后于原始pypi中的最新版本
默认方式
国内使用镜像
conda create -n dash-devs python=3.7 -c https://mirrors.aliyun.com/anaconda/pkgs/main/ -y
conda activate dash-devs
完成环境的创建及激活后，我们在对应环境中直接通过pip进行相关基础依赖库的安装即可：
默认方式
国内使用镜像
pip install dash feffery-antd-components -U -i https://pypi.tuna.tsinghua.edu.cn/simple
或
conda create -n pytest-devs python=3.8 -c https://mirrors.aliyun.com/anaconda/pkgs/main/ -y

'''


```
## 扫描仪扫描自动点击鼠标脚本   
```

#扫描仪扫描自动点击鼠标脚本
import pyautogui
import time

def click(x, y, interval):
    # 点击指定位置的鼠标
    pyautogui.click(x, y)

    # 等待指定的时间间隔
    time.sleep(interval)

# 定义一个包含点击位置和时间间隔的列表
clicks = [(2425, 957, 1),(2167, 107, 1), (2769, 1257, 1)]

# 遍历列表，依次点击每个位置
for x, y, interval in clicks:
    click(x, y, interval)
'''
#检查鼠标位置函数备用
def wait_and_detect_mouse_position():
    # 等待 2 秒
    time.sleep(4)

    # 检测鼠标位置
    mouse_position = pyautogui.position()

    return mouse_position

# 调用函数
mouse_position = wait_and_detect_mouse_position()
print("鼠标位置：", mouse_position)

'''

```
