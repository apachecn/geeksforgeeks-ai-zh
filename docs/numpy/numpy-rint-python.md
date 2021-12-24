# python 中的 numpy.rint()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-rint-python/

**numpy.rint()** 是一个数学函数，它将数组的元素舍入到最接近的整数。

> **语法:** numpy.rint(x[，out]) = ufunc 'rint')
> **参数:**
> **数组:***【array _ like】*输入数组。
> 
> **返回:**所有数组元素被舍入的数组，与输入具有相同的类型和形状。

**代码#1:工作**

```py
# Python program explaining
# rint() function
import numpy as np

in_array = [.5, 1.5, 2.5, 3.5, 4.5, 10.1]
print ("Input array : \n", in_array)

rintoff_values = np.rint(in_array)
print ("\nRounded values : \n", rintoff_values)

in_array = [.53, 1.54, .71]
print ("\nInput array : \n", in_array)

rintoff_values = np.rint(in_array)
print ("\nRounded values : \n", rintoff_values)

in_array = [.5538, 1.33354, .71445]
print ("\nInput array : \n", in_array)

rintoff_values = np.rint(in_array)
print ("\nRounded values : \n", rintoff_values)
```

**Output:**

```py
Input array : 
 [0.5, 1.5, 2.5, 3.5, 4.5, 10.1]

Rounded values : 
 [  0\.   2\.   2\.   4\.   4\.  10.]

Input array : 
 [0.53, 1.54, 0.71]

Rounded values : 
 [ 1\.  2\.  1.]

Input array : 
 [0.5538, 1.33354, 0.71445]

Rounded values : 
 [ 1\.  1\.  1.]

```

**代码#2:工作**

```py
# Python program explaining
# rint() function
import numpy as np

in_array = [1 ,4, 7, 9, 12]
print ("Input array : \n", in_array)

rintoff_values = np.rint(in_array)
print ("\nRounded values : \n", rintoff_values)

in_array = [133 ,344, 437, 449, 12]
print ("\nInput array : \n", in_array)

rintoff_values = np.rint(in_array)
print ("\nRounded values upto 2: \n", rintoff_values)

in_array = [133 ,344, 437, 449, 12]
print ("\nInput array : \n", in_array)

rintoff_values = np.rint(in_array)
print ("\nRounded values upto 3: \n", rintoff_values)
```

**Output:**

```py
Input array : 
 [1, 4, 7, 9, 12]

Rounded values : 
 [  1\.   4\.   7\.   9\.  12.]

Input array : 
 [133, 344, 437, 449, 12]

Rounded values upto 2: 
 [ 133\.  344\.  437\.  449\.   12.]

Input array : 
 [133, 344, 437, 449, 12]

Rounded values upto 3: 
 [ 133\.  344\.  437\.  449\.   12.]

```

**参考文献:**[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . rint . html # numpy . rint](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.rint.html#numpy.rint)
。