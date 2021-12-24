# Python 中的 numpy.char.multiply()函数

> 原文:[https://www . geesforgeks . org/numpy-char-multiply-function-in-python/](https://www.geeksforgeeks.org/numpy-char-multiply-function-in-python/)

NumPy 模块中 char 类的乘法()方法用于元素方式的 字符串多重连接。

### num py . char . multiply()

> ***语法:** numpy.char.multiply(a，i)*
> ***参数:***
> 
> *   ***一个:**字符串或 unicode 数组*
> *   ***i :** 重复次数*
> 
> ***返回:**字符串数组*

**示例 1 :** 在单元素字符串数组上使用方法。

## 蟒蛇 3

```
# importing the module
import numpy as np

# created an array
arr1 = np.array(['Geeks'])
print("Original Array :")
print(arr1)

# number of times to be repeated
i = 3

# using the char.multiply() method
arr2 = np.char.multiply(arr1, i)
print("\nNew array :")
print(arr2)
```