# 字符串的两个 NumPy 数组的元素串联

> 原文:[https://www . geeksforgeeks . org/element-wise-concation-two-numpy-array-of-string/](https://www.geeksforgeeks.org/element-wise-concatenation-of-two-numpy-arrays-of-string/)

在本文中，我们将讨论如何按元素连接两个字符串数组

**示例:**

```py
Input :
A = ['Akash', 'Ayush', 'Diksha', 'Radhika']
B = ['Kumar', 'Sharma', 'Tewari', 'Pegowal']

Output :
A + B = [AkashKumar, AyushSharma, 'DikshTewari', 'RadhikaPegowal']

```

我们将使用 **方法。**

> ***语法:** numpy.char.add(x1，x2)*
> ***参数:***
> 
> *   ***x1 :** 第一个要连接的数组(开始连接)*
> *   ***x2 :** 第二个要串接的数组(串接在最后)*
> 
> ***返回:**字符串或 unicode 数组*

**例 1:** 单元素字符串数组。

## 蟒蛇 3

```py
# importing library numpy as np
import numpy as np

# creating array as first_name
first_name = np.array(['Geeks'], 
                      dtype = np.str)
print("Printing first name array:")
print(first_name)

# creating array as last name
last_name = np.array(['forGeeks'], 
                     dtype = np.str)
print("Printing last name array:")
print(last_name)

# concate first_name and last_name 
# into new array named as full_name
full_name = np.char.add(first_name, last_name)
print("\nPrinting concatenate array as full name:")
print(full_name)
```

**输出:**

```py
Printing first name array:
['Geeks']
Printing last name array:
['forGeeks']

Printing concatenate array as full name:
['GeeksforGeeks']

```

**例 2:** 多元素字符串数组。

## 蟒蛇 3

```py
# importing library numpy as np
import numpy as np

# creating array as first_name
first_name = np.array(['Akash', 'Ayush', 'Diksha', 
                       'Radhika'], dtype = np.str)
print("Printing first name array:")
print(first_name)

# creating array as last name
last_name = np.array(['Kumar', 'Sharma', 'Tewari', 
                      'Pegowal'], dtype = np.str)
print("Printing last name array:")
print(last_name)

# concate first_name and last_name 
# into new array named as full_name
full_name = np.char.add(first_name, last_name)
print("\nPrinting concatenate array as full name:")
print(full_name)
```

**输出:**

```py
Printing first name array:
['Akash' 'Ayush' 'Diksha' 'Radhika']
Printing last name array:
['Kumar' 'Sharma' 'Tewari' 'Pegowal']

Printing concatenate array as full name:
['AkashKumar' 'AyushSharma' 'DikshaTewari' 'RadhikaPegowal']

```