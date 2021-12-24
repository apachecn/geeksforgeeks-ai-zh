# 比较和过滤 NumPy 数组

> 原文:[https://www . geeksforgeeks . org/comparison-and-filtering-numpy-array/](https://www.geeksforgeeks.org/comparing-and-filtering-numpy-array/)

在本文中，我们将看到如何对 NumPy 数组进行比较和过滤。

### **比较 NumPy 数组:**

让我们看看将在比较 NumPy 数组时使用的比较运算符–

*   大于(>)或 numpy.greater().

*   Equal (= =) or unequal (! =) or numpy.not_equal ().
*   Greater than or equal to (> =).
*   Is less than (< =).

【NumPy 数组比较步骤:

**步骤 1:** 首先在您的系统或环境中安装 NumPy。通过使用以下命令。

```py
pip install numpy(command prompt)
!pip install numpy(jupyter)
```

**第二步:**导入 NumPy 模块。

```py
import numpy as np
```

**步骤 3:** 使用 NumPy Array 方法创建元素数组。

```py
np.array([elements])
```

**步骤 4:** 现在使用比较运算符来比较 NumPy 数组。

**示例 1:**

*   Import NumPy module.
*   Use numpy.array () method to create an array.
*   Now use the greater () method to compare two arrays.

## 蟒 3

```py
# importing NumPy Module
import numpy as np 

# Creating Array
a = np.array([1,2,3,4]) 
b = np.array([3,8,5,6])

# Comparing two arrays
np.greater(a, b)
```

**输出:**

```py
array([False, False, False, False])
```

**例 2:**

*   导入 NumPy 模块。
*   使用 numpy.array()方法创建数组。
*   现在使用 less()方法比较两个数组。

## 蟒蛇 3

```py
# Importing NumPy Module
import numpy as np

# Creating Array using NumPy
a = np.array([1, 2, 3, 4])
b = np.array([3, 8, 5, 6])
np.less(a, b)
```

**输出:**

```py
array([ True,  True,  True,  True])
```

**示例 3:**

*   Import NumPy module.
*   Use numpy.array () method to create an array.
*   Now use the equal () method to compare two arrays.

## 蟒 3

```py
# Importing NumPy Module.
import numpy as np

# Create Arrays using np.array() Function.
a = np.array([1, 2, 3, 4])
b = np.array([3, 8, 5, 6])

# Compare a and b array elements
# if the elements in a and b are equal
# it returns True else returns False.
np.equal(a, b)
```

**输出:**

```py
array([ False,  False,  False, False])
```

**示例 4:**

*   Import NumPy module.
*   Use numpy.array () method to create an array.
*   Now use the not_equal () method to compare two arrays.

## 蟒 3

```py
# Importing NumPy Module.
import numpy as np

# Create Arrays using np.array() Function.
a = np.array([1, 2, 3, 4])
b = np.array([3, 8, 5, 6])

# Compare a and b array elements if the
# elements in a and b are  not equal
# it returns True else returns False.
np.not_equal(a, b)
```

**输出:**

```py
array([ True,  True,  True,  True])
```

**例 5:**

*   Import NumPy module.
*   Use numpy.array () method to create an array.
*   Now use the > = operator to compare two arrays.

## 蟒 3

```py
# Importing NumPy Module.
import numpy as np

# Create Arrays using np.array()
# Function.
a = np.array([1, 2, 3, 4])
b = np.array([3, 8, 5, 6])

# it returns if elements in a  are
# greater than a equal to b
print(a >= b)
```