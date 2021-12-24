# Python 中的 numpy.index()

> 原文:[https://www.geeksforgeeks.org/numpy-index-in-python/](https://www.geeksforgeeks.org/numpy-index-in-python/)

**`numpy.core.defchararray.index(arr, substring, start=0, end=None)` :** 查找指定范围内子字符串的最低索引，但如果未找到子字符串，则会引发 ValueError。

> **参数:**
> **arr :** 数组状或字符串待搜索。
> **子串:**要搜索的子串。
> **开始，结束:**【int，可选】搜索范围。
> 
> **返回:**找到的子字符串索引最低的整数数组，如果找不到子字符串，则引发 ValueError。

**代码#1:**

```py
# Python Program illustrating 
# numpy.char.index() method 
import numpy as np 

arr = ['this is geeks for geek']

print ("arr : ", arr)

print ("\nindex of 'geeks' : ", np.char.index(arr, 'geeks'))
```

**输出:**

```py
arr :  ['this is geeks for geek']

index of 'geeks' : [8]

```

**代码#2:**

```py
# Python Program illustrating 
# numpy.char.index() method 
import numpy as np 

arr = ['this is geeks for geek']

print ("\nindex of 'geeks' : ", np.char.index(arr, 'geeks', start = 2))
print ("\nindex of 'geeks' : ", np.char.index(arr, 'geeks', start = 10))
print ("\nindex of 'geek' : ", np.char.index(arr, 'geek', start = 10))
```

**输出:**

```py
index of 'geeks' : [8]
ValueError: substring not found
index of 'geek' : [18]

```