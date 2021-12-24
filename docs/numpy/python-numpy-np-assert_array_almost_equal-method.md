# Python | Numpy NP . assert _ array _ near _ equal()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-assert _ array _ near _ equal-method/](https://www.geeksforgeeks.org/python-numpy-np-assert_array_almost_equal-method/)

借助`**np.assert_array_almost_equal()**`方法，我们可以通过`np.assert_array_almost_equal()`方法得到两个数组对象不等于期望精度值时的断言错误。

> **语法:** `np.assert_array_almost_equal(actual, desired, decimal)`
> **返回:**如果两个对象不相等，则返回断言错误。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.assert_array_almost_equal()`方法，如果两个数组对象不相等，我们可以通过使用该方法获得断言错误。

```
# import numpy and assert_array_almost_equal
import numpy as np
import numpy.testing as npt

# using np.assert_array_almost_equal() method
gfg = npt.assert_array_almost_equal([0.2222, 1.2222], [0.2222, 1.2222], decimal = 3)

print(gfg)
```

**输出:**

> 没有人

**例 2 :**

```
# import numpy and assert_array_almost_equal
import numpy as np
import numpy.testing as npt

# using np.assert_array_almost_equal() method
gfg = npt.assert_array_almost_equal([0.2322, 1.2622], [3.2222, 1.2222], decimal = 3)

print(gfg)
```

**输出:**

> 断言错误:
> 数组几乎不等于 3 位小数
> 
> 不匹配:100%
> 最大绝对差:2.99
> 最大相对差:0.92793743
> x:数组([0.232，1.262])
> y:数组([3.222，1.222])