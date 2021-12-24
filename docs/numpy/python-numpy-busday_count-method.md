# Python | numpy.busday_count()方法

> 原文:[https://www . geesforgeks . org/python-numpy-busday _ count-method/](https://www.geeksforgeeks.org/python-numpy-busday_count-method/)

借助`**numpy.busday_count()**`方法，我们可以通过`numpy.busday_count()`方法得到从开始日期到结束日期的所有有效天数的值，不包括结束日期。

> **语法:** `numpy.busday_count(start_date, end_date)`
> 
> **返回:**返回有效日期计数。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`numpy.busday_count()`方法，我们能够获得开始日期和结束日期之间的有效天数计数。

```py
# import numpy
import numpy as np

# using numpy.busday_count() method
gfg = np.busday_count('2019-09', '2019-10')

print(gfg)
```

**输出:**

> Twenty-one

**例 2 :**

```py
import numpy as np

# using numpy.busday_count() method
gfg = np.busday_count('2019-09', '2019-10', weekmask ='Sat')

print(gfg)
```

**输出:**

> four