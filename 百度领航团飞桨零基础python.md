首先我们来安装python的环境

课程的老师介绍了三种安装方式，一种是直接安装python的本体，第二种是安装Anaconda，第三种是AI Studio

在安装完环境之后，我们第一个事情是执行第一个Python的程序。使用百度的AI studio的基本方法是使用cell，然后在编辑模式和命令模式下执行我们第一段python代码。

标识符命名规则

简单地理解，标识符就是一个名字，就好像我们每个人都有属于自己的名字，它的主要作用就是作为变量、函数、类、模块以及其他对象的名称
Python 中标识符的命名不是随意的，而是要遵守一定的命令规则，比如说：标识符是由字符（A~Z 和 a~z）、下划线和数字组成，但第一个字符不能是数字。 标识符不能和 Python 中的保留字相同。 Python中的标识符中，不能包含空格、@、% 以及 $ 等特殊字符。 在 Python 中，标识符中的字母是严格区分大小写的
数据类型间的相互转化

pythonint(2.5)str(4)bool(3) # 非0： Ture 其它 Falsefloat('0.6')

组合数据类型列表list，这一种有序的集合可以随时添加和删除其中的元素。

pythonlist1 = [1, 2, 3, 4, 5 ]list2 = ["a", "b", "c", "d","e","f"]list3 = ['physics', 'chemistry', 1997, 2000]len(list1)list1[4]list3.append(5)list1.pop()

元组是另一种有序列表。元组与列表非常相似，但是元组初始化就不能修改。

pythontuple1 = (1, 2, 3, 4, 5 )tuple2 = ("a", "b", "c", "d","e","f")tuple3 = ('physics', 'chemistry', 1997, 2000)len(tuple1)

可变对象，不可变对象

可变对象：list dict set

不可变对象：tuple string int float bool

字典dictPython内置了字典：dict的支持，dict全称dictionary，在其他语言中也称为map，使用键-值（key-value）存储，具有极快的查找速度。pythonword = {'apple':'苹果','banana':'香蕉'}scores = {'小张':100, '小李':80}grad = {4:'很好',3: '好',2:'中',1:'差',0:'很差'}

集合 setset和dict类似，也是一组key的集合，但不存储value。由于key不能重复，所以，在set中，没有重复的key。字符串索引、切片切片的语法：[起始:结束:步长] 字符串[start: end: step] 这三个参数都有默认值，默认截取方向是从左往右的 start:默认值为0； end : 默认值未字符串结尾元素； step : 默认值为1；如果切片步长是负值，截取方向则是从右往左的
字符串常用函数count计数，find查找，index查找，split字符串拆分，replace字符串替换，strip字符串标准化，字符串变形upper，lower，capitalize

生成器
通过列表生成式，我们可以直接创建一个列表。但是，受到内存限制，列表容量肯定是有限的。而且，创建一个包含100万个元素的列表，不仅占用很大的存储空间，如果我们仅仅需要访问前面几个元素，那后面绝大多数元素占用的空间都白白浪费了。

异常即是一个事件，该事件会在程序执行过程中发生，影响了程序的正常执行。
一般情况下，在 Python 无法正常处理程序时就会发生一个异常。异常是 Python 对象，表示一个错误。当 Python 脚本发生异常时我们需要捕获处理它，否则程序会终止执行。

try 的工作原理是，当开始一个 try 语句后，Python 就在当前程序的上下文中作标记，这样当异常出现时就可以回到这里，try 子句先执行，接下来会发生什么依赖于执行时是否出现异常。
如果当 try 后的语句执行时发生异常，Python 就跳回到 try 并执行第一个匹配该异常的 except 子句，异常处理完毕，控制流就通过整个 try 语句（除非在处理异常时又引发新的异常）。如果在 try 后的语句里发生了异常，却没有匹配的 except 子句，异常将被递交到上层的 try，或者到程序的最上层（这样将结束程序，并打印缺省的出错信息）。

参数传递位置参数，缺省参数，可变参数，关键字参数，命名关键字参数，位置参数位置参数是最简单的一种函数调用的方式。位置参数须以正确的顺序传入函数、数量必须和声明时的一样。

参数传递

位置参数，缺省参数，可变参数，关键字参数，命名关键字参数，位置参数

位置参数是最简单的一种函数调用的方式。位置参数须以正确的顺序传入函数、数量必须和声明时的一样。

使用类的好处

降低复杂性-》更少的bug-》提高可维护行类可以将数据与函数绑定在一起，使代码模块化调用数据和函数，使用对象名.的方式，使代码更加优雅

如何定义类class Athlete:第一部分：class定义类的关键字，Athlete符合python标识符命名规则，：表示类内容的开始def init(self,a_name,a_dob=None,a_times=[]):第二部分：def定义函数的关键字，init 方法是一个特殊方法会在实例化对象时自动调用，我们会在这个方法中对数据进行赋值。self作为类中函数的第一个参数，方便该方法调用该类的其他属性和方法。第三部分：自定义的属性和方法如何使用类1.创建对象对象名 = 类名(参数)2.使用.调用类的方法和属性对象.属性名对象.方法名()类方法是所有对象共享方法。如何使用：定义：方法定义时，使用@classmethod标记调用：类名.类方法对象.类方法私用的属性和方法的定义：在属性和方法名前加 __ 两个下划线如何调用:只能通过类中的方法来调用私有的属性和方法继承与方法的重写定义：

class 子类名(父类名)：

情况1，如果子类有新增的属性，那么需要在子类__init方法中，调用父类的__init__

情况2，如果子类没有新增的属性,子类不需要写__init__方法使用：对象名 = 子类名(参数)继承的好处：代码重用，升级功能（重写），新增功能（新的方法）方法重写子类方法与父类方法完全相同，子类若重写了父类的方法，则子类对象调用方法时就是调用的自己类中重新的方法。
