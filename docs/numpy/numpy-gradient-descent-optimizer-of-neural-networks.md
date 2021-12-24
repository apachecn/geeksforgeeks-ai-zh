# 神经网络的数值梯度下降优化器

> 原文:[https://www . geesforgeks . org/numpy-梯度下降-神经网络优化器/](https://www.geeksforgeeks.org/numpy-gradient-descent-optimizer-of-neural-networks/)

在微分学中，一个函数的导数告诉我们，只要输入变量稍微改变一下，输出就会改变多少。这个想法也可以扩展到多变量函数。本文展示了使用 NumPy 实现梯度下降算法。这个想法很简单——从一个任意的起点开始，向最小值移动(即梯度值为-ve)，返回一个尽可能接近最小值的点。

GD()是用于此目的的用户定义函数。它采用以下参数:

*   **Gradient** is a function, or it can be a python callable object, which uses a vector & to return the gradient of the function we are trying to minimize.
*   **Start** is any starting point that we assign to the function. It is a single independent variable. It can also be a list or a multivariable Numpy array.
*   **learn _ rate** Control the amplitude of vector update.
*   **n _ ITER** is the number of iterations that the operation should run.
*   **Tol** is the tolerance level that specifies the minimum movement in each iteration.

下面给出了产生所需功能的实现。

**例:**

## 蟒 3

```
import numpy as np

def GD(f, start, lr, n_iter=50, tol=1e-05):
    res = start

    for _ in range(n_iter):

        # gradient is calculated using the np.gradient 
        # function.
        new_val = -lr * np.gradient(f)
        if np.all(np.abs(new_val) <= tol):
            break
        res += new_val

    # we return a vector as the gradient can be
    # multivariable function. if the function has 1
    # dependent variable then it returns a scalar value.
    return res

# Example 1
f = np.array([1, 2, 4, 7, 11, 16], dtype=float)
print(f"The vector notation of global minima:{GD(f,10,0.01)}")

# Example 2
f = np.array([2, 4], dtype=float)
print(f'The vector notation of global minima: {GD(f,10,0.1)}')
```

**输出:**

> 全局极小的向量表示法:【9.5 9.25 8.75 8.25 7.75 7.5】
> 
> 全局极小的向量表示法:【2.0539126 e-15 2.0539126 e-15】

让我们详细看看这个函数中使用的相关概念。

## 公差等级应用

下面的代码行使 GD()能够提前终止，并在 n_iter 完成之前返回，如果更新小于或等于容差水平，当我们到达局部最小值或鞍点时，这尤其加快了过程，在鞍点处，由于梯度非常低，增量移动非常慢，因此加快了收敛速度。

## 蟒 3

```
if np.all(np.abs(new_val) <= tol):
   break
```

## 学习率使用(超参数)

*   学习率是一个非常关键的超参数，因为它影响梯度下降算法的行为。例如，如果我们将学习速率从 0.2 更改为 0.7，我们会得到另一个非常接近 0 的解，但是由于学习速率很高，x 会有很大的变化，即它会多次通过最小值，因此它会在设置为零之前振荡。这种振荡增加了整个算法的收敛时间。
*   小的学习速率会导致缓慢的收敛，如果迭代次数很少，那么算法甚至可能在找到最小值之前就返回，这将使情况变得更糟。

下面给出了一个例子来说明学习率是如何影响结果的。

**例:**

## 蟒 3

```
import numpy as np

def GD(f, start, lr, n_iter=50, tol=1e-05):
    res = start
    for _ in range(n_iter):
        # gradient is calculated using the np.gradient function.
        new_val = -lr * np.gradient(f)
        if np.all(np.abs(new_val) <= tol):
            break
        res += new_val

    # we return a vector as the gradient can be multivariable function.
    # if the function has 1 dependent variable then it returns a scalar value.
    return res

f = np.array([2, 4], dtype=float)
# low learing rate doesn't allow to converge at global minima
print(f'The vector notation of global minima: {GD(f,10,0.001)}')
```

**输出** :

```
[9.9 9.9]
```

算法返回的值甚至不接近 0。这表明我们的算法在收敛到全局最小值之前返回。