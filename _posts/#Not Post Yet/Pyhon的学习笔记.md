# Pyhon的学习笔记

# 第二部分 - 类型与运算


## 介绍python对象类型

### python的核心数据类型

> 内置对象

| 对象类型     | 例子 常例/创建                            |
| -------- | ----------------------------------- |
| 数字       | 1234, 3.14, 3+4j, Decimal, Fraction |
| 字符串      | 'spam', "guido's", b'a\xolc'        |
| 列表       | [1, [2, 'three'], 4]                |
| 字典       | {'food':'spam', 'taste':'yum'}      |
| 元组       | (1,'spam',4,'U')                    |
| 文件       | myfile=open('egg', 'r')             |
| 集合       | set('abc'), {'a','b','c'}           |
| 其他类型     | 类型、None、布尔形                         |
| 编程单元类型   | 函数、模块、类、                            |
| 与实现相关的类型 | 编译的代码堆栈跟踪                           |

- python中没有类型声明，它是动态类型，自动跟踪你的类型而不是要求声明代码
- 强类型语言，你只能对一个对象进行适合该类型的有效的操作



### 布尔(boolean)型

`True`和`False`为两种明确的布尔型数据类型

- 本质上是内置的证书类型int的子类
  - True和False和整数1和0是一样的



### Python表达式操作符

| 操作符            | 描述                 |
| -------------- | ------------------ |
| x or y         | 逻辑或，只有x为假的，才会计算y   |
| x and y        | 逻辑与，只有x为真，才会计算y    |
| not x          | 逻辑非                |
| >, <, <=, >=   | 大小比较               |
| x == y, x != y | 对等比较               |
| +, -, *, /     | 加减乘除               |
| x % y          | 余数                 |
| x[i]           | 索引                 |
| x[i:j:k]       | 分片                 |
| x(...)         | 调用（函数、方法、类及其他可调用的） |
| x.attr         | 属性引用               |
| (...)          | 元组，表达式，生成器表达式      |
| [...]          | 列表，列表解析            |
| {...}          | 字典、集合、集合和字典解析      |



### 列表

- 列表是一个任意类型的对象的位置相关的有序组合
- 没有固定大小，大小可变
- 通过偏移量（offset）进行赋值及其他各种列表的方式进行调用

### 列表的序列操作

列表是序列的一种，支持所有对字符串所讨论过的序列操作。

```python
>>> L = [123, 'spam', 1.23]		# A list of three different-type objects
>>> len(L)
3
>>> L[0]						# Indexing by position
123
>>> L[:-1]						# Slicing a list returns a new list
>>> L + [4, 5, 6]				# Concatenation make a new list too
[123, 'spam', 1.23, 4, 5, 6]
>>> L							# not change the original list
[123, 'spam', 1.23]
```



### 字典

- 它不是序列，是一种映射关系(mapping).
- 映射是一个其他对象的合计，通过键而不是相对位置来存储
- 具有可变性

```python
>>> D = {'food': 'Spam', 'quantity': 4, 'color': 'pink'}
>>> D['food']		# Fetch value of key 'food'
'Spam'

>>> D['quantity'] += 1		# Add 1 to 'quantity' value
>>> D
{'food': 'Spam', 'color': 'pink', 'quantity':5}

# 空字典，每次以一个键来填写它。
>>> D = {}
>>> D['name'] = 'Bob'
>>> D['job'] = 'dev'

>>> D
{'job': 'dev', 'name': 'Bob'}
>>> print(D['name'])
Bob
```



### 键的排序: for 循环

通过字典的keys方法收集一个键的列表

```python
>>> D = {'a':1, 'b':2, 'c':3}
>>> D
{'c': 3, 'b': 2, 'a': 1}
>>> Ks = list(D.keys())
>>> Ks
['c', 'b', 'a']
>>> Ks.sort()
>>> Ks
['a', 'b', 'c']
>>> for key in Ks:
...     print(key, '=>', D[key])
...
a => 1
b => 2
c => 3
```

简化版：

```python
>>> D
{'c': 3, 'b': 2, 'a': 1}
>>> for key in sorted(D):
	print(key,'=>',D[key])
a => 1
b => 2
c => 3
```


### 元组

元组对象(tuple)基本上就是一个不可改变的列表，它是序列，具有不可变性。它编写在圆括号中。支持任意类型、任意套嵌以及常见的序列操作：

```python
>>> T = (1,2,3,4)				# A 4-item tuple
>>> len(T)						# length
4

>>> T + (5,6)					# Concatenation
(1, 2, 3, 4, 5, 6)

>>> T[0]						# Indexing, Slicing, and more
1

#In python 3:
>>> T.index(4)					# Tuple method: 4 appears at offset 3
3
>>> T.count(4)					# 4 appears once
1
	
```

元组不能再改变，元组是不可变的序列，也不可增加长短：

```python
>>> T[0] = 2					# Tuples are immutable
...error text omitted...
TypeError: 'tuple' object does not support item assignment
>>> T.append(4)
AttibutorError: 'tuple' object has no attribute 'append'
```

### 为什么要用元组

因为它的不可变性，提供了一种完整性的约束。



##字符串

#### 基本操作

- 可通过+进行合并
- *进行重复

```python
>>> len('abs')		# Length: # of items
3
>>> 'abc' + 'def'   # Concatenation: a new string
'abcdef'
>>> 'Ni!' * 4		# Repitition
'Ni!Ni!Ni!Ni!'
>>> print('-' * 80)	# 80dashes
```

> - Python中不需要做预声明，包括数据的大小
> - Python会使用引用值计数的垃圾收集策略，自动回收无用对象的内存空间
> - 注意，python不允许数字和字符串混合，'abc' + 9 会出错

```python
>>> myjob = "hacker"
>>> for c in myjob: print(c, end=' ')		# for中的循环迭代 in表达式操作符对字符和子字符串进行成员关系的测试
h a c k e r
>>> "k" in myjojb
True
>>> "z" in myjob
False
```

#### 索引和分片

> 字符串为字符的有序集合

- Python的偏移量是从0开始的，与C不同的是，支持负偏移（从结束处反向计数）

```python
>>> S = 'spam'
>>> S[0], S[-2]				# Indexing from front or end
('s', 'a')					
>>> S[1:3], S[1:], S[:-1]	# Slicing: extract a section
('pa', 'pam', 'spa')
```



![Screen Shot 2016-10-26 at 10.24.17 AM](img/in-post/python_Study/Screen Shot 2016-10-26 at 10.24.17 AM.png)



#### 常用字符串函数方法

##### 1. find()

Python find() 方法检测字符串中是否包含子字符串 str ，如果指定 beg（开始） 和 end（结束） 范围，则检查是否包含在指定范围内，如果包含子字符串返回开始的索引值(index number)，否则返回-1。

`str.find(str, beg=0, end=len(string))`

**实例：**

```python
#!/usr/bin/python

str1 = "this is string example....wow!!!";
str2 = "exam";

print str1.find(str2);			# 15
print str1.find(str2, 10);		# 15
print str1.find(str2, 40);		# -1
```

##### 2. split()

Python split()通过指定分隔符对字符串进行切片，str为分隔符，num为分割次数

`str.split(str="", num=string.count(str))` 

**返回值**： 分割后的字符串列表

**实例：**

```python
#!/usr/bin/python

str = "Line1-abcdef \nLine2-abc \nLine4-abcd";
print str.split( );	# ['Line1-abcdef', 'Line2-abc', 'Line4-abcd']
print str.split(' ', 1 );  # ['Line1-abcdef', '\nLine2-abc \nLine4-abcd']


header, body = r.split('\r\n\r\n', 1) # 分割1次，header被赋予列表index0的值， body为index1的值

```

##### 3. strip() 

Python strip() 方法用于移除字符串头尾指定的字符（默认为空格）。

`str.strip([chars]);`

**返回值**

返回移除字符串头尾指定的字符生成的新字符串。

```
#!/usr/bin/python

str = "0000000this is string example....wow!!!0000000";
print str.strip( '0' );  # this is string example....wow!!!


```

##### str.encode() str.decode()

转换string为bytestring

例子：

```python
>>> a = 'man'
>>> a
'man'
>>> a.encode()
b'man'
>>> type(a)
<class 'str'>
>>> type(a.encode())
<class 'bytes'>


>>> b = b'girl'
>>> b
b'girl'
>>> b.decode()
'girl'
```







##### x. str.format()

**语法**
它通过{}和:来代替%。

**“映射”示例**:

**通过位置**

```python
In [1]: '{0},{1}'.format('kzc',18)  
Out[1]: 'kzc,18'  
In [2]: '{},{}'.format('kzc',18)  
Out[2]: 'kzc,18'  
In [3]: '{1},{0},{1}'.format('kzc',18)  
Out[3]: '18,kzc,18'
```

**通过关键字参数**

```python
In [5]: '{name},{age}'.format(age=18,name='kzc')  
Out[5]: 'kzc,18'
```

**通过对象属性**
```
class Person:  
    def __init__(self,name,age):  
        self.name,self.age = name,age  
        def __str__(self):  
            return 'This guy is {self.name},is {self.age} old'.format(self=self)  
In [2]: str(Person('kzc',18))  
Out[2]: 'This guy is kzc,is 18 old'
```
**通过下标**

```python
In [7]: p=['kzc',18]
In [8]: '{0[0]},{0[1]}'.format(p)
Out[8]: 'kzc,18'
```





## 元组、文件及其他

- 元组由简单的对象组构成
- 元组(tuple)不能在原处修改，它是不可变的
- 不支持任何方法调用
- 具有列表的大多属性



### 实际应用中的元组






# 第三部分 - 语句和语法

### If语句

```python
if <test1>:					# if test
    <statements1>			# Associated block
elif <test2>:				# Optional elifs
    <statements2>
else:						# Optional else
    <statements3>
```

- 记得模块的缩进

### pass语句

因为函数部分还未完成，但又不能空着不写，因此可以用pass来替代占个位置

```python
def func():
	pass		#pass语句在函数中来占为
```





# 函数

### def语句

```python
	def <name>(arg1, arg2, ...argN):
        ...
   		return <value>
```



- def语句是实施执行的
- 没有独立的编译时间
- 不需要像C一样在运行前全部定义
- 可以用if根据不同的情况，定义同一个func()以不同的方式
- 函数仅仅是对象






# 第五部分 - 模块

- 每一个文件就是一个模块  如 test.py
- 模块由两个语句和一个重要的内置函数进行处理
  - import  使客户端(导入者)以一个整体获取一个模块
  - from 允许客户端从一个模块文件中获取特定的变量名
  - imp.reload 在不中止Python程序的情况下，提供了一种重新载入模块文件代码的方法



# 第六部分 - 类和opp

OO(面对对象) OPP(面对对象程序设计): 

- 代码的重用
- 把代码的沉余度降至最低，
- 对现存的代码进行定制来编写程序



1. 类是一种产生实例的工厂
2. def出现在类的内部，通常称为**方法**，而且会自动接受第一个特殊参数(通常称为self)，这个参数提供了被处理的实例的参考值。
3. `def __initial__(self, who)也称**构造函数**





# 第七部分 - 异常和工具

## 异常基础

try/except: 	捕捉由python或你引起的异常并恢复

try/finally:	无论异常是否发生，执行清理行为

raise：		手动在代码中触发异常

assert:		有条件的在程序代码中触发异常

with/as:		在python2.6和后续版本中实现环境管理器



- 异常时一种结构化的"超级goto"，异常处理器(try语句)会留下标记，并可执行一些代码。

**try/except:**

```python
try:
<语句>        #运行别的代码
except <名字>：
<语句>        #如果在try部份引发了'name'异常
except <名字>，<数据>:
<语句>        #如果引发了'name'异常，获得附加的数据
else:
<语句>        #如果没有异常发生
```

**使用except而不带任何异常类型**
你可以不带任何异常类型使用except，如下实例：

```python
try:
    正常的操作
   ......................
except:
    发生异常，执行这块代码
   ......................
else:
    如果没有异常执行这块代码
```






# 其他
## **pass**

pass 表示这里什么都没有，不执行任何操作
如果你的程序还有未完成的函数和类等，你可以先添加一些注释，然后代码部分仅仅写一个 pass，这样程序可以运行不会报错，而后期你可以继续完善你的程序
```python
>>> class Nothing:  
    pass  
  
>>>   
```

## **断言 assert**

如果断言成功, 条件成立,后面语句为真, 则通过测试, 否则为测试失败, 中断程序报错

```
>>> x  
1.2  
>>> assert x > 1  
>>> assert x > 2  
Traceback (most recent call last):  
  File "<pyshell#61>", line 1, in <module>  
    assert x > 2  
AssertionError  
>>> assert x > 2, 'x must bigger than 2'  
Traceback (most recent call last):  
  File "<pyshell#64>", line 1, in <module>  
    assert x > 2, 'x must bigger than 2'  
AssertionError: x must bigger than 2  
>>>   
```

## **open/文件操作**

`open(file[, mode[, buffering[, encoding[, errors[, newline[, closefd=True]]]]]])`

**open函数有很多的参数，常用的是file，mode和encoding**

- file文件位置，需要加引号
- mode文件打开模式，见下面3
- encoding表示的是返回的数据采用何种编码，一般采用utf8或者gbk

`f=open('/tmp/hello','w')`

**常用模式:**

> 读写模式:r只读,r+读写,w新建(会覆盖原有文件),a追加模式,b二进制文件.

如:'rb','wb','r+b'等等


**注意：**

1、使用'W'，文件若存在，首先要清空，然后（重新）创建，

2、使用'a'模式 ，把所有要写入文件的数据都追加到文件的末尾，即使你使用了seek（）指向文件的其他地方，如果文件不存在，将自动被创建。

- **关键字参数**

  python里面运行可变参数的出现，参数中出现(*arg,**arg2)的形式。

  例如：

  ```python
  def foo1(arg1,arg2,key1=1,key2=2,*arg,**keywords):
      print "arg1 parameters is ",arg1
      print "arg2 parameters is ",arg2
      print "key1 parameter is ",key1
      print "key2 parameter is ",key2
      print "Arbitrary parameter is ", arg
      print "keywords parameter is ",keywords

  foo1(1,2,3,4,5,6,k1=1,k2=2,k3=3)
  ```

  输出：

  ```python
  arg1 parameters is  1
  arg2 parameters is  2
  key1 parameter is  3
  key2 parameter is  4
  arg parameter is  (5, 6)
  keywords parameter is  {'k3': 3, 'k2': 2, 'k1': 1}
  ```

  函数参数分为**四部分**：

  - arg1, arg2，key1，key2普通参数
  - *arg 非关键字参数列表
  - **keywords 关键字参数列表

  函数声名部分，参数的**四个部分不可颠倒位置**，可以没有其中某几部分。

  python函数的这种特性使得函数参数更加灵活，**参数个数也不受限制。**

  注意：这种用法常用在python的装饰器中，至于什么是装饰器，它是python里面非常重要的一个特性，我会在以后详解

## **Python在函数中使用**`*`**和**`**`**接收元组和列表**

- 获取可变数量的参数 的时候特别有用。
- 由于在args变量前有*前缀 ，所有多余的函数参数都会作为一个元组存储在args中 。如果使用的是**前缀 ，多余的参数则会被认为是一个字典的健/值对 。
    - 对于def func(*args):，*args表示把传进来的位置参数存储在tuple（元组）args里面。例如，调用func(1, 2, 3) ，args就表示(1, 2, 3)这个元组 。
    - 对于def func(**args):，**args表示把参数作为字典的健-值对存储在dict（字典）args里面。例如，调用func(a='I', b='am', c='wcdj') ，args就表示{'a':'I', 'b':'am', 'c':'wcdj'}这个字典 。
- 注意普通参数与*和**参数公用的情况，一般将*和**参数放在参数列表最后。
    - ​
##  **classmethod & staticmethod 区别**

-   普通对象方法，第一个参数需要是self，它表示一个具体的实例本身。
-   `@classmethod` 是一个函数修饰符，它表示接下来的是一个类方法，而对于平常我们见到的则叫做实例方法。 类方法的第一个参数cls，而实例方法的第一个参数是self，表示该类的一个实例。 
    - 类方法有类变量cls传入，从而可以用cls做一些相关的处理。**并且有子类继承时，调用该类方法时，传入的类变量cls是子类，而非父类。** 对于类方法，可以通过类来调用，就像C.f()，有点类似C＋＋中的静态方法, 也可以通过类的一个实例来调用，就像C().f()，这里C()，写成这样之后它就是类的一个实例了。 
    - `@staticmethod`静态方法则没有，它基本上跟一个全局函数相同，一般来说用的很少




## Python的列表推导式

- 列表推导式书写形式：　　

[表达式 for 变量 in 列表]    或者  [表达式 for 变量 in 列表 if 条件]

- 列表推导式标准操作方法：

  ```python
  >>> a = [1,2,3,4,5,6,7,8,9,10]
  >>> [3*x for x in a]
  [3, 6, 9, 12, 15, 18, 21, 24, 27, 30]
  ```

  ​

## 读取/存储文件数据的方式

```python
with open(path, 'w+', encoding='utf-8') as f:
    # log('save', path, s, data)
    f.write(s)
```

**python读取文件内容的方法：**

```python
file_path = './db/douban.txt'
    file = open(file_path, 'r', encoding='utf-8')
    all_the_text = file.read()
    file.close()
```



## 内置函数：bin()、oct()、int()、hex()可实现进制转换

| ↓    | 2进制            | 8进制            | 10进制            | 16进制            |
| ---- | -------------- | -------------- | --------------- | --------------- |
| 2进制  | -              | bin(int(x, 8)) | bin(int(x, 10)) | bin(int(x, 16)) |
| 8进制  | oct(int(x, 2)) | -              | oct(int(x, 10)) | oct(int(x, 16)) |
| 10进制 | int(x, 2)      | int(x, 8)      | -               | int(x, 16)      |
| 16进制 | hex(int(x, 2)) | hex(int(x, 8)) | hex(int(x, 10)) | -               |

## 遍历函数enumerate

在同时需要index和value值的时候可以使用 enumerate。

```python
list1 = ["这", "是", "一个", "测试"]
for index, item in enumerate(list1):
    print index, item
>>>
0 这
1 是
2 一个
3 测试
```

## 时间显示和格式

```python
def log(*args, **kwargs):
    # time.time() 返回 unix time
    # 如何把 unix time 转换为普通人类可以看懂的格式呢？ 
    format = '%H:%M:%S' # 23:59:59
    value = time.localtime(int(time.time()))
    dt = time.strftime(format, value)
    with open('log.gua.txt', 'a', encoding='utf-8') as f:
        print(dt, *args, file=f, **kwargs)
```

format:

```
%a Abbreviated weekday name 
%A Full weekday name 
%b Abbreviated month name 
%B Full month name 
%c Date and time representation appropriate for locale 
%d Day of month as decimal number (01 - 31) 
%H Hour in 24-hour format (00 - 23) 
%I Hour in 12-hour format (01 - 12) 
%j Day of year as decimal number (001 - 366) 
%m Month as decimal number (01 - 12) 
%M Minute as decimal number (00 - 59) 
%p Current locale's A.M./P.M. indicator for 12-hour clock 
%S Second as decimal number (00 - 59) 
%U Week of year as decimal number, with Sunday as first day of week (00 - 51) 
%w Weekday as decimal number (0 - 6; Sunday is 0) 
%W Week of year as decimal number, with Monday as first day of week (00 - 51) 
%x Date representation for current locale 
%X Time representation for current locale 
%y Year without century, as decimal number (00 - 99) 
%Y Year with century, as decimal number 
%z, %Z Time-zone name or abbreviation; no characters if time zone is unknown 
%% Percent sign
```

