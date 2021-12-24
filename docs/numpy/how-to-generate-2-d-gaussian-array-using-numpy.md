# 如何用 NumPy 生成二维高斯阵列？

> 原文:[https://www . geeksforgeeks . org/如何使用-numpy/](https://www.geeksforgeeks.org/how-to-generate-2-d-gaussian-array-using-numpy/) 生成-2-d-高斯数组

在本文中，让我们讨论如何使用 NumPy 生成二维高斯阵列。使用 Numpy python 模块创建二维高斯数组

#### **使用的功能:**

*   [**numpy . mesh grid()**](https://www.geeksforgeeks.org/numpy-meshgrid-function/)**–**It**用于从代表笛卡尔索引或矩阵索引的两个给定一维数组中创建矩形网格。**

****语法:****

> **网格网格(*xi，副本=真，稀疏=假，索引='xy')**

*   **[**【numpy . linespace()】**](https://www.geeksforgeeks.org/numpy-linspace-python/)**–**returns 数字间隔均匀。**

****语法:****

> **numpy.linspace(开始，停止，num = 50，endpoint = True，retstep = False，dtype = None)**

*   **[**numpy . exp()**](https://www.geeksforgeeks.org/numpy-exp-python/)**–**t他的数学函数帮助用户计算输入数组中所有元素的指数。**

****语法:****

> **numpy.exp(数组，out = None，其中= True，casting = 'same_kind '，order = 'K '，dtype = None)**

****例 1:****

## **蟒蛇 3**

```
# Importing Numpy package
import numpy as np

# Initializing value of x-axis and y-axis
# in the range -1 to 1
x, y = np.meshgrid(np.linspace(-1,1,10), np.linspace(-1,1,10))
dst = np.sqrt(x*x+y*y)

# Initializing sigma and muu
sigma = 1
muu = 0.000

# Calculating Gaussian array
gauss = np.exp(-( (dst-muu)**2 / ( 2.0 * sigma**2 ) ) )

print("2D Gaussian array :\n")
print(gauss)
```

****输出:****

> **2D 高斯阵列:
> 【【0.36787944 0.44822088 0.51979489 0.57375342 0.60279818 0.60279818】
> 0.57375342 0.51979489 0.44822088 0.3678944】
> 【0。44894 . 4888888888
> 【0.57375342 0.69905581 0.81068432 0.89483932 0.9401382 0.9401382
> 0.89483932 0.81068432 0.6990581 0.57375342】
> 【0.51979489 0.6990581**

****例 2:****

## **蟒蛇 3**

```
# Importing Numpy package
import numpy as np

# Initializing value of x-axis and y-axis
# in the range -2 to +2
x, y = np.meshgrid(np.linspace(-2,2,15), np.linspace(-2,2,15))
dst = np.sqrt(x*x+y*y)

# Initializing sigma and muu
sigma = 1
muu = 0.000

# Calculating Gaussian array
gauss = np.exp(-( (dst-muu)**2 / ( 2.0 * sigma**2 ) ) )

print("2D Gaussian array :\n")
print(gauss)
```

****输出:****

> **2D 高斯阵列:
> [[0.01831564 0.03113609 0.0487813 0.07043526 0.09372907 0.11494916
> 0.12992261 0.1353528 0.129261 0 . 1299266
> 【0.09372907 0.15933686 0.24963508 0.36044779 0.47965227 0.58824471】
> 0.66487032 0.69256932 0.6648732 0.5847031 0.96000544 0.84936582 0.69256932 0.52045012
> 0.36044779 0.2300663 0.13533528】
> 【0.12992261】0.2208649 0.344444044
> 【0.0487813 0.08292689 0.12992261 0.1875951 0.24963508 0.30615203
> 0.34603184 0.36044779 0.34603184**