# Python | Numpy NP . assert _ approach _ equal()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-assert _ 近似 _equal-method/](https://www.geeksforgeeks.org/python-numpy-np-assert_approx_equal-method/)

借助`**np.assert_approx_equal()**`方法，使用`np.assert_approx_equal()`方法，如果两个项目不等于有效数字，我们可以得到断言错误。

> **语法:** `np.assert_approx_equal(actual, desired, significant)`
> **返回:**如果两个值不相等，则返回断言错误。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.assert_approx_equal()`方法，如果两个值不等于一个有效数字，我们可以使用该方法获得断言错误。

```
# import numpy and assert_approx_equal
import numpy as np
import numpy.testing as npt

# using np.assert_approx_equal() method
gfg = npt.assert_approx_equal(1.2222222222, 1.2222222222, significant = 5)

print(gfg)
```

**输出:**

> 不

**例 2 :**

```
# import numpy and assert_approx_equal
import numpy as np
import numpy.testing as npt

# using np.assert_approx_equal() method
gfg = npt.assert_approx_equal(1.2222222222, 1.23422222, significant = 5)

print(gfg)
```

**输出:**

> 资产部分错误:
> 项目不等于 5 个有效数字:
> 实际:1.2222222222】期望:1.2342222