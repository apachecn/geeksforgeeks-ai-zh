# python 中的 numpy.loadtxt()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-load txt-in-python/

Python 中的 **`numpy.load()`** 用于从文本文件中加载数据，目的是成为简单文本文件的快速阅读器。

请注意，文本文件中的每一行必须具有相同数量的值。

> **语法:** numpy.loadtxt(fname，dtype='float '，comments='# '，分隔符=None，converters=None，skiprows = 0，usecols=None，unpack=False，ndmin=0)
> 
> **参数:**
> **fname :** 要读取的文件、文件名或生成器。如果文件扩展名为。gz 或. bz2，文件首先被解压缩。请注意，生成器应该为 Python 3k 返回字节字符串。
> **数据类型:**结果数组的数据类型；默认值:float。如果这是一个结构化的数据类型，结果数组将是一维的，并且每一行都将被解释为数组的一个元素。
> **分隔符:**用于分隔值的字符串。默认情况下，这是任何空白。
> **转换器:**将列号映射到将该列转换为浮点数的函数的字典。例如，如果列 0 是日期字符串:converters = {0: datestr2num}。默认值:无。
> **Skip prows:**跳过第一个 Skip prows 行；默认值:0。
> 
> **返回:**正常

**代码#1:**

```py
# Python program explaining 
# loadtxt() function
import numpy as geek

# StringIO behaves like a file object
from io import StringIO   

c = StringIO("0 1 2 \n3 4 5")
d = geek.loadtxt(c)

print(d)
```

**输出:**

```py
[[ 0\.  1\.  2.]
 [ 3\.  4\.  5.]]
```

**代码#2:**

```py
# Python program explaining 
# loadtxt() function
import numpy as geek

# StringIO behaves like a file object
from io import StringIO   

c = StringIO("1, 2, 3\n4, 5, 6")
x, y, z = geek.loadtxt(c, delimiter =', ', usecols =(0, 1, 2), 
                                                unpack = True)

print("x is: ", x)
print("y is: ", y)
print("z is: ", z)
```

**输出:**

```py
x is:  [ 1\.  4.]
y is:  [ 2\.  5.]
z is:  [ 3\.  6.]
```

**代码#3:**

```py
# Python program explaining 
# loadtxt() function
import numpy as geek

# StringIO behaves like a file object
from io import StringIO   

d = StringIO("M 21 72\nF 35 58")
e = geek.loadtxt(d, dtype ={'names': ('gender', 'age', 'weight'),
                                  'formats': ('S1', 'i4', 'f4')})

print(e)
```

**输出:**

```py
[(b'M', 21,  72.) (b'F', 35,  58.)]

```