# num py . save()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-save/

**`numpy.save()`** 功能用于将输入数组存储在扩展名为(npy)的磁盘文件中。npy)。

> **语法:** numpy.save(文件，arr，allow_pickle=True，fix_imports=True)
> 
> **参数:**
> **文件:**:保存数据的文件或文件名。如果文件是字符串或路径，如果文件名还没有扩展名，则将在文件名后附加一个. npy 扩展名。如果文件是一个文件对象，那么文件名不变。
> **允许 _pickle :** :允许使用 Python pickles 保存对象数组。不允许腌菜的原因包括安全性(加载腌菜数据可以执行任意代码)和可移植性(腌菜对象可能无法在不同的 Python 安装上加载)。默认值:真
> **fix_imports :** 仅适用于强制 Python 3 上对象数组中的对象以 Python 2 兼容的方式进行酸洗。
> **arr :** 待保存的数组数据。
> 
> **返回:**将输入数组存储在扩展名为(npy)的磁盘文件中。npy)。

**代码#1:工作**

```py
# Python program explaining 
# save() function 

import numpy as geek

a = geek.arange(5)

# a is printed.
print("a is:")
print(a)

# the array is saved in the file geekfile.npy 
geek.save('geekfile', a)

print("the array is saved in the file geekfile.npy")

```

**输出:**

```py
a is:
[0 1 2 3 4]
the array is saved in the file geekfile.npy

```

**代码#2**

```py
# Python program explaining 
# save() function 

import numpy as geek

# the array is loaded into b
b = geek.load('geekfile.npy')

print("b is:")
print(b)

# b is printed from geekfile.npy
print("b is printed from geekfile.npy")
```

**输出:**

```py
b is:
[0 1 2 3 4]
b is printed from geekfile.npy

```