# NumPy–按多个条件过滤行

> 原文:[https://www . geeksforgeeks . org/numpy-按多条件筛选行/](https://www.geeksforgeeks.org/numpy-filtering-rows-by-multiple-conditions/)

在本文中，我们将讨论如何通过多个条件过滤 NumPy 数组的行。在跳转到按多个条件过滤行之前，让我们首先看看如何基于一个条件应用过滤器。基本上有两种方法可以做到这一点:

**方法一:使用掩膜阵列**

掩码功能从数组 *arr* 中过滤出位于*掩码*数组中假索引处的数字。开发人员可以根据他们的要求设置掩码数组——当很难形成过滤逻辑时，这将变得非常有用。

**接近**

*   导入模块
*   制作初始数组
*   定义掩码
*   根据掩码创建一个新数组
*   打印新数组

**程序:**

## 蟒蛇 3

```py
# importing numpy lib
import numpy as np

# making a numpy array
arr = np.array([x for x in range(11, 20)])

print("Original array")
print(arr)

# defining mask
mask = [True, False, True, False, True, True, False, False, False]

# making new array on conditions
new_arr = arr[mask]

print("New array")
print(new_arr)
```

**输出**

> 原始数组
> 
> [11 12 13 14 15 16 17 18 19]
> 
> 新数组
> 
> [11 13 15 16]

**方法二:使用迭代法**

开发人员不是使用掩码，而是迭代数组 *arr* ，并在每个数组元素上应用条件。

**接近**

*   导入模块
*   创建数组
*   创建一个空数组
*   遍历数组
*   根据某些条件选择项目
*   将选定的项目添加到空数组中
*   显示阵列

**程序:**

## 蟒蛇 3

```py
# importing numpy lib
import numpy as np

# making a numpy array
arr = np.array([x for x in range(11, 20)])

print("Original array")
print(arr)

# making a blank list
new_arr = []

for x in arr:
  # applying condition: appending even numbers
    if x % 2 == 0:
        new_arr.append(x)

# Converting new list into numpy array
new_arr = np.array(new_arr)
print("New array")
print(new_arr)
```

**输出**

> 原始数组
> 
> [11 12 13 14 15 16 17 18 19]
> 
> 新数组
> 
> [12 14 16 18]

现在让我们尝试在 NumPy 数组上应用多个条件

**方法一:使用面膜**

**接近**

*   导入模块
*   创建初始数组
*   基于多个条件定义掩码
*   根据掩码向新数组添加值
*   显示阵列

**例**

## 蟒蛇 3

```py
# importing numpy lib
import numpy as np

# making a numpy array
arr = np.array([x for x in range(11, 40)])

print("Original array")
print(arr)

# defining mask based on two conditions:
# array element must be greater than 15
# and must be a divisible by 2
mask = (arr > 15) & (arr % 2 == 0)

# making new array on conditions
new_arr = arr[mask]
print("New array")
print(new_arr)
```

**输出**

> 原始数组
> 
> [11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34
> 
> 35 36 37 38 39]
> 
> 新数组
> 
> [16 18 20 22 24 26 28 30 32 34 36 38]

**方法二:迭代法**

**接近**

*   导入模块
*   创建初始数组
*   创建一个空数组
*   遍历数组
*   基于多个条件选择项目
*   将所选项目添加到空列表中
*   显示阵列

**例**

## 蟒蛇 3

```py
# importing numpy lib
import numpy as np

# making a numpy array
arr = np.array([x for x in range(11, 40)])

print("Original array")
print(arr)

# making a blank list
new_arr = []

for x in arr:
    # applying two conditions: number is divisible by 2 and is greater than 15
    if x % 2 == 0 and x > 15:
        new_arr.append(x)

# Converting new list into numpy array
new_arr = np.array(new_arr)
print("New array")
print(new_arr)
```

**输出**

> 原始数组
> 
> [11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34
> 
> 35 36 37 38 39]
> 
> 新数组
> 
> [16 18 20 22 24 26 28 30 32 34 36 38]

**方法三:使用λ**

**接近**

*   导入模块
*   创建初始数组
*   使用 lambda 函数应用多个条件
*   相应地选择项目
*   向新数组中添加项
*   显示阵列

**例**

## 蟒蛇 3

```py
# importing numpy lib
import numpy as np

# making a numpy array
arr = np.array([x for x in range(11, 40)])

print("Original array")
print(arr)

# using lambda to apply condition
new_arr = list(filter(lambda x: x > 15 and x % 2 == 0 and x % 10 != 0, arr))

# Converting new list into numpy array
new_arr = np.array(new_arr)
print("New array")
print(new_arr)
```

**输出**

> 原始数组
> 
> [11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34
> 
> 35 36 37 38 39]
> 
> 新数组
> 
> [16 18 22 24 26 28 32 34 36 38]