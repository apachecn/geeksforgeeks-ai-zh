# Python | sympy.digits()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-digits-method/](https://www.geeksforgeeks.org/python-sympy-digits-method/)

借助 **sympy.digits()** 方法，我们可以在 sympy 中找到任意给定基数上给定整数的位数。

> **语法:**位数字(n，t=10)
> 
> **参数:**
> **n–**表示整数。
> **b–**表示基本整数(可选)。b 的默认值为 10。
> 
> **返回:**返回一个以 b 为基数的 n 位数列表，列表中的第一个元素是 b(如果 n 为负数，则为-b)。

**示例#1:**

```
# import digits() method from sympy
from sympy.ntheory.factor_ import digits

n = 7524
b = 10

# Use digits() method 
digits_n_b = digits(n, b) 

print("Digits of {} in base {} =  {} ".format(n, b, digits_n_b)) 
```

**输出:**

```
Digits of 7524 in base 10 =  [10, 7, 5, 2, 4] 

```

**例 2:**

#从 sympy 导入数字()方法
从 sympy . syntheory . factor _ 导入数字

n = 33
b = 2

#使用 digits()方法
digits_n_b = digits(n，b)

打印(“以{}为基数的{}位数= {}”。格式(n，b，digits_n_b))
**输出:**

```
Digits of 33 in base 2 =  [2, 1, 0, 0, 0, 0, 1] 

```