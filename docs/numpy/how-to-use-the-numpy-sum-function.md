# 如何使用 NumPy 求和函数？

> 原文:[https://www . geeksforgeeks . org/如何使用 numpy-sum-function/](https://www.geeksforgeeks.org/how-to-use-the-numpy-sum-function/)

NumPy 的 [sum()](https://www.geeksforgeeks.org/numpy-sum-in-python/) 函数对于 Python 中给定数组的所有元素求和极其有用。在本文中，我们将讨论如何利用这个函数，以及如何快速使用它来提升代码的功能。

让我们来看看如何使用这些函数，以及使用这个函数而不是迭代求和的好处。我们先自己写底层算法做简单求和。这将采取如下函数的形式:

## python 3

```
# Let's define our function
# Parameters: Input Array
def sum(array):

    # Set variable for our final answer
    sum = 0

    # Parse through our array
    for i in array:

        # Continuously add current element
        # to final sum
        sum += i

    # Return our sum
    return sum

# Create a test array
testArray = [1, 3, 34, 92, 29, 48, 20.3]

# Test our function
print('The sum of your numbers is ' + str(sum(testArray)))
```