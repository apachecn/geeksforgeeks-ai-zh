# NumPy–使用比奈公式的斐波那契数列

> 原文:[https://www . geesforgeks . org/numpy-Fibonacci-series-use-Binet-formula/](https://www.geeksforgeeks.org/numpy-fibonacci-series-using-binet-formula/)

我们都熟悉斐波那契数列。序列中的每个数字都是它前面两个数字的总和。所以，顺序是这样的:0，1，1，2，3，5，8，13，21，34……在本教程中，我们将借助**比奈公式**使用 NumPy 实现相同的操作。

**比奈公式**
![  fn = \left [\left (\frac{1 + \sqrt{5}}{2}  \right )^{n} - \left (\frac{1 - \sqrt{5}}{2}  \right )^{n}  \right ]\ast \frac{1}{\sqrt{5}}  where, alpha = \left (\frac{1 + \sqrt{5}}{2}  \right ), beta = \left (\frac{1 - \sqrt{5}  }{2}\right )  ](img/fe7c6d5d5601ca0038aafe14be8ec48b.png "Rendered by QuickLaTeX.com")

**n** 是与斐波那契数列的第一个**n 个数字相关的参数。**在第一个例子中，我们将找出斐波那契数列的前 10 个数字(n = 10)，然后我们从用户那里获取参数“n”，并产生相应的结果。

**注:**我们忽略了斐波那契数列的第一个元素(0)

**例 1:** 求前 10 个斐波那契数。

```
import numpy as np

# We are creating an array contains n = 10 elements
# for getting first 10 Fibonacci numbers
a = np.arange(1, 11)
lengthA = len(a)

# splitting of terms for easiness
sqrtFive = np.sqrt(5)
alpha = (1 + sqrtFive) / 2
beta = (1 - sqrtFive) / 2

# Implementation of formula
# np.rint is used for rounding off to integer
Fn = np.rint(((alpha ** a) - (beta ** a)) / (sqrtFive))
print("The first {} numbers of Fibonacci series are {} . ".format(lengthA, Fn))
```

**输出:**

> 斐波那契数列的前 10 个数字是[ 1。1.2.3.5.8.13.21.34.55.] .

**示例 2 :** 寻找第一个‘n’个斐波那契数..

```
import numpy as np

# We are creating an array contains n elements
# for getting first 'n' Fibonacci numbers
fNumber = int(input("Enter the value of n + 1'th number : "))
a = np.arange(1, fNumber)
length_a = len(a)

# splitting of terms for easiness
sqrt_five = np.sqrt(5)
alpha = (1 + sqrt_five) / 2
beta = (1 - sqrt_five) / 2

# Implementation of formula
# np.rint is used for rounding off to integer
Fn = np.rint(((alpha ** a) - (beta ** a)) / (sqrt_five))
print("The first {} numbers of Fibonacci series are {} . ".format(length_a, Fn))
```

**输出:**

```
# Here user input was 10
Enter the value of n+1'th number :10
The first 9 numbers of Fibonacci series are [ 1\.  1\.  2\.  3\.  5\.  8\. 13\. 21\. 34.] . 
```