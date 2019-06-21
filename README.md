## 一、环境
使用的是Python 3
目前有两个环境
- Colab Notebook 用来做机器学习
- Visual Studio Code 用来学习Python语法


## 二、print and input


<pre><code>
some_var = input("输入一个数字")

if some_var > 10:
    print("some_var比10大")
elif some_var < 10:    # elif句是可选的
    print("some_var比10小")
else:                  # else也是可选的
    print("some_var就是10")
</code></pre>


## 三、python变量特性+命名释方法

* Python 中的变量不需要声明类型。
* 用“=”号来给变量赋值
* 每个变量在使用前都必须赋值，变量赋值以后才会被创建。
* Python中，一切事物都是对象，变量引用的是对象或者说是对象在内存中的地址。
* 在Python中，变量本身没有数据类型的概念，通常所说的“变量类型”是变量所引用的对象的类型，或者说是变量的值的类型。
* Python允许同时为多个变量赋值。
* Python中的一切都是对象，变量是对象的引用！
* 命名释方法：详情：https://python-guide.gitbooks.io/python-style-guide/content/style-guide/variables.html

### python中“：”

<pre><code>
string = "asfasdfgdfsgsdfgsdfgdsfg" 
#默认返回全部
print string[:]

#返回1到9结果
print string[1:9]

#返回1到9结果,步长为1
print string[1:9:]

#返回1到9结果,步长为2
print string[1:9:2]

#返回1到9结果,步长为-1
print string[1:9:-1]

#转置
print string[::-1]
</code></pre>

### dir( )
<pre><code>
>>>dir()   #  获得当前模块的属性列表
['__builtins__', '__doc__', '__name__', '__package__', 'arr', 'myslice']
>>> dir([ ])    # 查看列表的方法
['__add__', '__class__', '__contains__', '__delattr__', '__delitem__', '__delslice__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getslice__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__setslice__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
</code></pre>

### help()
<pre><code>
>>>help('sys')             # 查看 sys 模块的帮助
……显示帮助信息……
 
>>>help('str')             # 查看 str 数据类型的帮助
……显示帮助信息……
 
>>>a = [1,2,3]
>>>help(a)                 # 查看列表 list 帮助信息
……显示帮助信息……
 
>>>help(a.append)          # 显示list的append方法的帮助
……显示帮助信息……
</code></pre>

### import()
import语句使用以下几种方式导入包中的模块: 
* import Graphics.Primitive.fill 导入模块Graphics.Primitive.fill,只能以全名访问模块属性,例如 Graphics.Primitive.fill.floodfill(img,x,y,color). 
* from Graphics.Primitive import fill 导入模块fill ,只能以 fill.属性名这种方式访问模块属性,例如 fill.floodfill(img,x,y,color). 
* from Graphics.Primitive.fill import floodfill 导入模块fill ,并将函数floodfill放入当前名称空间,直接访问被导入的属性，例如 floodfill(img,x,y,color).

### pep8介绍
pep8 是一种编码风格,详情：https://www.cnblogs.com/kungfupanda/p/5267802.html。
  
# 4. python数值基本知识：
<pre><code>
# 整数
3  # => 3

# 算术没有什么出乎意料的
1 + 1  # => 2
8 - 1  # => 7
10 * 2  # => 20

# 但是除法例外，会自动转换成浮点数
35 / 5  # => 7.0
5 / 3  # => 1.6666666666666667

# 整数除法的结果都是向下取整
5 // 3     # => 1
5.0 // 3.0 # => 1.0 # 浮点数也可以
-5 // 3  # => -2
-5.0 // 3.0 # => -2.0

# 浮点数的运算结果也是浮点数
3 * 2.0 # => 6.0

# 模除
7 % 3 # => 1

# x的y次方
2**4 # => 16

# 用括号决定优先级
(1 + 3) * 2  # => 8

# 布尔值
True
False

# 用not取非
not True  # => False
not False  # => True

# 逻辑运算符，注意and和or都是小写
True and False # => False
False or True # => True

# 整数也可以当作布尔值
0 and 2 # => 0
-5 or 0 # => -5
0 == False # => True
2 == True # => False
1 == True # => True

# 用==判断相等
1 == 1  # => True
2 == 1  # => False

# 用!=判断不等
1 != 1  # => False
2 != 1  # => True

# 比较大小
1 < 10  # => True
1 > 10  # => False
2 <= 2  # => True
2 >= 2  # => True

# 大小比较可以连起来！
1 < 2 < 3  # => True
2 < 3 < 2  # => False

# 字符串用单引双引都可以
"这是个字符串"
'这也是个字符串'

# 用加号连接字符串
"Hello " + "world!"  # => "Hello world!"

# 字符串可以被当作字符列表
"This is a string"[0]  # => 'T'

# 用.format来格式化字符串
"{} can be {}".format("strings", "interpolated")

# 可以重复参数以节省时间
"{0} be nimble, {0} be quick, {0} jump over the {1}".format("Jack", "candle stick")
# => "Jack be nimble, Jack be quick, Jack jump over the candle stick"

# 如果不想数参数，可以用关键字
"{name} wants to eat {food}".format(name="Bob", food="lasagna") 
# => "Bob wants to eat lasagna"

# 如果你的Python3程序也要在Python2.5以下环境运行，也可以用老式的格式化语法
"%s can be %s the %s way" % ("strings", "interpolated", "old")

# None是一个对象
None  # => None

# 当与None进行比较时不要用 ==，要用is。is是用来比较两个变量是否指向同一个对象。
"etc" is None  # => False
None is None  # => True

# None，0，空字符串，空列表，空字典都算是False
# 所有其他值都是True
bool(0)  # => False
bool("")  # => False
bool([]) # => False
bool({}) # => False
</code></pre>
