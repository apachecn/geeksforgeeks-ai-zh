# 如何在给定 NumPy 数组所有元素的字符之间插入空格？

> 原文:[https://www . geeksforgeeks . org/如何在给定 numpy 数组的所有元素的字符之间插入空格/](https://www.geeksforgeeks.org/how-to-insert-a-space-between-characters-of-all-the-elements-of-a-given-numpy-array/)

在本文中，我们将讨论如何在给定字符串数组的所有元素的字符之间插入空格。
**例:**

```
Suppose we have an array of string as follows:
A = ["geeks", "for", "geeks"]

then when we insert a space between the characters
of all elements of the above array we get the 
following output.
A = ["g e e k s", "f o r", "g e e k s"]

```

为此，我们将使用 **np.char.join()。**该方法基本上返回一个字符串，其中各个字符通过该方法中指定的分隔符连接在一起。这里使用的分隔符是空格。

> **语法:** np.char.join(sep，string)
> 
> **参数:**
> **sep:** 是任意指定的分隔符
> **字符串:**是任意指定的字符串。

**示例:**

## 蟒蛇 3

```
# importing numpy as np
import numpy as np

# creating array of string
x = np.array(["geeks", "for", "geeks"],
             dtype=np.str)
print("Printing the Original Array:")
print(x)

# inserting space using np.char.join()
r = np.char.join(" ", x)
print("Printing the array after inserting space\
between the elements")
print(r)
```

**输出:**

```
Printing the Original Array:
['geeks' 'for' 'geeks']
Printing the array after inserting spacebetween the elements
['g e e k s' 'f o r' 'g e e k s']
```