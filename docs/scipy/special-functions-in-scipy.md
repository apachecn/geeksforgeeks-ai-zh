# SciPy 中的特殊功能

> 原文:[https://www.geeksforgeeks.org/special-functions-in-scipy/](https://www.geeksforgeeks.org/special-functions-in-scipy/)

在本文中，我们将了解 Scipy 中的特殊函数。scipy 中的特殊函数用于对给定数据执行数学运算。scipy 中的特殊功能是 scipy 包中提供的一个模块。在这个特殊函数中，可用的方法有:

*   **cbrt**–给出给定数字的立方根
*   **梳理**–给出元素的组合
*   **exp 10**–给出给定数字的 10 次方
*   **表达式**–给出相对误差指数，(exp(x)–1)/x。
*   **gamma**–通过计算 z*gamma(z) = gamma(z+1)和 gamma(n+1) = n 返回数值！，表示自然数“n”。
*   **朗伯图**–计算任意复数 z 的 W(z) * exp(W(z))，其中 W 是朗伯图函数
*   **对数求和表达式**–给出给定数字的指数和的对数
*   **烫发**–给出元素的排列

**我们来详细了解一下这些功能。**

#### 1.cbrt()

这用于返回给定数字的立方根。

> **语法:** cbrt(数字)

**例:**求立方根的程序

## 蟒蛇 3

```
from scipy.special import cbrt

# cube root of 64
print(cbrt(64))

# cube root of 78
print(cbrt(78))

# cube root of 128
print(cbrt(128))
```

**输出:**

```
4.0
4.272658681697917
5.039684199579493
```

**示例:**在给定的数组元素中寻找立方根的程序。

## 蟒蛇 3

```
from scipy.special import cbrt

# cube root of elements in an array
arr = [64, 164, 564, 4, 640]
arr = list(map(cbrt,arr))
print(arr)
```

**输出:**

> [4.0, 5.473703674798428, 8.26214922566535, 1.5874010519681994, 8.617738760127535]

#### **2。梳子()**

它被称为组合，返回给定值的组合。

> **语法:** scipy.special.comb(N，k)
> 
> 其中，N 为输入值，k 为重复次数。

**例 1:**

## 蟒蛇 3

```
# import combinations
from scipy.special import comb

# combinations of input 4
print(comb(4,1))
```

**输出:**

```
4.0
```

**例 2:**

## 蟒蛇 3

```
# import combinations module
from scipy.special import comb

# combinations of 4
print([comb(4,1),comb(4,2),comb(4,3),
       comb(4,4),comb(4,5)])

# combinations of 6
print([comb(6,1),comb(6,2),comb(6,3),
       comb(6,4),comb(6,5)])
```

**输出:**

```
[4.0, 6.0, 4.0, 1.0, 0.0]
[6.0, 15.0, 20.0, 15.0, 6.0]
```

#### 3.exp10()

这个方法给出的数字是给定数字的 10 次方。

> **语法:** exp10(值)
> 
> 其中值是作为输入给出的数字。

**例:**求 10 次方的程序

## 蟒蛇 3

```
from scipy.special import exp10

# 10 to the power of 2
print(exp10(2))
```

**输出:**

```
100.0
```

**示例:**为一个范围寻找 10 的幂的程序

## 蟒蛇 3

```
from scipy.special import exp10

# exponent raise to power 10 
# for a range
for i in range(1,10):
  print(exp10(i)
```

**输出:**

```
10.0
100.0
1000.0
10000.0
100000.0
1000000.0
10000000.0
100000000.0
1000000000.0
```

#### 4.exprel()

它被称为相对误差指数函数。它返回给定变量的误差值。如果 x 接近零，则 exp(x)接近 1。

> **语法:**scipy . special . exprel(input _ data)

**例 1:**

## 蟒蛇 3

```
# import exprel
from scipy.special import exprel

# calculate exprel of 0
print(exprel(0))
```

**输出:**

```
1.0
```

**例 2:**

## 蟒蛇 3

```
# import exprel
from scipy.special import exprel

# list of elements 
arr = [0,1,2,3,4,5]

print(list(map(exprel,arr)))
```

**输出:**

> [1.0, 1.718281828459045, 3.194528049465325, 6.361845641062556, 13.399537508286059, 29.48263182051532]

#### 5.伽马射线()

它被称为伽马函数。它是广义阶乘，因为 z*gamma(z) = gamma(z+1)和 gamma(n+1) = n！，表示自然数“n”。

> **语法:**scipy . special . gamma(input _ data)
> 
> 其中，输入数据为输入数字。

**例 1:**

## 蟒蛇 3

```
# import gamma function
from scipy.special import gamma

print(gamma(56))
```

**输出:**

```
1.2696403353658278e+73
```

**例 2:**

## 蟒蛇 3

```
# import gamma function
from scipy.special import gamma

print([gamma(56), gamma(156), gamma(0),
       gamma(1), gamma(5)])
```

**输出:**

```
[1.2696403353658278e+73, 4.789142901463394e+273, inf, 1.0, 24.0]
```

#### 6.lambertw()

它也被称为朗伯函数。它计算 W(z)的值，使得 z = W(z) * exp(W(z))对于任何复数 z，其中 W 被称为朗伯函数

> **语法:**scipy . special . lambertw(input _ data)

**示例:**

## 蟒蛇 3

```
# import lambert function
from scipy.special import lambertw

# calculate W value
print([lambertw(1),lambertw(0),lambertw(56),
       lambertw(68),lambertw(10)])
```