# NumPy–算术运算

> 原文:[https://www.geeksforgeeks.org/numpy-arithmetic-operations/](https://www.geeksforgeeks.org/numpy-arithmetic-operations/)

**NumPy** 是一个执行数组计算(矩阵运算)的开源 Python 库。它是用 C 语言实现的库的包装器，用于执行几个三角、代数和统计运算。NumPy 对象可以很容易地转换成其他类型的对象，如熊猫数据框和张量流张量。Python 列表可以用于数组计算，但是比 NumPy 慢很多。NumPy 使用[矢量化](https://www.geeksforgeeks.org/vectorization-in-python/)实现了快速实现。NumPy 数组的一个重要特性是，开发人员可以用一个命令对每个元素执行相同的数学运算。

让我们理解使用 NumPy 的算术运算。

### **添加**

## 蟒蛇 3

```py
import numpy as np

# Defining both the matrices
a = np.array([5, 72, 13, 100])
b = np.array([2, 5, 10, 30])

# Performing addition using arithmetic operator
add_ans = a+b
print(add_ans)

# Performing addition using numpy function
add_ans = np.add(a, b)
print(add_ans)

# The same functions and operations can be used for multiple matrices
c = np.array([1, 2, 3, 4])
add_ans = a+b+c
print(add_ans)

add_ans = np.add(a, b, c)
print(add_ans)
```

**输出**

```py
[  7  77  23 130]
[  7  77  23 130]
[  8  79  26 134]
[  8  79  26 134]
```

我们可以看到，矩阵的形状是一样的，如果不同，如果可能的话，Numpy 会尝试[广播](https://www.geeksforgeeks.org/python-broadcasting-with-numpy-arrays/)。读者可以看到，使用算术运算(+)和 numpy 函数(np.add)可以完成相同的运算(加法)。

### **减法**

## 蟒蛇 3

```py
import numpy as np

# Defining both the matrices
a = np.array([5, 72, 13, 100])
b = np.array([2, 5, 10, 30])

# Performing subtraction using arithmetic operator
sub_ans = a-b
print(sub_ans)

# Performing subtraction using numpy function
sub_ans = np.subtract(a, b)
print(sub_ans)
```

**输出**

```py
[ 3 67  3 70]
[ 3 67  3 70]
```

用户也可以用矩阵和常数进行广播

## 蟒蛇 3

```py
import numpy as np

# Defining both the matrices
a = np.array([5, 72, 13, 100])
b = np.array([2, 5, 10, 30])

# Performing subtraction using arithmetic operator
sub_ans = a-b-1
print(sub_ans)

# Performing subtraction using numpy function
sub_ans = np.subtract(a, b, 1)
print(sub_ans)
```

**输出**

```py
[ 2 66  2 69]
[ 2 66  2 69]
```

### 乘法器

## 蟒蛇 3

```py
import numpy as np

# Defining both the matrices
a = np.array([5, 72, 13, 100])
b = np.array([2, 5, 10, 30])

# Performing multiplication using arithmetic operator
mul_ans = a*b
print(mul_ans)

# Performing multiplication using numpy function
mul_ans = np.multiply(a, b)
print(mul_ans)
```

**输出**

```py
[  10  360  130 3000]
[  10  360  130 3000]
```

### **分部**

## 蟒蛇 3

```py
import numpy as np

# Defining both the matrices
a = np.array([5, 72, 13, 100])
b = np.array([2, 5, 10, 30])

# Performing division using arithmetic operators
div_ans = a/b
print(div_ans)

# Performing division using numpy functions
div_ans = np.divide(a, b)
print(div_ans)
```

**输出**

```py
[ 2.5        14.4         1.3         3.33333333]
[ 2.5        14.4         1.3         3.33333333]
```

在 NumPy 中有无数的其他函数，让我们一个接一个地看到其中的一些。

mod()和 power()函数

**例**

## 蟒蛇 3

```py
# Performing mod on two matrices
mod_ans = np.mod(a, b)
print(mod_ans)

#Performing remainder on two matrices
rem_ans=np.remainder(a,b)
print(rem_ans)

# Performing power of two matrices
pow_ans = np.power(a, b)
print(pow_ans)
```

**输出**

```py
[ 1  2  3 10]
[ 1  2  3 10]
[                 25          1934917632        137858491849
 1152921504606846976]
```

一些聚合和统计函数

**例**

## 蟒蛇 3

```py
# Getting mean of all numbers in 'a'
mean_a = np.mean(a)
print(mean_a)

# Getting average of all numbers in 'b'
mean_b = np.average(b)
print(mean_b)

# Getting sum of all numbers in 'a'
sum_a = np.sum(a)
print(sum_a)

# Getting variance of all number in 'b'
var_b = np.var(b)
print(var_b)
```

**输出**

```py
47.5
11.75
190
119.1875
```