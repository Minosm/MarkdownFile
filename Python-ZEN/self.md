#### juself是指向对象（实例化后的类）自身的指针

- self.

在当前对象的空间中去

指向当前对象的内存地址

self是推荐关键字，可以不用self，换成其他的（不过一定要有，是面向对象的体现）

类似于“this”

确保访问自己对象的数据

self在定义时不可省略；



---

类变量和实例变量；

self就是区分这个的？



regular python tutor

“类变成的这个实例”



共享类变量，可变，列表，指针，

所以不应该使用类变量（可变），实例使用的话，会互相影响

---

```python
class A:
    def __init__(self,x):
        print(x)
a = A(5)
```

类的传参



class 派生类名(基类名)：

类的继承才有（）

可以把父类放在元组里多继承；

foo = fuck oriented object

包括了术语'foo','bar' 或'foobar'作为伪变量而没有任何适当的解释或定义。这可能被认为是微不足道的，但一些新来者，特别是那些非英语国家的人，在理解这些术语时会遇到 困难。本文纠正这一问题

---

​	、

STEM 理工科的统称（science，technology，engineering，math）

Everything被视为维基百科的前身，而Everything中也包含了大量Jargon File的内容

everything是jargon file



> ### 单下划线、双下划线、头尾双下划线说明：
>
> - **__ foo __**: 定义的是特殊方法，一般是系统定义名字 ，类似 **__ init __()** 之类的。
> - **_ foo**: 以单下划线开头的表示的是 protected 类型的变量，即保护类型只能允许其本身与子类进行访问，不能用于 **from module import \***
> - **__foo**: 双下划线的表示的是私有类型(private)的变量, 只能是允许这个类本身进行访问了。



- **import 模块**：导入一个模块；注：相当于导入的是一个文件夹，是个相对路径。

- **from…import**：导入了一个模块中的一个函数；注：相当于导入的是一个文件夹中的文件，是个绝对路径。

  **from…import \***：是把一个模块中所有函数都导入进来; 注：相当于：相当于导入的是一个文件夹中所有文件，所有函数都是绝对路径。（

  可以直接使用函数，不需要" . "

推荐使用 import 语句，避免使用 from … import，因为这样可以使你的程序更加易读，也可以避免名称冲突



> ```python
> import 模块名
> 模块名.xxx = 引用
> 
> from 模块名 import *
> xxx = 拷贝  # 能修改属性值　　
> ```

- from 模块 import * : 导入模块时，会跳过私有属性;
- import 模块 : 通过引用可以访问私有属性





Python 解释器执行代码时，有一些内建、隐含的变量，`__name__`就是其中之一，其意义是“模块名称”

如果该模块是被引用，那么`__name__`的值会是此模块的名称；如果该模块是直接被执行，那么`__name__`的值是`__main__`



> 对比两段程序运行结果可发现，当直接运行包含main函数的程序时，main函数会被执行，同时程序的__name__变量值为'__main__'。
>
> 当包含有main函数的程序被作为module被import时，该module程序(print_main_function.py)对应的__name__变量值为该module对应的函数名称，因此该module程序（print_main_function.py）中的main函数不会被执行。

python程序是逐行执行的



src = source   源
dst = destination 目的