# 如何将 NumPy 数组设为只读？

> 原文:[https://www . geesforgeks . org/how-to-make-a-numpy-array-只读/](https://www.geeksforgeeks.org/how-to-make-a-numpy-array-read-only/)

我们来讨论一下如何让 NumPy 数组不可变，即不可重写或不可更改。这可以通过将 NumPy 数组的可写标志设置为 false 来实现。

**语法:**

```py
array.flags.writable=False
```

这将可写标志设置为假，因此数组变成不可变的，即只读。请看下面的例子

**例:**

## 蟒蛇

```py
import numpy as np

a = np.zeros(11)
print("Before any change ")
print(a)

a[1] = 2
print("Before after first change ")
print(a)

a.flags.writable = False
print("After making array immutable on attempting  second change ")
a[1] = 7
```

**输出:**

```py
Before any change
[0\. 0\. 0\. 0\. 0\. 0\. 0\. 0\. 0\. 0\. 0.]
Before after first change
[0\. 2\. 0\. 0\. 0\. 0\. 0\. 0\. 0\. 0\. 0.]
After making array immutable on attempting  second change
Traceback (most recent call last):
  File "gfg9.py", line 11, in <module>
    a[1]=7
ValueError: assignment destination is read-only
```