# 如何用 Python 中的 SciPy 找到一个数的阶乘？

> 原文:[https://www . geesforgeks . org/如何使用 python 中的 scipy 找到阶乘 OS-a-number/](https://www.geeksforgeeks.org/how-to-find-the-factorial-os-a-number-using-scipy-in-python/)

SciPy 是一个开源的 Python 库，用于解决科学和数学问题。它建立在 NumPy 上，允许我们使用各种高级命令进行操作和可视化。Scipy 还提供了一个 **scipy.special .阶乘()**函数来计算任意数字的阶乘。

## scipy.special .阶乘()

该函数接受两个参数，int 或 array_like of int 另一个布尔值，并根据布尔值将给定参数的阶乘作为整数或浮点数返回。

> **语法:** scipy.special.factorial(n，exact=False)
> 
> **参数:**
> 
> **n** : int 或类似 int 的数组
> 
> **精确** ： 布尔值， 可选
> 
> **返回:**
> 
> **nf** :浮点或整数或数组(输出取决于精确值)。

**注意:**如果精确为真，则返回整数值，如果为假，则使用伽马函数返回浮点值，默认值为假。

**例 1:**

## 蟒蛇 3

```
# importing module
from scipy.special import factorial

print(factorial(3))

# False always return float value
print(factorial(4, exact=False))
```