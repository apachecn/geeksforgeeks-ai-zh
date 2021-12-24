# Python 中的 numpy.poly()

> 原文:[https://www.geeksforgeeks.org/numpy-poly-in-python/](https://www.geeksforgeeks.org/numpy-poly-in-python/)

多项式根序列中的 **numpy.poly()** 函数返回多项式的系数。

> **语法:** numpy.poly(seq)
> 
> **参数:**
> **序列:**多项式根的根序列，或根矩阵。
> 
> **返回:**多项式系数从最高到最低的 1D 阵列。
> c[0]* x * *(N)+c[1]* x * *(N-1)+…+c[N-1]* x+c[N]，其中 c[0]总是等于 1。

```
# Python code explaining  
# numpy.poly() 

# importing libraries 
import numpy as np 

# Giving the roots 
seq_1 = (2, 1, 0)
a = np.poly(seq_1)
print ("Coefficients of the polynomial: ", a)

# Constructing polynomial  
p1 = np.poly1d(a)
print ("\nAbove polynomial = \n", p1) 
```

**输出:**

```
Coefficients of the polynomial:  [ 1\. -3\.  2\.  0.]

Above polynomial = 
    3     2
1 x - 3 x + 2 x
```

**代码#2:**

```
# Python code explaining  
# numpy.poly() 

# importing libraries 
import numpy as np 

# Giving the roots
seq_2 = (2, 1, 0, 2, 4, 2)
b = np.poly(seq_2)
print ("Coefficients of the polynomial: ", b)

# Constructing polynomial  
p2 = np.poly1d(b)
print ("\nAbove polynomial = \n", p2) 
```

**输出:**

```
Coefficients of the polynomial:  [  1\. -11\.  46\. -92\.  88\. -32\.   0.]

Above polynomial = 
    6      5      4      3      2
1 x - 11 x + 46 x - 92 x + 88 x - 32 x

```