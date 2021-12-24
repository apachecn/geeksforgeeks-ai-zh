# sciPy stats.variation()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-variation-function-python/](https://www.geeksforgeeks.org/scipy-stats-variation-function-python/)

`**scipy.stats.variation(arr, axis = None)**`函数计算变异系数。它被定义为标准差与平均值之比。

> **参数:**
> **arr:**【array _ like】输入数组。
> **轴:**【int 或 int 的元组】轴，我们要沿此轴计算变异系数。
> - >轴= 0 沿柱变异系数。
> - >轴= 1 个沿行工作的变异系数。
> 
> **结果:**数组随指定轴数值的变异系数。

**代码#1:** 变异的使用()

```py
from scipy.stats import variation 
import numpy as np

arr = np.random.randn(5, 5)

print ("array : \n", arr)

# rows: axis = 0, cols: axis = 1

print ("\nVariation at axis = 0: \n", variation(arr, axis = 0))

print ("\nVariation at axis = 1: \n", variation(arr, axis = 1))
```

**Output:**

```py
array : 
 [[-1.16536706 -1.29744691 -0.39964651  2.14909277 -1.00669835]
 [ 0.79979681  0.91566149 -0.823054    0.9189682  -0.01061181]
 [ 0.9532622   0.38630077 -0.79026789 -0.70154086  0.79087801]
 [ 0.53553389  1.46409899  1.89903817 -0.35360202 -0.14597738]
 [-1.53582875 -0.50077039 -0.23073327  0.32457064 -0.43269088]]

Variation at axis = 0: 
 [-12.73042404   5.10272979 -14.6476392    2.15882202  -3.64031032]

Variation at axis = 1: 
 [-3.73200773  1.90419038  5.77300406  1.29451485 -1.27228112]

```

**代码#2:** 如何实现无变异()

```py
import numpy as np

arr = np.random.randn(5, 5)

print ("array : \n", arr)

# this function works similar to variation()
cv = lambda x: np.std(x) / np.mean(x)

var1 = np.apply_along_axis(cv, axis = 0, arr = arr)
print ("\nVariation at axis = 0: \n", var1)

var2 = np.apply_along_axis(cv, axis = 1, arr = arr)
print ("\nVariation at axis = 0: \n", var2)
```

**Output:**

```py
array : 
 [[ 0.51268414 -1.93697931  0.41573223  2.14911168  0.15036631]
 [-0.50407207  1.51519879 -0.42217231 -1.09609322  1.93184432]
 [-1.07727163  0.27195529 -0.1308108  -1.75406388  0.94046395]
 [ 1.23283059 -0.03112461  0.59725109  0.06671002 -0.97537666]
 [ 1.1233506   0.97658799 -1.10309113 -1.33142901 -0.28470146]]

Variation at axis = 0: 
 [ 3.52845174  7.40891024 -4.74078192 -3.57928544  2.85092056]

Variation at axis = 0: 
 [ 5.04874565  4.22763514 -2.74104828  4.10772935 -8.24126977]

```