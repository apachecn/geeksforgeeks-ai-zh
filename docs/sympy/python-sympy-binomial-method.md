# Python |症状二项式()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-binomial-method/](https://www.geeksforgeeks.org/python-sympy-binomial-method/)

借助 **sympy.binomial()** 方法，我们可以从一组 ***n*** 截然不同的物品中找到选择 ***k*** 物品的方法数量。也常写成 ***nCk*** ，读作“n 选 k”。

(1) ![ \begin{equation*}     \binom{N}{k} \end{equation*} ](img/6e2b0303330f3e60daf7413c5e238c04.png "Rendered by QuickLaTeX.com")

> **语法:**二项式(N，K)
> 
> **参数:**
> **N–**表示可供选择的物品数量。
> **K–**表示要选择的项目数量。
> 
> **返回:**返回从一组 ***N*** 不同物品中选择 ***K*** 物品的方式数

**示例#1:**

```
# import sympy 
from sympy import * 

N = 4
K = 2 
print("N = {}, K = {}".format(N, K))

# Use sympy.binomial() method 
comb = binomial(N, K)  

print("N choose K : {}".format(comb))  
```

**输出:**

```
N = 4, K = 2
N choose K : 6

```

**例 2:**

```
# import sympy 
from sympy import * 

N, K = symbols('A B')

print("N = {}, K = {}".format(N, K))

# Use sympy.binomial() method 
comb = binomial(N, K)  

print("N choose K : {}".format(comb))  
```

**输出:**

```
N = A, K = B
N choose K : binomial(A, B)

```