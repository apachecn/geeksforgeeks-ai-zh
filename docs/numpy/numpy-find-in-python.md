# Python 中的 numpy.find()

> 原文:[https://www.geeksforgeeks.org/numpy-find-in-python/](https://www.geeksforgeeks.org/numpy-find-in-python/)

**`numpy.core.defchararray.find(arr, substring, start=0, end=None)` :** 查找指定范围内子字符串的最低索引。

> **参数:**
> **arr :** 数组状或字符串待搜索。
> **子串:**要搜索的子串。
> **开始，结束:**【int，可选】搜索范围。
> 
> **返回:**找到的子串索引最低的整数数组。

**代码#1:**

```py
# Python Program illustrating 
# numpy.char.find() method 
import numpy as np 

arr = ['vdsdsttetteteAAAa', 'AAAAAAAaattttds', 'AAaaxxxxtt', 'AAaaXDSDdscz']

print ("arr : ", arr)

print ("\nfind of 'tt'", np.char.find(arr, 'tt'))
print ("find of 'tt'", np.char.find(arr, 'tt', start = 0))
print ("find of 'tt'", np.char.find(arr, 'tt', start = 8))
```

**输出:**

```py
arr :  ['vdsdsttetteteAAAa', 'AAAAAAAaattttds', 'AAaaxxxxtt', 'AAaaXDSDdscz']

find of 'tt' [ 5  9  8 -1]
find of 'tt' [ 5  9  8 -1]
find of 'tt' [ 8  9  8 -1]

```

**代码#2:**

```py
# Python Program illustrating 
# numpy.char.find() method 
import numpy as np 

arr = ['vdsdsttetteteAAAa', 'AAAAAAAaattttds', 'AAaaxxxxtt', 'AAaaXDSDdscz']

print ("\nfind of 'Aa'", np.char.find(arr, 'Aa'))
print ("find of 'Aa'", np.char.find(arr, 'Aa', start = 8))
```

**输出:**

```py
find of 'Aa' [15  6  1  1]
find of 'Aa' [15 -1 -1 -1]

```