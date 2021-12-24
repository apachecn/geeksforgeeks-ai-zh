# Python | sympy.compositepi()方法

> 原文:[https://www . geesforgeks . org/python-sympy-composite pi-method/](https://www.geeksforgeeks.org/python-sympy-compositepi-method/)

借助 **sympy.compositepi()** 方法，我们可以求出小于或等于给定数目的合成数。

> **语法:** compositepi(n)
> 
> **参数:**
> **n–**表示计算合成数的个数。
> 
> **返回:**返回小于或等于 **n** 的合成数。

**示例#1:**

```py
# import compositepi() method from sympy
from sympy import compositepi

n = 10

# Use compositepi() method 
count_composites = compositepi(n) 

print("The number of composites numbers less than or equal to {} is {}".format(n, count_composites))
```

**输出:**

```py
The number of composites numbers less than or equal to 10 is 5

```

**例 2:**

```py
# import compositepi() method from sympy
from sympy import compositepi

n = 100

# Use compositepi() method 
count_composites = compositepi(n) 

print("The number of composites numbers less than or equal to {} is {}".format(n, count_composites))          
```

**输出:**

```py
The number of composites numbers less than or equal to 100 is 74

```