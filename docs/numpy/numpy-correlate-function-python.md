# numpy.correlate()函数–Python

> 原文:[https://www . geeksforgeeks . org/numpy-correlate-function-python/](https://www.geeksforgeeks.org/numpy-correlate-function-python/)

**`numpy.correlate()`** 函数定义了两个一维序列的互相关。该函数计算信号处理文本中通常定义的相关性:c _ { av }[k]= sum _ n a[n+k]* conj(v[n])

> **语法:** numpy.correlate(a，v，mode = 'valid ')
> 
> **参数:**
> **a、v :** 【阵 _ 象】输入序列。
> **模式:** [{ '有效'，'相同'，'完整' }，可选]参考卷积文档字符串。默认值为“有效”。
> 
> **返回:**【n 数组】a 和 v 的离散互相关

**代码#1 :**

```
# Python program explaining
# numpy.correlate() function

# importing numpy as geek 
import numpy as geek 

a = [2, 5, 7]
v = [0, 1, 0.5]

gfg = geek.correlate(a, v)

print (gfg)
```

**输出:**

```
[8.5]

```

**代码#2 :**

```
# Python program explaining
# numpy.correlate() function

# importing numpy as geek 
import numpy as geek 

a = [2, 5, 7]
v = [0, 1, 0.5]

gfg = geek.correlate(a, v, "same")

print (gfg)
```

**输出:**

```
[4.5 8.5 7\. ]

```