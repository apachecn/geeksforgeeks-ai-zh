# Python 中的 numpy.random.randn()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-random-rann-python/

**numpy.random.randn()** 函数创建一个指定形状的数组，并根据**标准正态**分布用随机值填充它。

如果提供了正参数，randn 将生成一个 shape (d0，d1，…，dn)数组，其中填充了从均值 0 和方差 1 的**单变量“正态”(高斯)分布**中采样的随机浮点(如果 d_i 中有任何一个是浮点，则首先通过截断将其转换为整数)。如果未提供参数，则返回从分布中随机采样的单个浮点值。

**语法:**

```py
numpy.random.randn(d0, d1, ..., dn)
```

**参数:**

```py
d0, d1, ..., dn : [int, optional]Dimension of the returned array we require, 
     If no argument is given a single Python float is returned.

```

**返回:**

```py
Array of defined shape, filled with random floating-point samples from 
the standard normal distribution.

```

**代码 1:随机构建 1D 阵列**

```py
# Python Program illustrating
# numpy.random.randn() method

import numpy as geek

# 1D Array
array = geek.random.randn(5)
print("1D Array filled with random values : \n", array);
```

**输出:**

```py
1D Array filled with randnom values : 
 [-0.51733692  0.48813676 -0.88147002  1.12901958  0.68026197]

```

**代码 2:随机构建 2D 阵列**

```py
# Python Program illustrating
# numpy.random.randn() method

import numpy as geek

# 2D Array   
array = geek.random.randn(3, 4)
print("2D Array filled with random values : \n", array);
```

**输出:**

```py
2D Array filled with random values : 
 [[ 1.33262386 -0.88922967 -0.07056098  0.27340112]
 [ 1.00664965 -0.68443807  0.43801295 -0.35874714]
 [-0.19289416 -0.42746963 -1.80435223  0.02751727]]

```

**代码 3:随机构建 3D 阵列**

```py
# Python Program illustrating
# numpy.random.randn() method

import numpy as geek

# 3D Array     
array = geek.random.randn(2, 2 ,2)
print("3D Array filled with random values : \n", array);
```

**输出:**

```py
3D Array filled with random values : 
 [[[-0.00416587 -0.66211158]
  [-0.97254293 -0.68981333]]

 [[-0.18304476 -0.8371425 ]
  [ 2.18985366 -0.9740637 ]]]

```

 **代码 4:随机创建数组的操作**

```py
# Python Program illustrating
# numpy.random.randn() method

import numpy as geek

# 3D Array     
array = geek.random.randn(2, 2 ,2)
print("3D Array filled with random values : \n", array);

# Multiplying values with 3
print("\nArray * 3 : \n", array *3)

# Or we cab directly do so by 
array = geek.random.randn(2, 2 ,2) * 3 + 2
print("\nArray * 3 + 2 : \n", array);
```

**输出:**

```py
3D Array filled with random values : 
 [[[ 1.9609643  -1.89882763]
  [ 0.52252173  0.08159455]]

 [[-0.6060213  -0.86759247]
  [ 0.53870235 -0.77388125]]]

Array * 3 : 
 [[[ 5.88289289 -5.69648288]
  [ 1.56756519  0.24478366]]

 [[-1.81806391 -2.6027774 ]
  [ 1.61610704 -2.32164376]]]

Array * 3 + 2 : 
 [[[-2.73766306  6.80761741]
  [-1.57909191 -1.64195796]]

 [[ 0.51019498  1.30017345]
  [ 3.8107863  -4.07438963]]]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . randn . html](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.random.randn.html)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作。
。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。