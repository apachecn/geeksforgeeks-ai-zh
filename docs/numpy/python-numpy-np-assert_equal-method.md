# Python | Numpy np.assert_equal()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-assert _ equal-method/](https://www.geeksforgeeks.org/python-numpy-np-assert_equal-method/)

借助`**np.assert_equal()**`方法，利用`np.assert_equal()`方法可以得到两个对象不相等时的断言错误。

> **语法:** `np.assert_equal(actual, desired)`
> **返回:**如果两个对象不相等，返回断言错误。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.assert_equal()`方法，我们能够在两个对象不相等时使用该方法得到断言错误。

```py
# import numpy and assert_equal
import numpy as np
import numpy.testing as npt

# using np.assert_equal() method
gfg = npt.assert_equal([1, 2], [1, 2])

print(gfg)
```

**输出:**

> 没有人

**例 2 :**

```py
# import numpy and assert_equal
import numpy as np
import numpy.testing as npt

# using np.assert_equal() method
gfg = npt.assert_equal([1, 2], [5, 2])

print(gfg)
```

**输出:**

> 资产错误:
> 项不相等:
> 项=0
> 
> 实际:1
> 期望:5