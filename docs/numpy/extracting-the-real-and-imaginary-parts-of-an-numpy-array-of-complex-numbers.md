# 提取复数 NumPy 数组的实部和虚部

> 原文:[https://www . geeksforgeeks . org/提取复数数组的实部和虚部/](https://www.geeksforgeeks.org/extracting-the-real-and-imaginary-parts-of-an-numpy-array-of-complex-numbers/)

Numpy 库给了我们像`[real()](https://www.geeksforgeeks.org/numpy-real-function-python/)` 、`[imag()](https://www.geeksforgeeks.org/numpy-imag-function-python/)`这样的函数来求一个复数的实部和虚部。

*   `**real() :**`求复数的实部
*   `**imag() :**`求复数的虚部

例 1:

```py
# importing the module
import numpy as np

# creating a NumPy array
complex_num = np.array([-1 + 9j, 2 - 77j,
                        31 - 25j, 40 - 311j,
                        72 + 11j])

# traversing the list
for i in range(len(complex_num)):
      print("{}. complex number is {}".format(i + 1, complex_num[i]))
      print ("The real part is: {}".format(complex_num[i].real))
      print ("The imaginary part is: {}\n".format(complex_num[i].imag))
```

**输出:**

```py
1\. complex number is (-1+9j)
The real part is: -1.0
The imaginary part is: 9.0

2\. complex number is (2-77j)
The real part is: 2.0
The imaginary part is: -77.0

3\. complex number is (31-25j)
The real part is: 31.0
The imaginary part is: -25.0

4\. complex number is (40-311j)
The real part is: 40.0
The imaginary part is: -311.0

5\. complex number is (72+11j)
The real part is: 72.0
The imaginary part is: 11.0

```

**例 2 :** 实数的虚数将为 0。

```py
# importing the module
import numpy as np

# creating a NumPy array
complex_num = np.array([-1, 31, 0.5])

# traversing the list
for i in range(len(complex_num)):
      print("{}. Number is {}".format(i + 1, complex_num[i]))
      print ("The real part is: {}".format(complex_num[i].real))
      print ("The imaginary part is: {}\n".format(complex_num[i].imag))
```

**输出:**

```py
1\. Number is -1.0
The real part is: -1.0
The imaginary part is: 0.0

2\. Number is 31.0
The real part is: 31.0
The imaginary part is: 0.0

3\. Number is 0.5
The real part is: 0.5
The imaginary part is: 0.0

```