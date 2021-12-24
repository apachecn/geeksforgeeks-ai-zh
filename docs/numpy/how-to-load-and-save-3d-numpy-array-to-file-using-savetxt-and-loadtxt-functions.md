# 如何使用 savetxt()和 loadtxt()函数将 3D Numpy 数组加载保存到文件中？

> 原文:[https://www . geeksforgeeks . org/如何使用-save txt-和-loadtxt-functions 加载和保存-3d-numpy-数组到文件/](https://www.geeksforgeeks.org/how-to-load-and-save-3d-numpy-array-to-file-using-savetxt-and-loadtxt-functions/)

**前提条件:**[【num py . save txt()](https://www.geeksforgeeks.org/numpy-savetxt/)、[【num py . load txt()](https://www.geeksforgeeks.org/numpy-loadtxt-in-python/)

**Numpy.savetxt()** 是 Numpy 库中 python 中的一种方法，用于将 1D 和 2D 数组保存到文件中。

> **语法:** numpy.savetxt(fname，X，fmt='%.18e '，分隔符= ' '，换行符='\n '，页眉= "，页脚= "，注释='# '，编码=None)

**numpy.loadtxt()** 是 numpy 库中 python 中的一种方法，用于从文本文件中加载数据，以便更快地读取。

> **语法:** numpy.loadtxt(fname，dtype='float '，comments='# '，分隔符=None，converters=None，skiprows = 0，usecols=None，unpack=False，ndmin=0)

## **保存和加载三维数组**

如前所述，我们只能在 numpy.savetxt()中使用 1D 或 2D 数组，如果我们使用更多维度的数组，它将抛出一个**值错误–**预期的 1D 或 2D 数组，而是得到了 3D 数组。因此，我们需要找到一种保存和检索的方法，至少对于 3D 数组来说是这样，下面是如何通过使用一些 Python 技巧来做到这一点的。

*   **第一步:**将 3D 阵重塑为 2D 阵。
*   **步骤 2:** 将该数组插入文件
*   **第三步:**从文件加载数据显示
*   **第 4 步:**转换回原来的形状数组

**示例:**

## 蟒蛇 3

```py
import numpy as gfg

arr = gfg.random.rand(5, 4, 3)

# reshaping the array from 3D
# matrice to 2D matrice.
arr_reshaped = arr.reshape(arr.shape[0], -1)

# saving reshaped array to file.
gfg.savetxt("geekfile.txt", arr_reshaped)

# retrieving data from file.
loaded_arr = gfg.loadtxt("geekfile.txt")

# This loadedArr is a 2D array, therefore
# we need to convert it to the original
# array shape.reshaping to get original
# matrice with original shape.
load_original_arr = loaded_arr.reshape(
    loaded_arr.shape[0], loaded_arr.shape[1] // arr.shape[2], arr.shape[2])

# check the shapes:
print("shape of arr: ", arr.shape)
print("shape of load_original_arr: ", load_original_arr.shape)

# check if both arrays are same or not:
if (load_original_arr == arr).all():
    print("Yes, both the arrays are same")
else:
    print("No, both the arrays are not same")
```

**输出:**

```py
shape of arr:  (5, 4, 3)
shape of load_original_arr:  (5, 4, 3)
Yes, both the arrays are same
```