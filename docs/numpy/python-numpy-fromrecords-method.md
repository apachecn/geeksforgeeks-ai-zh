# Python | Numpy fromrecords()方法

> 原文:[https://www . geesforgeks . org/python-numpy-from records-method/](https://www.geeksforgeeks.org/python-numpy-fromrecords-method/)

借助`**numpy.core.fromrecords()**`方法，我们可以使用`numpy.core.fromrecords()`方法使用单个记录的列表来创建记录数组。

> **语法:** `numpy.core.fromrecords([(tup1), (tup2)], metadata)`
> 
> **返回:**返回数组的记录。

**示例#1 :**

在这个例子中我们可以看到，使用`numpy.core.fromrecords()`方法，我们能够通过使用列表的单个记录来获得记录数组。

```py
# import numpy
import numpy as np

# using numpy.core.fromrecords() method
gfg = np.core.records.fromrecords([(101, 'Jitender', 21),
                                    (102, 'Deepak', 20)], 
                            names = 'Rollno, Name, Age')

print(gfg[0])
```

**输出:**

> (101，' jitender '，21)

**例 2 :**

```py
# import numpy
import numpy as np

# using numpy.core.fromrecords() method
gfg = np.core.records.fromrecords([(101, 'Jitender', 21),
                                    (102, 'Deepak', 20)],
                             names = 'Rollno, Name, Age')

print(gfg.Name)
```

**输出:**

> [“吉坦德”“迪帕克”]