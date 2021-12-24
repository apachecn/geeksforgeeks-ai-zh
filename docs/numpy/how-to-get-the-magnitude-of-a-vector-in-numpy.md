# 如何得到 NumPy 中矢量的大小？

> 原文:[https://www . geeksforgeeks . org/如何获得数字矢量幅度/](https://www.geeksforgeeks.org/how-to-get-the-magnitude-of-a-vector-in-numpy/)

线性代数的基本特征是向量，向量是既有方向又有大小的对象。在 Python 中，NumPy 数组可以用来描述一个向量。

**矢量大小的获取主要有两种方式:**

*   By defining an explicit function which computes the magnitude of a given vector based on the below mathematical formula:

    ```
    if V is vector such that, V = (a, b, c)
    then ||V|| = ?(a*a + b*b + c*c)

    ```

    下面是一些按照上述方法计算矢量大小的程序:

    ```
    # program to compute magnitude of a vector

    # importing required libraries
    import numpy
    import math

    # function defination to compute magnitude o f the vector
    def magnitude(vector): 
        return math.sqrt(sum(pow(element, 2) for element in vector))

    # displaying the original vector
    v = numpy.array([0, 1, 2, 3, 4])
    print('Vector:', v)

    # computing and displaying the magnitude of the vector
    print('Magnitude of the Vector:', magnitude(v))
    ```

    **输出:**

    ```
    Vector: [0 1 2 3 4]
    Magnitude of the Vector: 5.477225575051661

    ```

    下面是采用相同方法的另一个示例:

    ```
    # program to compute magnitude of a vector

    # importing required libraries
    import numpy
    import math

    # function defination to compute magnitude o f the vector
    def magnitude(vector): 
        return math.sqrt(sum(pow(element, 2) for element in vector))

    # computing and displaying the magnitude of the vector
    print('Magnitude of the Vector:', magnitude(numpy.array([1, 2, 3])))
    ```

    **输出:**

    ```
    Magnitude of the Vector: 3.7416573867739413

    ```

*   By using the `norm()` method in `linalg` module of `NumPy` library. The Linear Algebra module of `NumPy` offers various methods to apply linear algebra on any `NumPy` array. Below are some programs which use `numpy.linalg.norm()` to compute the magnitude of a vector:

    ```
    # program to compute magnitude of a vector

    # importing required libraries
    import numpy

    # displaying the original vector
    v = numpy.array([1, 2, 3])
    print('Vector:', v)

    # computing and displaying the magnitude of
    # the vector using norm() method
    print('Magnitude of the Vector:', numpy.linalg.norm(v))
    ```

    **输出:**

    ```
    Vector: [1 2 3]
    Magnitude of the Vector: 3.7416573867739413

    ```

    一个额外的参数`ord`可以用来计算向量的第 n 阶`norm()`。

    ```
    # program to compute the nth order of the 
    # magnitude of a vector

    # importing required libraries
    import numpy

    # displaying the original vector
    v = numpy.array([0, 1, 2, 3, 4])
    print('Vector:', v)

    # computing and displaying the magnitude of the vector
    print('Magnitude of the Vector:', numpy.linalg.norm(v))

    # Computing the nth order of the magnitude of vector
    print('ord is 0: ', numpy.linalg.norm(v, ord = 0))
    print('ord is 1: ', numpy.linalg.norm(v, ord = 1))
    print('ord is 2: ', numpy.linalg.norm(v, ord = 2))
    print('ord is 3: ', numpy.linalg.norm(v, ord = 3))
    print('ord is 4: ', numpy.linalg.norm(v, ord = 4))
    ```

    **输出:**

    ```
    Vector: [0 1 2 3 4]
    Magnitude of the Vector: 5.477225575051661
    ord is 0:  4.0
    ord is 1:  10.0
    ord is 2:  5.477225575051661
    ord is 3:  4.641588833612778
    ord is 4:  4.337613136533361

    ```