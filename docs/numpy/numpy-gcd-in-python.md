# Python 中的 numpy.gcd()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-gcd-in-python/

**`numpy.gcd(arr1, arr2, out = None, where = True, casting = ‘same_kind’, order = ‘K’, dtype = None)` :** 该数学函数帮助用户计算|arr1|和|arr2|元素的 GCD 值。

两个或两个以上不全为零的数的最大公约数(GCD)是除以每个数的最大正数。

**例:**求 120 和 2250 的 GCD

```py
120 = 2^3 * 3 * 5
2250 = 2 * 3^2 * 5^3

Now, GCD of 120 and 2250 = 2 * 3 * 5 = 30

```

> **参数:**
> **arr 1/arr 2:**【array _ like】输入数组。
> 
> **返回:**两个或多个数的最大公约数(GCD)。

**代码:**

```py
# Python program illustrating 
# gcd() method 
import numpy as np 

arr1 = [120, 24, 42, 10]
arr2 = [2250, 12, 20, 50]

print ("arr1 : ", arr1)
print ("arr2 : ", arr2)

print ("\nGCD of arr1 and arr2 : ", np.gcd(arr1, arr2))
print ("\nGCD of arr1 and 10   : ", np.gcd(arr1, 10))

```

**输出:**

```py
arr1 : [120, 24, 42, 10]
arr2 : [2250, 12, 20, 50]

GCD of arr1 and arr2 : [30, 12,  2, 10]

GCD of arr1 and 10   : [10,  2,  2, 10]

```