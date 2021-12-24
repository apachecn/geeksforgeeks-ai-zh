# Python 中的 numpy.load()

> 原文:[https://www.geeksforgeeks.org/numpy-load-in-python/](https://www.geeksforgeeks.org/numpy-load-in-python/)

**`numpy.load()`** 函数从扩展名为(npy)的磁盘文件中返回输入数组。npy)。

> **语法:** numpy.load(file，mmap_mode=None，allow_pickle=True，fix_imports=True，编码='ASCII ')
> 
> **参数:**
> **文件:**:类似文件的对象、字符串或 pathlib。路径。要读取的文件。类似文件的对象必须支持 seek()和 read()方法。
> **mmap_mode :** 如果不是无，则使用给定的模式对文件进行内存映射(模式的详细描述见 numpy.memmap】)。
> **allow_pickle :** 允许加载存储在 npy 文件中的酸洗对象数组。
> **fix_imports :** 仅在 Python 3 上加载 Python 2 生成的腌制文件时有用，其中包括包含对象数组的 npy/npz 文件。
> **编码:**仅在 Python 3 中加载 Python 2 生成的腌制文件时有用，其中包括包含对象数组的 npy/npz 文件。
> 
> **返回:**文件中存储的数据。为了。对于 npz 文件，必须关闭 NpzFile 类的返回实例，以避免泄漏文件描述符。

**代码#1:工作**

```
# Python program explaining 
# load() function 

import numpy as geek

a = geek.array(([i + j for i in range(3) 
                       for j in range(3)]))
# a is printed.
print("a is:")
print(a)

geek.save('geekfile', a)
print("the array is saved in the file geekfile.npy")

# the array is saved in the file geekfile.npy 
b = geek.load('geekfile.npy')

# the array is loaded into b
print("b is:")
print(b)

# b is printed from geekfile.npy
print("b is printed from geekfile.npy")
```

**输出:**

```
a is:
[0, 1, 2, 1, 2, 3, 2, 3, 4]
the array is saved in the file geekfile.npy
b is:
[0, 1, 2, 1, 2, 3, 2, 3, 4]
b is printed from geekfile.npy

```

**代码#2:**

```
# Python program explaining 
# load() function 

import numpy as geek

# a and b are numpy arrays.
a = geek.array(([i + j for i in range(3) 
                       for j in range(3)]))
b = geek.array([i + 1 for i in range(3)])

# a and b are printed.
print("a is:")
print(a)
print("b is:")
print(b)

# a and b are stored in geekfile.npz
geek.savez('geekfile.npz', a = a, b = b)

print("a and b are stored in geekfile.npz")

# compressed file is loaded
c = geek.load('geekfile.npz')

print("after loading...")
print("a is:", c['a'])
print("b is:", c['b'])
```

**输出:**

```
a is:
[0 1 2 1 2 3 2 3 4]
b is:
[1 2 3]
a and b are stored in geekfile.npz
after loading...
a is: [0 1 2 1 2 3 2 3 4]
b is: [1 2 3]

```