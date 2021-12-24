# 在 NumPy 中拆分数组

> 原文:[https://www.geeksforgeeks.org/splitting-arrays-in-numpy/](https://www.geeksforgeeks.org/splitting-arrays-in-numpy/)

数组拆分可以是垂直的、水平的或深度方向的。同样的，我们可以分别使用`hsplit()`、`vsplit()`和`dsplit()`功能。我们可以通过指示拆分应该发生的位置，将数组拆分成相同形状的数组。

*   **Horizontal splitting:** The **‘hsplit()’** function splits an array along axis parameter = 1\. **‘numpy.hsplit’** is equivalent to **‘split’** with **axis parameter = 1**, the array is always splitted along the second axis regardless of the array dimension. This function split an array into multiple sub-arrays horizontally (column-wise).

    **语法:**

    ```
    numpy.hsplit(ary, indices_or_sections)
    ```

    **示例:**

    ```
    # Horizontal array splitting using np.hsplit()
    import numpy as np

    # Making of  a 3x3 array
    a = np.arange(9).reshape(3, 3)

    # Horizontal splitting of array 
    # 'a' using np.hsplit().
    print("The array {} gets splitted \
    horizontally to form {} ".format(a, np.hsplit(a, 3)))

    # Horizontal splitting of array 'a' 
    # using 'split' with axis parameter = 1.
    print("The array {} gets splitted \
    horizontally to form {} ".format(a, np.split(a, 3, 1)))
    ```

    **输出:**

    ```
     The array [[0 1 2]
     [3 4 5]
     [6 7 8]] gets splitted horizontally to form [array([[0],
           [3],
           [6]]), array([[1],
           [4],
           [7]]), array([[2],
           [5],
           [8]])] 
    The array [[0 1 2]
     [3 4 5]
     [6 7 8]] gets splitted horizontally to form [array([[0],
           [3],
           [6]]), array([[1],
           [4],
           [7]]), array([[2],
           [5],
           [8]])]
    ```

*   **Vertical splitting:** The **‘vsplit()’** function splits an array along axis parameter = 0.**‘numpy.vsplit’** is equivalent to **‘split’** with **axis parameter = 0**. This function split an array into multiple sub-arrays vertically (row-wise).

    ```
    numpy.vsplit(ary, indices_or_sections)
    ```

    **示例:**

    ```
    import numpy as np

    # Making of  a 3x3 array
    a = np.arange(9).reshape(3, 3)

    # Vertical splitting of array 'a'
    # using np.vsplit().
    print("The array {} gets splitted \
    vertically to form {} ".format(a, np.vsplit(a, 3)))

    # Vertical splitting of array 'a' 
    # using 'split' with axis parameter = 0.
    print("The array {} gets splitted \
    vertically to form {} ".format(a, np.split(a, 3, 0)))
    ```

    **输出:**

    > 数组[[0 1 2]
    > [3 4 5]
    > [6 7 8]]被垂直拆分成[数组([[0，1，2]])、数组([[3，4，5]])、数组([[6，7，8]])]
    > 数组[[0 1 2]
    > [3 4 5]
    > [6 7 8]]被垂直拆分成[数组([[0，1，2]])、数组([[3，4，5]])]、数组([[3，4，5])

*   **Depth-wise splitting:** It Split the array into multiple sub-arrays along the 3rd axis (depth).

    ```
    numpy.dsplit(ary, indices_or_sections)
    ```

    **示例:**

    ```
    import numpy as np

    # Making of  a 3x3x3 array.
    b = np.arange(27).reshape(3, 3, 3)

    # Depth-wise splitting of array
    # 'b' using np.dsplit().
    print("The array {} gets splitted \
    depth-wise to form {}".format(b, np.dsplit(b, 3)))
    ```

    **输出:**

    > 数组[[[ 0 1 2]
    > [ 3 4 5]
    > [ 6 7 8]]
    > 
    > [[9 10 11]
    > [12 13 14]
    > [15 16 17]]
    > 
    > [[18 19 20]
    > [21 22 23]
    > [24 25 26]]]在深度方向上被分割以形成[数组([[ 0]，
    > [ 3]，
    > [ 6]]，
    > 
    > [[ 9]，
    > [12]，
    > [15]]，
    > 
    > [[18]，
    > [21]，
    > [24]]])，数组([[ 1]，
    > [ 4]，
    > [ 7]]，
    > 
    > [[10]，
    > [13]，
    > [16]]，
    > 
    > [[19]，
    > [22]，
    > [25]]])，数组([[ 2]，
    > [ 5]，
    > [ 8]]，
    > 
    > [[11]，
    > [14]，
    > [17]]，
    > 
    > [[20]，
    > [23]，
    > [26]]])]