# sciPy stats.gmean()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-gmean-function-python/](https://www.geeksforgeeks.org/scipy-stats-gmean-function-python/)

**scipy.stats.gmean(array，axis=0，dtype=None)** 计算数组元素沿数组指定轴的几何平均值(python 中的列表)。
是配方–

![](img/8c0c930d575b75e0ba70b526184b7dbb.png)

> **参数:**
> **数组:**输入具有计算几何平均值元素的数组或对象。
> **轴:**计算平均值的轴。默认轴= 0
> **数据类型:**设置返回元素的类型。
> **根据设定的参数返回:**数组元素的几何平均值。

**代码#1:**

## 蟒蛇 3

```
# Geometric Mean

from scipy.stats.mstats import gmean
arr1 = gmean([1, 3, 27])

print("Geometric Mean is :", arr1)
```

**Output:** 

```
Geometric Mean is : 4.32674871092
```

**代码#2:** 带多维数据

## 蟒蛇 3

```
# Geometric Mean

from scipy.stats.mstats import gmean
arr1 = [[1, 3, 27],
        [3, 4, 6],
        [7, 6, 3],
        [3, 6, 8]]

print("Geometric Mean is :", gmean(arr1))

# using axis = 0
print("\nGeometric Mean is with default axis = 0 : \n",
      gmean(arr1, axis = 0))

# using axis = 1
print("\nGeometric Mean is with default axis = 1 : \n",
      gmean(arr1, axis = 1)) 
```

**Output:** 

```
Geometric Mean is : [ 2.81731325  4.55901411  7.89644408]

Geometric Mean is with default axis = 0 : 
 [ 2.81731325  4.55901411  7.89644408]

Geometric Mean is with default axis = 1 : 
 [ 4.32674871  4.16016765  5.01329793  5.24148279]
```