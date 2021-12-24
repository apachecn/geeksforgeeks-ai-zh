# Python 中的 numpy.count()

> 原文:[https://www.geeksforgeeks.org/numpy-count-in-python/](https://www.geeksforgeeks.org/numpy-count-in-python/)

**`numpy.core.defchararray.count(arr, substring, start=0, end=None)` :** 统计指定范围内子字符串的非重叠出现。

> **参数:**
> **arr :** 数组状或字符串待搜索。
> **子串:**要搜索的子串。
> **开始，结束:**【int，可选】搜索范围。
> 
> **返回:**一个整数数组，其中子字符串的出现次数不重叠。

**代码#1:**

```
# Python Program illustrating 
# numpy.char.count() method 

import numpy as np 

# 2D array 
arr = ['vdsdsttetteteAAAa', 'AAAAAAAaattttds', 'AAaaxxxxtt', 'AAaaXDSDdscz']

print ("arr : ", arr)

print ("Count of 'tt'", np.char.count(arr, 'tt'))
print ("Count of 'tt'", np.char.count(arr, 'tt', start = 0))
print ("Count of 'tt'", np.char.count(arr, 'tt', start = 8))
```

**输出:**

```
arr :  ['vdsdsttetteteAAAa', 'AAAAAAAaattttds', 'AAaaxxxxtt', 'AAaaXDSDdscz']
Count of 'tt' [2 2 1 0]
Count of 'tt' [2 2 1 0]
Count of 'tt' [1 2 1 0]

```

**代码#2:**

```
# Python Program illustrating 
# numpy.char.count() method 
import numpy as np 

# 2D array 
arr = ['vdsdsttetteteAAAa', 'AAAAAAAaattttds', 'AAaaxxxxtt', 'AAaaXDSDdscz']

print ("arr : ", arr)

print ("Count of 'Aa'", np.char.count(arr, 'Aa'))
print ("Count of 'Aa'", np.char.count(arr, 'Aa', start = 8))
```

**输出:**

```
arr :  ['vdsdsttetteteAAAa', 'AAAAAAAaattttds', 'AAaaxxxxtt', 'AAaaXDSDdscz']

Count of 'Aa' [1 1 1 1]
Count of 'Aa' [1 0 0 0]

```