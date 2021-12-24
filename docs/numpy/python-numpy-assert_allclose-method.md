# Python | numpy . assert _ all close()方法

> 原文:[https://www . geeksforgeeks . org/python-numpy-assert _ all close-method/](https://www.geeksforgeeks.org/python-numpy-assert_allclose-method/)

借助`**numpy.assert_allclose()**`方法，使用`numpy.assert_allclose()`可以得到两个数组对象不相等时的断言错误。

> **语法:** `numpy.assert_allclose(actual_array, desired_array)`
> 
> **返回:**如果两个数组对象不相等，则返回断言错误。

**示例#1 :**
在这个示例中，我们可以看到，使用`numpy.assert_allclose()`方法，如果两个数组不相等，我们能够得到断言错误。

```
# import numpy
import numpy as np

# using numpy.assert_allclose() method
gfg1 = [1, 2, 3]
gfg2 = np.array(gfg1)

if np.testing.assert_allclose(gfg1, gfg2):
     print("Matched")
```

**输出:**

> 相配的

**例 2 :**

```
# import numpy
import numpy as np

# using numpy.assert_allclose() method
gfg1 = [1, 2, 3]
gfg2 = np.array([4, 5, 6])

print(np.testing.assert_allclose(gfg1, gfg2))
```

**输出:**

> 不匹配:100%
> 最大绝对差:3
> 最大相对差:0.75
> gfg1:数组([1，2，3])
> gfg2:数组([4，5，6])