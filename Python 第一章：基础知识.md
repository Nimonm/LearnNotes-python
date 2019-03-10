# Python 第一章：基础知识

## 1. 基础知识

#### 长整数：

在正数后面加一个‘L’或‘l’，但是小写容易误认为是1，所以一般用大写。

#### 十六进制：

~~~
>>> 0xAF
175
~~~

#### 八进制数：

~~~
>>> 101
8
~~~

十六进制和八进制首位都是0.

#### 变量：

临时存储器

#### 语句：

改变事物，如：赋值语句改变了变量，print语句改变了屏幕显示的内容。

#### 获取用户输入：

~~~
>>> input('the mean of life: ')
the mean of life: happy
happy
~~~

#### 函数：

~~~
>>> 2**3
8
>>> pow(2,3) # 幂运算
8
>>> 10 + pow(2,3*5)/3.0
10932.666666666666
>>> abs(-10)
10
>>> 1/2
0
>>> rond(1.0/2.0) # 将结果四舍五入到最接近的整数
1.0
~~~

#### 模块：

~~~
>>> import math
>>> math.floor(32.9)
32.0
~~~

用import导入模块，然后按照“模块.函数”的格式使用，若想将年龄转换为整数32，而不是浮点数32.0，可以用int函数：

~~~
>>> int(math.floor(32.9))
32
~~~

不写模块的名字：

~~~
>>> from math import sqrt
>>> sqrt(9)
3.0
~~~

cmath和复数

~~~
>>> from math import sqrt
>>> sqrt(-1)
报错  # 原因：不能求负数的平方根
>>> import cmath
>>> cmath.sqrt(-1)
1j

>>> (1+3j)*(9+4j)
(-3+31j)
~~~

回到 __ future __



#### 字符串

单引号字符串和转义引号

字符串中含有单引号的时候最好用双引号，或者句中的引号用反斜杠进行转义。

~~~、
>>> 'Let's go!'
SyntaxError: invalid syntax
>>> 'Let\'s go!'
Let's go!
~~~

拼接字符串

~~~
>>> "hello, + "world"
"hello,world"
>>> x = "hello,"
>>> y = "world"
>>> x + y
'hello,world'
~~~

字符串表示，str和repr

~~~
>>> "hello,world"
"hello,world"
>>> 10000L
10000L
>>> print("hello,world")
hello,world
>>> print(10000L)
10000
>>> print(str(10000L))
10000L
>>> print(repr(10000L))
10000L
~~~

input和raw_input比较

~~~
>>> input("enter a number: ")
enter a number: 3
3
>>> raw_input("enter a number: ")
enter a number: 3
'3'
~~~

除非对input有特别需要，否则应尽量使用raw_input。

长字符串：

>  如果需要些衣蛾非常长的字符串，需要跨行，可以用三个引号代替普通引号，也可以使用三个双引号。

原始字符串，以r开头：

~~~
>>> path = 'C:\nowhere'
>>> path
C:
owhere

>>> path = 'C:\\nowhere'
>>> path
C:\nowhere

path = 'C:\\prgram files\\fnord\\foo\\bar\\baz\\frozz\\bozz'  # 很麻烦

>>> print(r'C:\prgram files\fnord\foo\bar\baz\frozz\bozz')
C:\prgram files\fnord\foo\bar\baz\frozz\bozz
~~~

Unicode字符串：

~~~
>>> u'hello world'
u'hello world'
~~~



#### 本章函数

~~~
abs(number)                     # 绝对值
cmath.sqrt(number)              # 平方根，可用于负数
math.sqrt(number)               # 平方根，不可用于负数
float(object)                   # 
help()                          #
input(prompt)                   #
int(object)                     #
long(object)                    #
math.ceil(number)               # 向上取整
math.floor(number)              # 向下取整
pow(x,y[,z])                    # x的y次幂（所得结果对z取模）
raw_input(prompt)               # 获取用户输入，结果被看做原始字符串
repr(object)                    # 字符串
round(number[.ndigits])         # 根据给定精度对数字进行四舍五入
str(object)                     # 字符串
~~~

