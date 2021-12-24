# Python 中的 numpy.char.add()函数

> 原文:[https://www . geesforgeks . org/numpy-char-add-function-in-python/](https://www.geeksforgeeks.org/numpy-char-add-function-in-python/)

NumPy 模块中 char 类的 add()方法用于两个字符串或 unicode 数组的元素级字符串连接。

### num py . char . add()

> ***语法:** numpy.char.add(x1，x2)*
> ***参数:***
> 
> *   ***x1 :** 第一个要连接的数组(开始连接)*
> *   ***x2 :** 第二个要串接的数组(串接在最后)*
> 
> ***返回:**字符串或 unicode 数组*

**示例 1 :** 在 2 个单元素字符串数组上使用该方法。

## 蟒蛇 3

```
# importing the module
import numpy as np

# create the arrays
x1 = ['Hello']
x2 = ['World']
print("The arrays are : ")
print(x1)
print(x2)

# using the char.add() method
result = np.char.add(x1, x2)
print("\nThe concatenated array is :")
print(result)
```