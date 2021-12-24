# Python | numpy.lookfor()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-lookfor-method/](https://www.geeksforgeeks.org/python-numpy-lookfor-method/)

借助`**numpy.lookfor()**`方法，我们可以使用`numpy.lookfor()`方法获取 numpy 中模块的信息。

> **语法:** `numpy.lookfor(module_name)`
> **返回:**返回模块相关信息。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`numpy.lookfor()`方法，我们能够获得关于模块的信息。

```
# import numpy
import numpy as np

# using numpy.lookfor() method
print(np.lookfor("isin"))
```

**输出:**

> 搜索结果“is in”
> ————
> numpy . is if
> 测试元素-正无穷大或负无穷大。
> 检查对象是否是路径库。路径对象。
> numpy.isin
> 计算“test_elements”中的元素，仅通过“element”广播。

**例 2 :**

```
# import numpy
import numpy as np

# using numpy.lookfor() method
print(np.lookfor("isdigit"))
```

**输出:**

> 搜索结果为“is digit”
> ————-
> numpy . bytes 0 . is digit
> b . is digit()->bool
> numpy . str 0 . is digit
> s . is digit()->bool
> numpy . chararray
> chararray(shape，itemsize=1，unicode=False，buffer=None，offset=0，
> numpy.char。