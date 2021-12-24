# Python 中的 numpy.fix()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-fix-python/

**numpy.fix()** 是一个数学函数，它将数组的元素舍入到最接近零的整数。舍入后的值以浮点形式返回。

> **语法:** numpy.fix(a，b =无)
> **参数:**
> 
> **a :** *【阵样】*输入待浮阵。
> **b:***【ndarray，可选】*输出阵。
> 
> **返回:**整数数组

**代码#1:工作**

```py
# Python program explaining
# fix() function

import numpy as np

in_array = [.5, 1.5, 2.5, 3.5, 4.5, 10.1]
print ("Input array : \n", in_array)

fixoff_values = np.fix(in_array)
print ("\nRounded values : \n", fixoff_values)

in_array = [.53, 1.54, .71]
print ("\nInput array : \n", in_array)

fixoff_values = np.fix(in_array)
print ("\nRounded values : \n", fixoff_values)

in_array = [.5538, 1.33354, .71445]
print ("\nInput array : \n", in_array)

fixoff_values = np.fix(in_array)
print ("\nRounded values : \n", fixoff_values)
```

**输出:**

```py
Input array : 
 [0.5, 1.5, 2.5, 3.5, 4.5, 10.1]

Rounded values : 
 [  0\.   1\.   2\.   3\.   4\.  10.]

Input array : 
 [0.53, 1.54, 0.71]

Rounded values : 
 [ 0\.  1\.  0.]

Input array : 
 [0.5538, 1.33354, 0.71445]

Rounded values : 
 [ 0\.  1\.  0.]
```

**代码#2:工作**

```py
# Python program explaining
# fix() function

import numpy as np

in_array = [1, 4, 7, 9, 12]
print ("Input array : \n", in_array)

fixoff_values = np.fix(in_array)
print ("\nRounded values : \n", fixoff_values)

in_array = [133, 344, 437, 449, 12]
print ("\nInput array : \n", in_array)

fixoff_values = np.fix(in_array)
print ("\nRounded values upto 2: \n", fixoff_values)

in_array = [133, 344, 437, 449, 12]
print ("\nInput array : \n", in_array)

fixoff_values = np.fix(in_array)
print ("\nRounded values upto 3: \n", fixoff_values)
```

**输出:**

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

**参考文献:**[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . fix . html # numpy . fix](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.fix.html#numpy.fix)
。