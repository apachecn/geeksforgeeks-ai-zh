# Python |症状二项式 _ 系数 _ 列表()方法

> 原文:[https://www . geesforgeks . org/python-sympy-二项式 _ 系数 _list-method/](https://www.geeksforgeeks.org/python-sympy-binomial_coefficients_list-method/)

借助**方法，我们可以将二项式系数作为帕斯卡三角形的行。**

> **语法:**二项式 _ 系数 _ 列表(n)
> 
> **参数:**
> **n–**表示整数。
> 
> **返回:**以帕斯卡三角形的行形式返回二项式系数列表。

**示例#1:**

```
# import binomial_coefficients_list() method from sympy
from sympy.ntheory import binomial_coefficients_list

n = 6

# Use binomial_coefficients_list() method 
binomial_coefficients_list_n = binomial_coefficients_list(n) 

print("{}th row of Pascal's Triangle = {} ".format(n, binomial_coefficients_list_n))
```

**输出:**

```
6th row of Pascal's Triangle = [1, 6, 15, 20, 15, 6, 1] 

```

**例 2:**

```
# import binomial_coefficients_list() method from sympy
from sympy.ntheory import binomial_coefficients_list

n = 9

# Use binomial_coefficients_list() method 
binomial_coefficients_list_n = binomial_coefficients_list(n) 

print("{}th row of Pascal's Triangle = {} ".format(n, binomial_coefficients_list_n))
```

**输出:**

```
9th row of Pascal's Triangle = [1, 9, 36, 84, 126, 126, 84, 36, 9, 1]  

```