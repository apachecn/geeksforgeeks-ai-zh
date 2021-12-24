# Python 中的 numpy.equal()

> 原文:[https://www.geeksforgeeks.org/numpy-equal-python/](https://www.geeksforgeeks.org/numpy-equal-python/)

**numpy.equal(arr1，arr2，out = None，其中= True，casting = 'same_kind '，order = 'K '，dtype = None，ufunc 'not_equal') :** 此逻辑函数检查 arr1 **==** arr2 elemen-twise。

**参数:**

> **arr 1:**【array _ like】输入数组
> T3】arr 2:【array _ like】输入数组
> 
> **输出:**【n 数组，可选】输出数组，与输入数组具有相同的尺寸，与结果一起放置。
> 
> ****kwargs :** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> 
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。

**返回:**

```py
Returns arr1 == arr2 element-wise

```

**代码 1 :**

```py
# Python Program illustrating
# numpy.equal() method
import numpy as geek 

a  = geek.equal([1., 2.], [1., 3.])
print("Check to be Equal : \n", a, "\n")

b = geek.equal([1, 2], [[1, 3],[1, 4]])
print("Check to be Equal : \n", b, "\n")
```

**输出:**

```py
Check to be Equal : 
 [ True False] 

Check to be Equal : 
 [[ True False]
 [ True False]] 

```

**代码 2:使用比较数据类型。相等()功能**

```py
# Python Program illustrating
# numpy.equal() method
import numpy as geek 

# Here we will compare Complex values with int
a = geek.array([0 + 1j, 2])
b = geek.array([1,2])

d  = geek.equal(a, b)
print("Comparing complex with int using .equal() : ", d)
```

**输出:**

```py
Comparing complex with int using .equal() :  [False  True]
```

**代码 3 :**

```py
# Python Program illustrating
# numpy.not_equal() method
import numpy as geek 

# Here we will compare Float with int values
a = geek.array([1.1, 1])
b = geek.array([1, 2])

d  = geek.not_equal(a, b)
print("\nComparing float with int using .not_equal() : ", d)
```

**输出:**

```py
Comparing float with int using .not_equal() :  [ True  True]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . equal . html](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.equal.html)
。