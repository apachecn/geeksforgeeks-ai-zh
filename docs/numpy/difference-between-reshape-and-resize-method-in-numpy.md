# Numpy

中整形()和调整大小()方法的区别

> 原文:[https://www . geeksforgeeks . org/numpy 中的整形和调整大小方法的区别/](https://www.geeksforgeeks.org/difference-between-reshape-and-resize-method-in-numpy/)

无论是**[**numpy . resize()**](https://www.geeksforgeeks.org/numpy-reshape-python/)还是**[**NumPy . resize()**](https://www.geeksforgeeks.org/python-numpy-numpy-resize/)**方法都是用来改变 NumPy 数组的大小。它们之间的区别在于 resize()方法不改变原始数组，只返回改变后的数组，而 resize()方法不返回任何内容，直接改变原始数组。******

********示例 1:** 使用重塑()******

 ****## 蟒蛇 3

```
# importing the module
import numpy as np 

# creating an array 
gfg = np.array([1, 2, 3, 4, 5, 6]) 
print("Original array:")
display(gfg)  

# using reshape()
print("Changed array")
display(gfg.reshape(2, 3)) 

print("Original array:")
display(gfg)
```****