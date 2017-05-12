### 代码基础要素

#### 标识符

1. 在 Python 里，标识符有字母、数字、下划线组成。所有标识符可以包括英文(区分大小写)、数字以及下划线(_)，但不能以数字开头。

2. 在Python 中下划线是有特殊意义。

   > 以单下划线开头 ，代表不能直接访问的类属性，需通过类提供的接口进行访问，不能用 from xxx import * 而导入。

   ```
   _id = 1;
   ```

   > 以双下划线开头的 __foo 代表类的私有成员；__

   ```
   __id = 1;
   ```

   以双下划线开头和结尾的 __foo__ 代表 Python 里特殊方法专用的标识，如 __init__() 代表类的构造函数。

3. Python 可以同一行显示多条语句，方法是用分号 ; 分开，如：

   ```
   >>> print 'hello';print 'runoob';
   hello
   runoob
   ```

4. 得到

#### 保留字符

​	所有 Python 的关键字只包含小写字母。

| and      | exec    | not    |
| -------- | ------- | ------ |
| assert   | finally | or     |
| break    | for     | pass   |
| class    | from    | print  |
| continue | global  | raise  |
| def      | if      | return |
| del      | import  | try    |
| elif     | in      | while  |
| else     | is      | with   |
| except   | lambda  | yield  |

#### 行和缩进

学习 Python 与其他语言最大的区别就是，Python 的代码块不使用大括号 {} 来控制类，函数以及其他逻辑判断。python 最具特色的就是用缩进来写模块。

#### 多行语句

Python语句中一般以新行作为为语句的结束符。

但是我们可以使用斜杠（ \）将一行的语句分为多行显示，如下所示：

```
total = item_one + \
        item_two + \
        item_three
```

语句中包含 [], {} 或 () 括号就不需要使用多行连接符。如下实例：

```
days = ['Monday', 'Tuesday', 'Wednesday',
        'Thursday', 'Friday']
```

#### Python 引号

Python 可以使用引号( **'** )、双引号( **"** )、三引号( **'''** 或 **"""** ) 来表示字符串，引号的开始与结束必须的相同类型的。

其中三引号可以由多行组成，编写多行文本的快捷语法，常用语文档字符串，在文件的特定地点，被当做注释。

```
word = 'word'
sentence = "这是一个句子。"
paragraph = """这是一个段落。
包含了多个语句"""
```



#### Python注释

python中单行注释采用 # 开头。

```
#!/usr/bin/python
# -*- coding: UTF-8 -*-
# 文件名：test.py

# 第一个注释
print "Hello, Python!";  # 第二个注释
```

python 中多行注释使用三个单引号(''')或三个双引号(""")。

```
#!/usr/bin/python
# -*- coding: UTF-8 -*-
# 文件名：test.py


'''
这是多行注释，使用单引号。
这是多行注释，使用单引号。
这是多行注释，使用单引号。
'''

"""
这是多行注释，使用双引号。
这是多行注释，使用双引号。
这是多行注释，使用双引号。
"""
```



#### Python空行

函数之间或类的方法之间用空行分隔，表示一段新的代码的开始。类和函数入口之间也用一行空行分隔，以突出函数入口的开始。

空行与代码缩进不同，空行并不是Python语法的一部分。书写时不插入空行，Python解释器运行也不会出错。但是空行的作用在于分隔两段不同功能或含义的代码，便于日后代码的维护或重构。

记住：空行也是程序代码的一部分。



#### 同一行显示多条语句

Python可以在同一行中使用多条语句，语句之间使用分号(;)分割，以下是一个简单的实例：

```
#!/usr/bin/python

import sys; x = 'runoob'; sys.stdout.write(x + '\n')
```



#### Print 输出

print 默认输出是换行的，如果要实现不换行需要在变量末尾加上逗号：

```
#!/usr/bin/python
# -*- coding: UTF-8 -*-

x="a"
# 换行输出
print x
# 不换行输出
print x,
```



#### 多个语句构成代码组

缩进相同的一组语句构成一个代码块，我们称之代码组。

像if、while、def和class这样的复合语句，首行**以关键字开始，以冒号( : )结束**，该行之后的一行或多行代码构成代码组。

我们将首行及后面的代码组称为一个子句(clause)。

如下实例：

```
if expression : 
   suite 
elif expression :  
   suite  
else :  
   suite 
```

#### 变量与数据类型

- Python 中的变量赋值不需要类型声明。

- 每个变量在内存中创建，都包括变量的标识，名称和数据这些信息。

- 每个变量在使用前都必须赋值，变量赋值以后该变量才会被创建。

- 等号（=）用来给变量赋值。等号（=）运算符左边是一个变量名,等号（=）运算符右边是存储在变量中的值。

- 变量不需要时，可以通过del　进行删除单个或多个对象的引用

  ##### 数据类型

  - ##### Numbers（数字）

    | int    | long                  | float      | complex    |
    | ------ | --------------------- | ---------- | ---------- |
    | 10     | 51924361L             | 0.0        | 3.14j      |
    | 100    | -0x19323L             | 15.20      | 45.j       |
    | -786   | 0122L                 | -21.9      | 9.322e-36j |
    | 080    | 0xDEFABCECBDAECBFBAEl | 32.3e+18   | .876j      |
    | -0490  | 535633629843L         | -90.       | -.6545+0J  |
    | -0x260 | -052318172735L        | -32.54e100 | 3e+26J     |
    | 0x69   | -4721885298529L       | 70.2E-12   | 4.53e-7j   |

  - String（字符串）

    - 字符串或串(String)是由数字、字母、下划线组成的一串字符。

    - 字符串分割可以使用变量 **[头下标:尾下标]**，就可以截取相应的字符串，其中下标是从 0 开始算起，可以是正数或负数，下标可以为空表示取到头或尾。

      ```
      s = 'ilovepython'
      s[1:5]的结果是love。
      ```

    - python字符串格式化符号:

      | 符   号 | 描述                 |
      | ----- | ------------------ |
      | %c    | 格式化字符及其ASCII码      |
      | %s    | 格式化字符串             |
      | %d    | 格式化整数              |
      | %u    | 格式化无符号整型           |
      | %o    | 格式化无符号八进制数         |
      | %x    | 格式化无符号十六进制数        |
      | %X    | 格式化无符号十六进制数（大写）    |
      | %f    | 格式化浮点数字，可指定小数点后的精度 |
      | %e    | 用科学计数法格式化浮点数       |
      | %E    | 作用同%e，用科学计数法格式化浮点数 |
      | %g    | %f和%e的简写           |
      | %G    | %f 和 %E 的简写        |
      | %p    | 用十六进制数格式化变量的地址     |

    - python的字符串内建函数

      | **方法**                                   | **描述**                                   |
      | :--------------------------------------- | :--------------------------------------- |
      | [string.capitalize()]()                  | 把字符串的第一个字符大写                             |
      | [string.center(width)](http://www.runoob.com/python/att-string-center.html) | 返回一个原字符串居中,并使用空格填充至长度 width 的新字符串        |
      | **string.count(str, beg=0, end=len(string))** | 返回 str 在 string 里面出现的次数，如果 beg 或者 end 指定则返回指定范围内 str 出现的次数 |
      | [string.decode(encoding='UTF-8', errors='strict')](http://www.runoob.com/python/att-string-decode.html) | 以 encoding 指定的编码格式解码 string，如果出错默认报一个 ValueError 的 异 常 ， 除 非 errors 指 定 的 是 'ignore' 或 者'replace' |
      | [string.encode(encoding='UTF-8', errors='strict')](http://www.runoob.com/python/att-string-encode.html) | 以 encoding 指定的编码格式编码 string，如果出错默认报一个ValueError 的异常，除非 errors 指定的是'ignore'或者'replace' |
      | **string.endswith(obj, beg=0, end=len(string))** | 检查字符串是否以 obj 结束，如果beg 或者 end 指定则检查指定的范围内是否以 obj 结束，如果是，返回 True,否则返回 False. |
      | [string.expandtabs(tabsize=8)](http://www.runoob.com/python/att-string-expandtabs.html) | 把字符串 string 中的 tab 符号转为空格，tab 符号默认的空格数是 8。 |
      | **string.find(str, beg=0, end=len(string))** | 检测 str 是否包含在 string 中，如果 beg 和 end 指定范围，则检查是否包含在指定范围内，如果是返回开始的索引值，否则返回-1 |
      | **string.format()**                      | 格式化字符串                                   |
      | **string.index(str, beg=0, end=len(string))** | 跟find()方法一样，只不过如果str不在 string中会报一个异常.    |
      | [string.isalnum()](http://www.runoob.com/python/att-string-isalnum.html) | 如果 string 至少有一个字符并且所有字符都是字母或数字则返回 True,否则返回 False |
      | [string.isalpha()](http://www.runoob.com/python/att-string-isalpha.html) | 如果 string 至少有一个字符并且所有字符都是字母则返回 True,否则返回 False |
      | [string.isdecimal()](http://www.runoob.com/python/att-string-isdecimal.html) | 如果 string 只包含十进制数字则返回 True 否则返回 False.   |
      | [string.isdigit()](http://www.runoob.com/python/att-string-isdigit.html) | 如果 string 只包含数字则返回 True 否则返回 False.      |
      | [string.islower()](http://www.runoob.com/python/att-string-islower.html) | 如果 string 中包含至少一个区分大小写的字符，并且所有这些(区分大小写的)字符都是小写，则返回 True，否则返回 False |
      | [string.isnumeric()](http://www.runoob.com/python/att-string-isnumeric.html) | 如果 string 中只包含数字字符，则返回 True，否则返回 False   |
      | [string.isspace()](http://www.runoob.com/python/att-string-isspace.html) | 如果 string 中只包含空格，则返回 True，否则返回 False.    |
      | [string.istitle()](http://www.runoob.com/python/att-string-istitle.html) | 如果 string 是标题化的(见 title())则返回 True，否则返回 False |
      | [string.isupper()](http://www.runoob.com/python/att-string-isupper.html) | 如果 string 中包含至少一个区分大小写的字符，并且所有这些(区分大小写的)字符都是大写，则返回 True，否则返回 False |
      | **string.join(seq)**                     | 以 string 作为分隔符，将 seq 中所有的元素(的字符串表示)合并为一个新的字符串 |
      | [string.ljust(width)](http://www.runoob.com/python/att-string-ljust.html) | 返回一个原字符串左对齐,并使用空格填充至长度 width 的新字符串       |
      | [string.lower()](http://www.runoob.com/python/att-string-lower.html) | 转换 string 中所有大写字符为小写.                    |
      | [string.lstrip()](http://www.runoob.com/python/att-string-lstrip.html) | 截掉 string 左边的空格                          |
      | [string.maketrans(intab, outtab\])](http://www.runoob.com/python/att-string-maketrans.html) | maketrans() 方法用于创建字符映射的转换表，对于接受两个参数的最简单的调用方式，第一个参数是字符串，表示需要转换的字符，第二个参数也是字符串表示转换的目标。 |
      | [max(str)](http://www.runoob.com/python/att-string-max.html) | 返回字符串 *str* 中最大的字母。                      |
      | [min(str)](http://www.runoob.com/python/att-string-min.html) | 返回字符串 *str* 中最小的字母。                      |
      | **string.partition(str)**                | 有点像 find()和 split()的结合体,从 str 出现的第一个位置起,把 字 符 串 string 分 成 一 个 3 元 素 的 元 组 (string_pre_str,str,string_post_str),如果 string 中不包含str 则 string_pre_str == string. |
      | **string.replace(str1, str2,  num=string.count(str1))** | 把 string 中的 str1 替换成 str2,如果 num 指定，则替换不超过 num 次. |
      | [string.rfind(str, beg=0,end=len(string) )](http://www.runoob.com/python/att-string-rfind.html) | 类似于 find()函数，不过是从右边开始查找.                 |
      | [string.rindex( str, beg=0,end=len(string))](http://www.runoob.com/python/att-string-rindex.html) | 类似于 index()，不过是从右边开始.                    |
      | [string.rjust(width)](http://www.runoob.com/python/att-string-rjust.html) | 返回一个原字符串右对齐,并使用空格填充至长度 width 的新字符串       |
      | string.rpartition(str)                   | 类似于 partition()函数,不过是从右边开始查找.            |
      | [string.rstrip()](http://www.runoob.com/python/att-string-rstrip.html) | 删除 string 字符串末尾的空格.                      |
      | **string.split(str="", num=string.count(str))** | 以 str 为分隔符切片 string，如果 num有指定值，则仅分隔 num 个子字符串 |
      | [string.splitlines([keepends\])](http://www.runoob.com/python/att-string-splitlines.html) | 按照行('\r', '\r\n', \n')分隔，返回一个包含各行作为元素的列表，如果参数 keepends 为 False，不包含换行符，如果为 True，则保留换行符。 |
      | [string.startswith(obj, beg=0,end=len(string))](http://www.runoob.com/python/att-string-startswith.html) | 检查字符串是否是以 obj 开头，是则返回 True，否则返回 False。如果beg 和 end 指定值，则在指定范围内检查. |
      | **string.strip([obj])**                  | 在 string 上执行 lstrip()和 rstrip()          |
      | [string.swapcase()](http://www.runoob.com/python/att-string-swapcase.html) | 翻转 string 中的大小写                          |
      | [string.title()](http://www.runoob.com/python/att-string-title.html) | 返回"标题化"的 string,就是说所有单词都是以大写开始，其余字母均为小写(见 istitle()) |
      | **string.translate(str, del="")**        | 根据 str 给出的表(包含 256 个字符)转换 string 的字符,要过滤掉的字符放到 del 参数中 |
      | [string.upper()](http://www.runoob.com/python/att-string-upper.html) | 转换 string 中的小写字母为大写                      |
      | [string.zfill(width)](http://www.runoob.com/python/att-string-zfill.html) | 返回长度为 width 的字符串，原字符串 string 右对齐，前面填充0   |
      | [string.isdecimal()](http://www.runoob.com/python/att-string-isdecimal.html) | isdecimal()方法检查字符串是否只包含十进制字符。这种方法只存在于unicode对象。 |

    - ｆｇ

  - List（列表）

    - 列表用[ ]标识。是python最通用的复合数据类型。

    - 列表中的分割也可以用到变量[头下标:尾下标]，就可以截取相应的列表，从左到右索引默认0开始的，从右到左索引默认-1开始，下标可以为空表示取到头或尾。

      ```
      list=[];
      list.append('runoob)
      list.append(786)
      list.append(2.23)
      ```

  - Tuple（元组）

    - 元组用"()"标识，类似于List（列表）。内部元素用逗号隔开。但是元组不能二次赋值，相当于只读列表。

      ```
      tuple = ( 'runoob', 786 , 2.23, 'john', 70.2 )
      ```

  - Dictionary（字典）

    - 字典用"{}"标识。字典由索引(key)和它对应的值value组成。

      ```
      dict = {};
      dict['id'] = 1000;
      dict['name'] = 'old driver';
      print dict

      输出结果为：

      {'id': 1000, 'name': 'old driver'}
      ```


      ```

#### 函数

你可以定义一个由自己想要功能的函数，以下是简单的规则：

- 函数代码块以 **def** 关键词开头，后接函数标识符名称和圆括号**()**。

- 任何传入参数和自变量必须放在圆括号中间。圆括号之间可以用于定义参数。

- 函数的第一行语句可以选择性地使用文档字符串—用于存放函数说明。

- 函数内容以冒号起始，并且缩进。

- **return [表达式]** 结束函数，选择性地返回一个值给调用方。不带表达式的return相当于返回 None。

- 格式

  ```
  def 函数名(传参a,传参b....):
  	'注释...'
  	
  	函数体 
  ```

### 基本语法结构

#### 条件语句

```
if 判断条件：
    执行语句……
else：
    执行语句……
```

```
if 判断条件1:
    执行语句1……
elif 判断条件2:
    执行语句2……
elif 判断条件3:
    执行语句3……
else:
    执行语句4……
```

#### 循环语句

- while

  ```
  while 判断条件：
      执行语句……
  ```


for 循环语句

```
for iterating_var in sequence:
   执行语句……
```
循环控制

| 控制语句        | 描述                      |
| ----------- | ----------------------- |
| break 语句    | 在语句块执行过程中终止循环，并且跳出整个循环  |
| continue 语句 | 跳出该次循环，执行下一次循环。         |
| pass 语句     | pass是空语句，是为了保持程序结构的完整性。 |



#### 异常捕获

格式A()

```
try:
	正常运行的代码
except <名字>：
	捕获了'name'异常异常，执行这块代码
except <名字>，<数据>:   [or  ]
	捕获了'name'异常，获得附加的数据
#except: 
#捕获了异常，不具体何种错误
else:
	如果没有异常执行这块代码
finally:
	退出try时总会执行
```

```

```





### 文件与I/O

- 输入:

  raw_input（函数从标准输入读取一个行，并返回一个字符串（去掉结尾的换行符））

  input（input 可以接收一个Python表达式作为输入，并将运算结果返回。）

- 输出:

  print:

- 文件：





### 面向对象

#### 语法格式

```
class ClassName(ParentClassA,ParentClassB):#继承ParentClassA、ParentClassB（ps:python与C一样支持多继承）
	'类的注释信息' 
	name = 'Li Xiao' #类属性，可以不定义或者不赋值
   
	def __init__(self, name):# 类的构造函数或初始化方法
		self.name = name #self代表类的实例，在定义类的方法时必须有的，在调用时不必传入。
    
    def getName(self):
    	return self.name
   
   
```

#### 类的实例化

```
cls1 = ClassName('Li Xiao')
```



#### 继承



```

```