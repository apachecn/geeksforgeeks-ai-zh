# Python | Numpy NP . assert _ array _ equal()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-assert _ array _ equal-method/](https://www.geeksforgeeks.org/python-numpy-np-assert_array_equal-method/)

借助`**np.assert_array_equal()**`方法，使用`np.assert_array_equal()`方法可以得到两个数组类对象不相等时的断言错误。

> **语法:** `np.assert_array_equal(x, y)`
> **返回:**如果两个对象不相等，则返回断言错误。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.assert_array_equal()`方法，如果两个类似错误的对象不相等，我们可以通过使用这个方法得到断言错误。

```
# import numpy and assert_array_equal
import numpy as np
import numpy.testing as npt

# using np.assert_array_equal() method
gfg = npt.assert_array_equal([1.22, 0.22], [1.22, 0.22])

print(gfg)
```

**输出:**

> 没有人

**例 2 :**

```
# import numpy and assert_array_equal
import numpy as np
import numpy.testing as npt

# using np.assert_array_equal() method
gfg = npt.assert_array_equal([1.22, 1.22], [2.22, 0.22])

print(gfg)
```

**输出:**

> 断言错误:
> 数组不相等
> 
> 不匹配:100%
> 最大绝对差:1。
> 最大相对差:4.54545455
> x:数组([1.22，1.22])
> y:数组([2.22，0.22])