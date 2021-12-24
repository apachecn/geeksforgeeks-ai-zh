# NumPy 数组相对于 Python 数组的优势

> 原文:[https://www . geeksforgeeks . org/numpy-arrays-over-python-arrays/](https://www.geeksforgeeks.org/benefit-of-numpy-arrays-over-python-arrays/)

当我们使用多维数组时，对 NumPy 的需求就产生了。传统的数组模块不支持多维数组。

让我们首先尝试在 Python 中创建一维数组(即一行多列)，而不安装 NumPy Package 以获得更清晰的图片。

## 蟒 3

```
from array import *

arr = array('i', [25, 16, 3])
print(arr)
```