# Python | Numpy NP . assert _ string _ equal()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-assert _ string _ equal-method/](https://www.geeksforgeeks.org/python-numpy-np-assert_string_equal-method/)

借助`**np.assert_string_equal()**`方法，使用`np.assert_string_equal()`方法可以得到两个字符串不相等时的断言错误。

> **语法:** `np.assert_string_equal(actual, desired)`
> **返回:**如果两个字符串不相等，返回断言错误。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.assert_string_equal()`方法，如果两个字符串不相等，我们可以通过使用该方法获得断言错误。

```py
# import numpy and assert_string_equal
import numpy as np
import numpy.testing as npt

# using np.assert_string_equal() method
gfg = npt.assert_string_equal('gfg', 'gfg')

print(gfg)
```

**输出:**

> 没有人

**例 2 :**

```py
# import numpy and assert_string_equal
import numpy as np
import numpy.testing as npt

# using np.assert_string_equal() method
gfg = npt.assert_string_equal('gfg', 'geeksforgeeks')

print(gfg)
```

**输出:**

> AssertionError:字符串的差异:
> –gfg+geeks forgeek