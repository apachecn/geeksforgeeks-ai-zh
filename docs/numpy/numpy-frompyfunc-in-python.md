# python 中的 numpy.frompyfunc()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-frompyfunc-in-python/

**numpy.frompyfunc(func，nin，nout)** 函数允许创建任意 Python 函数作为 Numpy ufunc(通用函数)。

> **参数:**
> **函数:**【一个 python 函数对象】任意 python 函数
> **nin:**【int】该函数的输入参数数量。
> **nout:**【int】该函数返回的对象数。
> **返回:**一个 Numpy 通用函数对象。

例如，abs_value = numpy.frompyfunc(abs，1，1)将创建一个 *ufunc* ，它将返回数组元素的绝对值。

**代码#1:**

## 蟒蛇 3

```py
# Python code to demonstrate the
# use of numpy.frompyfunc
import numpy as np

# create an array of numbers
a = np.array([34, 67, 89, 15, 33, 27])

# python str function as ufunc
string_generator = np.frompyfunc(str, 1, 1)

print("Original array-", a)
print("After conversion to string-", string_generator(a))
```

**Output:** 

```py
Original array- [34 67 89 15 33 27]
After conversion to string- ['34' '67' '89' '15' '33' '27']
```

**代码#2:**

## 蟒蛇 3

```py
# Python code to demonstrate
# user-defined function as ufunc
import numpy as np

# create an array of numbers
a = np.array([345, 122, 454, 232, 334, 56, 66])

# user-defined function to check
# whether a no. is palindrome or not
def fun(x):
    s = str(x)
    return s[::-1]== s

# 'check_palindrome' as universal function
check_palindrome = np.frompyfunc(fun, 1, 1)
print("Original array-", a)
print("Checking of number as palindrome-",
                      check_palindrome(a))
```

**Output:** 

```py
Original array- [345 122 454 232 334  56  66]
Checking of number as palindrome- [False False True True False False True]
```

**注意:**这个使用 frompyfunc 创建的自定义 *ufunc* 总是接受一个数组作为输入参数，并返回一个数组对象作为输出。