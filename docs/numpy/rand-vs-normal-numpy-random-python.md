# Python 中 rand vs normal . numpy . random

> 原文:[https://www . geesforgeks . org/rand-vs-normal-numpy-random-python/](https://www.geeksforgeeks.org/rand-vs-normal-numpy-random-python/)

在本文中，我们将详细研究 numpy . rand . rand()方法和 Numpy.random.normal()方法之间的主要区别。

*   **About random:** For random we are taking .rand()
    **[numpy.random.rand](https://www.geeksforgeeks.org/numpy-random-rand-python/)(d0, d1, …, dn) :**
    creates an array of specified shape and
    fills it with random values.
    **Parameters :**

    ```
    d0, d1, ..., dn : [int, optional]
    Dimension of the returned array we require, 

    If no argument is given a single Python float 
    is returned.

    ```

    **返回:**

    ```
    Array of defined shape, filled with random values.

    ```

*   **About normal:** For random we are taking .normal()
    **numpy.random.normal(loc = 0.0, scale = 1.0, size = None) :** creates an array of specified shape and fills it with random values which is actually a part of Normal(Gaussian)Distribution. This is Distribution is also known as Bell Curve because of its characteristics shape.
    **Parameters :**

    ```
    loc   : [float or array_like]Mean of 
    the distribution. 
    scale : [float or array_like]Standard 
    Derivation of the distribution. 
    size  : [int or int tuples]. 
    Output shape given as (m, n, k) then
    m*n*k samples are drawn. If size is 
    None(by default), then a single value
    is returned. 

    ```

    **返回:**

    ```
    Array of defined shape, filled with 
    random values following normal 
    distribution.

    ```

    **代码 1:随机构建 1D 阵列**

    ```
    # Python Program illustrating
    # numpy.random.rand() method

    import numpy as geek

    # 1D Array
    array = geek.random.rand(5)
    print("1D Array filled with random values : \n", array)
    ```

    **输出:**

    ```
    1D Array filled with random values : 
     [ 0.84503968  0.61570994  0.7619945   0.34994803  0.40113761]

    ```

    **代码 2:按照高斯分布随机构建 1D 阵列**

    ```
    # Python Program illustrating
    # numpy.random.normal() method

    import numpy as geek

    # 1D Array
    array = geek.random.normal(0.0, 1.0, 5)
    print("1D Array filled with random values "
          "as per gaussian distribution : \n", array)
    # 3D array
    array = geek.random.normal(0.0, 1.0, (2, 1, 2))
    print("\n\n3D Array filled with random values "
          "as per gaussian distribution : \n", array)
    ```

    **输出:**

    ```
    1D Array filled with random values as per gaussian distribution : 
     [-0.99013172 -1.52521808  0.37955684  0.57859283  1.34336863]

    3D Array filled with random values as per gaussian distribution : 
     [[[-0.0320374   2.14977849]]

     [[ 0.3789585   0.17692125]]]

    ```

     **代码 3 : Python 程序，演示了 NumPy 中随机与正常的图形表示**

    ```
    # Python Program illustrating
    # graphical representation of 
    # numpy.random.normal() method
    # numpy.random.rand() method

    import numpy as geek
    import matplotlib.pyplot as plot

    # 1D Array as per Gaussian Distribution
    mean = 0 
    std = 0.1
    array = geek.random.normal(0, 0.1, 1000)
    print("1D Array filled with random values "
          "as per gaussian distribution : \n", array);

    # Source Code : 
    # https://docs.scipy.org/doc/numpy-1.13.0/reference/
    # generated/numpy-random-normal-1.py
    count, bins, ignored = plot.hist(array, 30, normed=True)
    plot.plot(bins, 1/(std * geek.sqrt(2 * geek.pi)) *
              geek.exp( - (bins - mean)**2 / (2 * std**2) ),
              linewidth=2, color='r')
    plot.show()

    # 1D Array constructed Randomly
    random_array = geek.random.rand(5)
    print("1D Array filled with random values : \n", random_array)

    plot.plot(random_array)
    plot.show()
    ```

    **输出:**

    ```
    1D Array filled with random values as per gaussian distribution : 
     [ 0.12413355  0.01868444  0.08841698 ..., -0.01523021 -0.14621625
     -0.09157214]

    1D Array filled with random values : 
     [ 0.72654409  0.26955422  0.19500427  0.37178803  0.10196284]

    ```

    **重要提示:**
    在代码 3 中，图 1 清楚地显示了高斯分布，因为它是从通过 random.normal()方法生成的值创建的，因此遵循高斯分布。
    图 2 没有遵循任何分布，因为它是根据 random.rand()方法生成的随机值创建的。

    **注意:**
    代码 3 不会在在线-ID 上运行。请在您的系统上运行它们来探索工作。
    。
    本文由 <font color="green">**Mohit Gupta_OMG 供稿😀**</font> 。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。

    如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。