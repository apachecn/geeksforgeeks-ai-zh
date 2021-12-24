# Python | Numpy NP . assert _ array _ less()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-assert _ array _ less-method/](https://www.geeksforgeeks.org/python-numpy-np-assert_array_less-method/)

借助`**np.assert_array_less()**`方法，如果两个数组似的对象没有使用`np.assert_array_less()`方法按小于排序，就可以得到断言错误。

> **语法:** `np.assert_array_less(x, y)`
> **返回:**如果两个数组对象不相等，返回断言错误。

**示例#1 :**
在这个示例中，我们可以看到，使用`np.assert_array_less()`方法，如果两个类似数组的对象不相等，则我们能够得到断言错误。

```
# import numpy and assert_array_less
import numpy as np
import numpy.testing as npt

# using np.assert_array_less() method
gfg = npt.assert_array_less([3, 4], [1, 2])

print(gfg)
```

**输出:**

> 断言错误:
> 数组的顺序不低
> 
> 不匹配:100%
> 最大绝对差:2
> 最大相对差:2。
> x:数组([3，4])
> y:数组([1，2])

**例 2 :**

```
# import numpy and assert_array_less
import numpy as np
import numpy.testing as npt

# using np.assert_array_less() method
gfg = npt.assert_array_less([0.1, 1], [1, 2])

print(gfg)
```

**输出:**

> 没有人