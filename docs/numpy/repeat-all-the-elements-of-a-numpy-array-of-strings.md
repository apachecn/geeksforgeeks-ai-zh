# 重复 NumPy 字符串数组的所有元素

> 原文:[https://www . geeksforgeeks . org/repeat-numpy 字符串数组的所有元素/](https://www.geeksforgeeks.org/repeat-all-the-elements-of-a-numpy-array-of-strings/)

让我们看看如何重复给定字符串数组的所有元素 3 次。

**示例:**

> **输入:** ['Akash '，' Rohit '，' Ayush '，' Dhruv '，' Radhika']
> **输出:**[' akashakashkash '，' RohitRohitRohit '，' AyushAyushAyush '，' DhruvDhruvDhruv '，' radhikaradhikaradharadhika ']

我们将使用 **numpy.char.multiply(a，i)** 方法来完成这个任务。

## numpy.char.multiply(a，I)

> **语法:** numpy.char.multiply(a，i)
> **参数:**
> 
> *   **一个:**字符串或 unicode 数组
> *   **i :** 重复次数
> 
> **返回:**字符串数组

**实施例 1 :** 重复 3 次。

```py
# importing the module
import numpy as np

# created array of strings
arr = np.array(['Akash', 'Rohit', 'Ayush', 
                'Dhruv', 'Radhika'], dtype = np.str)
print("Original Array :")
print(arr)

# with the help of np.char.multiply()
# repeating the characters 3 times
new_array = np.char.multiply(arr, 3)
print("\nNew array :")
print(new_array)
```

**输出:**

> 原始数组:
> [' Akash ' ' Rohit ' ' Ayush ' ' Dhruv ' ' Radhika ']
> 
> 新数组:
> [' akashakashkash ' ' rohitrohithrohitrhhit ' ' ayushayushush ' ' DhruvDhruvDhruv ' ' RadhikaRadhikaRadhika ']

**实施例 2:** 重复 2 次。

```py
# importing the module
import numpy as np

# created array of strings
arr = np.array(['Geeks', 'for', 'Geeks'])
print("Original Array :")
print(arr)

# with the help of np.char.multiply()
# repeating the characters 3 times
new_array = np.char.multiply(arr, 2)
print("\nNew array :")
print(new_array)
```

**输出:**

```py
Original Array :
['Geeks' 'for' 'Geeks']

New array :
['GeeksGeeks' 'forfor' 'GeeksGeeks']

```