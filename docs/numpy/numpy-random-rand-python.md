# Python 中的 numpy . rand . rand()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-random-rand-python/

函数的作用是:创建一个指定形状的数组，并用随机值填充。
**语法:**

```py
numpy.random.rand(d0, d1, ..., dn)
```

**参数:**

```py
d0, d1, ..., dn : [int, optional]Dimension of the returned array we require, 
     If no argument is given a single Python float is returned.

```

**返回:**

```py
Array of defined shape, filled with random values.

```

**代码 1:随机构建 1D 阵列**

```py
# Python Program illustrating
# numpy.random.rand() method

import numpy as geek

# 1D Array
array = geek.random.rand(5)
print("1D Array filled with random values : \n", array);
```

**输出:**

```py
1D Array filled with random values : 
 [ 0.84503968  0.61570994  0.7619945   0.34994803  0.40113761]

```

**代码 2:随机构建 2D 阵列**

```py
# Python Program illustrating
# numpy.random.rand() method

import numpy as geek

# 2D Array   
array = geek.random.rand(3, 4)
print("\n\n2D Array filled with random values : \n", array);
```

**输出:**

```py

2D Array filled with random values : 
 [[ 0.94739375  0.5557614   0.69812121  0.86902435]
 [ 0.94758176  0.22254413  0.21605843  0.44673235]
 [ 0.61683839  0.40570269  0.34369248  0.46799524]]

```

**代码 3:随机构建 3D 阵列**

```py
# Python Program illustrating
# numpy.random.rand() method

import numpy as geek

# 3D Array     
array = geek.random.rand(2, 2 ,2)
print("\n\n3D Array filled with random values : \n", array);
```

**输出:**

```py

3D Array filled with random values : 
 [[[ 0.97942627  0.01068711]
  [ 0.35749073  0.22484643]]

 [[ 0.99733022  0.8029555 ]
  [ 0.44111692  0.90537128]]]

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . rand . html # numpy . rand . rand](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.random.rand.html#numpy.random.rand)

**注意:**
这些代码不会在在线-ID 上运行。请在您的系统上运行它们来探索工作。
。
本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。