# numpy.outer()函数–Python

> 原文:[https://www.geeksforgeeks.org/numpy-outer-function-python/](https://www.geeksforgeeks.org/numpy-outer-function-python/)

**`numpy.outer()`** 函数计算两个向量的外积。

> **语法:** numpy.outer(a，b，out =无)
> 
> **参数:**
> **a :** 【阵 _ 象】第一个输入向量。如果输入还不是一维的，则将其展平。
> **b:**【array _ like】第二输入向量。如果输入还不是一维的，则将其展平。
> **out:**【n 数组，可选】存储结果的位置。
> 
> **返回:**【ndarray】返回两个向量的外积。out[i，j] = a[i] * b[j]

**代码#1 :**

```
# Python program explaining
# numpy.outer() function

# importing numpy as geek 
import numpy as geek 

a = geek.ones(4)
b = geek.linspace(-1, 2, 4)

gfg = geek.outer(a, b)

print (gfg)
```

**输出:**

```
[[-1\.  0\.  1\.  2.]
 [-1\.  0\.  1\.  2.]
 [-1\.  0\.  1\.  2.]
 [-1\.  0\.  1\.  2.]]

```

**代码#2 :**

```
# Python program explaining
# numpy.outer() function

# importing numpy as geek 
import numpy as geek 

a = geek.ones(5)
b = geek.linspace(-2, 2, 5)

gfg = geek.outer(a, b)

print (gfg)
```

**输出:**

```
[[-2\. -1\.  0\.  1\.  2.]
 [-2\. -1\.  0\.  1\.  2.]
 [-2\. -1\.  0\.  1\.  2.]
 [-2\. -1\.  0\.  1\.  2.]
 [-2\. -1\.  0\.  1\.  2.]]

```