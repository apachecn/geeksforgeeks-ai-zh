# num py . mint type code()函数–python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py minty type code-function-python/

**`numpy.mintypecode()`** 函数返回给定类型可以安全转换到的最小尺寸类型的字符。

> **语法:**num py . minty type code(type chars，typeset = 'GDFgdf '，default = 'd '))
> 
> **参数:**
> **类型字符:**【字符串或数组列表 _like】如果是字符串列表，每个字符串应该代表一个数据类型。如果是 array_like，则使用数组数据类型的字符表示。
> **排版:**【字符串或字符串列表，可选】选择返回字符的字符集。默认设置为“GDFgdf”。
> **默认:**【str，可选】默认字符，如果 typechars 中没有字符与排版中的字符匹配，则返回该字符。
> **返回:**【字符串】代表找到的最小大小类型的字符。

**代码#1 :**

```
# Python program explaining
# numpy.mintypecode() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.mintypecode(['d', 'f', 'S'])

print (gfg)
```

**输出:**

```
d

```

**代码#2 :**

```
# Python program explaining
# numpy.mintypecode() function

# importing numpy as geek 
import numpy as geek 

x = geek.array([1.1, 2-1.j])

gfg = geek.mintypecode(x)

print (gfg)
```

**输出:**

```
D

```