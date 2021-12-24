# Python | Numpy NP . assert _ 几乎 _equal()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-assert _ 几乎 _equal-method/](https://www.geeksforgeeks.org/python-numpy-np-assert_almost_equal-method/)

借助`**np.assert_almost_equal()**`方法，我们可以通过`np.assert_almost_equal()`方法得到两项不等于期望精度值时的断言错误。

> **语法:** `np.assert_almost_equal(actual, desired, decimal)`
> **返回:**如果两个值不相等，则返回断言错误。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.assert_almost_equal()`方法，如果两个值不等于一个精度值，我们可以使用该方法获得断言错误。

```
# import numpy and assert_almost_equal
import numpy as np
import numpy.testing as npt

# using np.assert_almost_equal() method
gfg = npt.assert_almost_equal(1.2222222222, 1.2222222222, decimal = 5)

print(gfg)
```

**输出:**

> 不

**例 2 :**

```
# import numpy and assert_almost_equal
import numpy as np
import numpy.testing as npt

# using np.assert_almost_equal() method
gfg = npt.assert_almost_equal(1.2222222222, 1.2223422222, decimal = 5)

print(gfg)
```

**输出:**

> 断言错误:
> 数组几乎不等于 5 位小数
> 实际值:1.2222222222
> 期望值:1.22222222222