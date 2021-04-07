## 描述：

enumerate() 函数用于将一个可遍历的数据对象(如列表、元组或字符串)组合为一个索引序列，同时列出数据和数据下标，一般用在 for 循环当中。

因为contours也是迭代器类型（可遍历），所以也支持enumerate（）

Python 2.3. 以上版本可用，2.6 添加 start 参数。

#### 普通用法：

~~~python
enumerate(sequence, [start=0])
~~~

- 用于把list、元组、字符串加上索引/变为字典

- sequence -- 一个序列、迭代器或其他支持迭代对象

- 返回 enumerate(枚举) 对象

  - 可能需要list（）一下

  - dict([],[]) 可将两个list转换为字典

    - #### 也可以dict(enumerate(sequence, [start=x]))

    - 直接把序列转换为字典

#### 在for循环中：

~~~python
>>>seq = ['one', 'two', 'three']
>>> for i, element in enumerate(seq):
...     print i, element
... 
0 one
1 two
2 three
~~~

可以把序列和值一起输出







