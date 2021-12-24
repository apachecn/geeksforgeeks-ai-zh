# 使用 NumPy 将数组元素转换为浮点类型

> 原文:[https://www . geeksforgeeks . org/using-numpy-convert-array-elements-to-float-type/](https://www.geeksforgeeks.org/using-numpy-to-convert-array-elements-to-float-type/)

我们经常需要将 Python 中的数组转换为不同的类型。其中一种情况是，当给定一个数组时，必须将其转换为浮点类型的数组。这在进行数据分析时通常很有用，并且有多种方法可以做到这一点。虽然遍历数组并使用 Python 内置的`float()`转换函数是完全有效的，但是 NumPy 为我们提供了一些更优雅的方式来执行相同的过程。

**方法 1 :** 这里，我们可以利用 NumPy 提供的`**astype()**`功能。这个函数用指定的数据类型创建初始数组的另一个副本，在这种情况下是 float，然后我们可以将这个副本分配给一个特定的标识符，这个标识符就是 convertedArray。注意数据类型是用 NumPy 来指定的，主要是因为 NumPy `astype()`函数的约束，它只会把 NumPy 类型作为参数。

```py
# Process utilizing astype() function

# Import NumPy Library
import numpy as np

# Initialize our Array with Strings
# The String Type is denoted by the quotes ""
initialArray = ["1.1", "2.2", "3.3", "4.4"]

# Convert initial Array to NumPy Array
# Use the array() function
sampleArray = np.array(initialArray)

# Print our Initial Array
print("Our initial array: ", str(initialArray))
print("Original type: " + str(type(initialArray[0])))

# Actual Conversion of Array
# Note usage of astype() function
# np.float can be changed to represent differing types
convertedArray = sampleArray.astype(np.float)

# Print our final result
# Note that usage of str() is due to Python conventions
print("Our final array: ", str(convertedArray))
print("Final type: " + str(type(convertedArray[0])))
```

**输出:**

```py
Our initial array:  ['1.1', '2.2', '3.3', '4.4']
Original type: <class 'numpy.str_'>
Our final array:  [1.1 2.2 3.3 4.4]
Final type: <class 'numpy.float64'>

```

**方法二:**这里，我们将利用 NumPy 提供的 **`[asarray()](https://www.geeksforgeeks.org/numpy-asarray-in-python/#:~:text=asarray()%20in%20Python,-Last%20Updated%3A%2029&text=29%2D11%2D2018-,numpy.,tuples%20of%20lists%20and%20ndarrays.)`** 功能。

```py
# Process utilizing asarray() function

# Import NumPy Library
import numpy as np

# Initialize our array
# Note, once again, that this is of type String
# Non-NumPy arrays can be used
initialArray = np.array(["1.1", "2.2", "3.3", "4.4"])

# Print our initial array
print("Our Initial Array: ", str(initialArray))
print("Original type: " + str(type(initialArray[0])))

# Actual conversion of array
# Note that we utilize np.float64 as the finalize data type
finalArray = np.asarray(initialArray, dtype = np.float64, 
                        order ='C')

# Print our converted array
print("Our Final Array: ", str(finalArray))
print("Final type: " + str(type(finalArray[0])))
```

**输出:**

```py
Our initial array:  ['1.1', '2.2', '3.3', '4.4']
Original type: <class 'numpy.str_'>
Our final array:  [1.1 2.2 3.3 4.4]
Final type: <class 'numpy.float64'>

```