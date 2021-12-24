# Python 中的 sklearn.metrics.max_error()函数

> 原文:[https://www . geesforgeks . org/sklearn-metrics-max _ error-function-in-python/](https://www.geeksforgeeks.org/sklearn-metrics-max_error-function-in-python/)

max_error()函数计算最大残差。捕捉预测值和真实值之间最坏情况误差的指标。此函数比较列表、元组或数据框的每个元素(按索引方式)，并返回不匹配元素的计数。

> **语法:**sklearn . metrics . max _ error(y _ true，y_pred)
> 
> **参数:**
> 
> **y_true** :接受真实(正确)的目标值。
> 
> **y_pred:** 接受估算目标值。
> 
> **返回:**
> 
> **max _ error:<***float**>**T5:【一个正浮点值。*

**例 1:**

## 蟒蛇 3

```
# Import required module
from sklearn.metrics import max_error

# Assign data
y_true = [6, 2, 5, 1]
y_pred = [4, 2, 7, 1]

# Compute max_error
print(max_error(y_true, y_pred))
```

**输出:**

```
2

```

在上例中，列表 *y_true* 和 *y_pred* 中的元素仅在索引 0 和 2 处不同。因此，2 是*最大误差*。

**例 2:**

## 蟒蛇 3

```
# Import required module
from sklearn.metrics import max_error

# Assign data
y_true = [3.13,'GFG',56,57667]
y_pred = ['Geeks','for','Geeks',3000]

# Compute max_error
print(max_error(y_true, y_pred))
```

**输出:**

> UFuncTypeError: ufunc“减法”不包含带有签名的循环
> 匹配类型(dtype(' T1 ' U32 ')、dtype(' T2 ' U32 ')->dtype(' T4 ' U32 ')

为了使用 *max_error()，*列表、元组、数据帧等的元素。应该是类似的类型。

**例 3:**

## 蟒蛇 3

```
# Import required module
from sklearn.metrics import max_error

# Assign data
List = [1, 2, 3, 4, 5, 6, 7, 8, 9]
y_true = List
y_pred = List[::-1]

# Compute max_error
print(max_error(y_true, y_pred))
```

**输出:**

```
8

```

这里只有一个匹配的元素。