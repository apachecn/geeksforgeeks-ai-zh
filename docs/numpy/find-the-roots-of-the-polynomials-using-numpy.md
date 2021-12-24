# 用 NumPy

求多项式的根

> 原文:[https://www . geeksforgeeks . org/find-多项式的根-使用-numpy/](https://www.geeksforgeeks.org/find-the-roots-of-the-polynomials-using-numpy/)

在这篇文章中，我们来讨论如何找到 NumPy 数组的多项式的根。可以用各种方法找到，让我们详细看看。

**方法 1:** 使用[NP . root()](https://www.geeksforgeeks.org/numpy-roots-function-python/)

这个函数返回一个多项式的根，多项式的系数在 p 中给出。多项式的系数将按照各自的顺序放在一个数组中。

比如多项式是 **x <sup>2</sup> +3x + 1** ，那么数组就是【1，3，1】

> ***语法:**numpy . root(p)*
> 
> ***参数:***
> ***p:**【array _ like】Rank-1 多项式系数数组。*
> 
> ***返回:**【ndarray】包含多项式根的数组。*

让我们看一些例子:

**例 1:** 求多项式 x 的根 <sup>2</sup> +2x + 1

## 蟒蛇 3

```
# import numpy library
import numpy as np

# Enter the coefficients of the poly in the array
coeff = [1, 2, 1]
print(np.roots(coeff))
```

**输出:**

```
[-1\. -1.]
```

**例 2:** 求多项式的根 x <sup>3</sup> +3 x <sup>2</sup> + 2x +1

## 蟒蛇 3

```
# import numpy library
import numpy as np

# Enter the coefficients of the poly 
# in the array
coeff = [1, 3, 2, 1]
print(np.roots(coeff))
```

**输出:**

> [-2.32471796+0 . j-0.33764102+0.56227951j-0.33764102-0.56227951j]

**方法 2:** 使用 [np.poly1D()](https://www.geeksforgeeks.org/numpy-poly1d-in-python/)

这个函数有助于定义多项式函数。它使得对多项式应用“自然运算”变得容易。多项式的系数将按照各自的顺序放入数组中。

例如，对于多项式 x2 +3x + 1，数组将是[1，3，1]

**进场:**

*   对数组应用函数 np.poly1D()，并将其存储在变量中。
*   通过将变量乘以根或 r(内置关键字)找到根，并打印结果以获得给定多项式的根

> **语法:** numpy.poly1d(arr、root、var):

让我们看一些例子:

**例 1:** 求多项式 x 的根 <sup>2</sup> +2x + 1

## 蟒蛇 3

```
# import numpy library
import numpy as np

# enter the coefficients of poly 
# in the array
p = np.poly1d([1, 2, 1])

# multiplying by r(or roots) to 
# get the roots
root_of_poly = p.r
print(root_of_poly)
```

**输出:**

```
[-1\. -1.]
```

**例 2:** 求多项式的根 x <sup>3</sup> +3 x <sup>2</sup> + 2x +1

## 蟒蛇 3

```
# import numpy library
import numpy as np

# enter the coefficients of poly
# in the array
p = np.poly1d([1, 3, 2, 1])

# multiplying by r(or roots) to get 
# the roots
root_of_poly = p.r
print(root_of_poly)
```

**输出:**

> [-2.32471796+0 . j-0.33764102+0.56227951j-0.33764102-0.56227951j]