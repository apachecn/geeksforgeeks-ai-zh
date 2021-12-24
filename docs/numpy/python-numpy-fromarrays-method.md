# Python | Numpy fromarrays()方法

> 原文:[https://www . geeksforgeeks . org/python-numpy-from arrays-method/](https://www.geeksforgeeks.org/python-numpy-fromarrays-method/)

借助`**numpy.core.fromarrays()**`方法，我们可以使用`numpy.core.fromarrays()`方法使用不同数组的列表来创建记录数组。

> **语法:** `numpy.core.fromarrays([li1, li2....], metadata)`
> 
> **返回:**返回数组的记录。

**示例#1 :**

在这个例子中我们可以看到，使用`numpy.core.fromarrays()`方法，我们能够通过使用不同数组的列表来获得记录数组。

```
# import numpy
import numpy as np

# using numpy.core.fromarrays() method
li1 = np.array([101, 102, 103, 104])
li2 = np.array(['Jitender', 'Purnima', 'Ruhi', 'Varun'])
li3 = np.array([21, 22, 12, 35])

gfg = np.core.records.fromarrays([li1, li2, li3],
                      names ='Rollno, Name, Age')

print(gfg[1])
```

**输出:**

> （102， 'Purnima'， 22）

**例 2 :**

```
# import numpy
import numpy as np

# using numpy.core.fromarrays() method
li1 = np.array([101, 102, 103, 104])
li2 = np.array(['Jitender', 'Purnima', 'Ruhi', 'Varun'])
li3 = np.array([21, 22, 12, 35])

gfg = np.core.records.fromarrays([li1, li2, li3],
                      names ='Rollno, Name, Age')

print(gfg.Rollno)
print(gfg.Name)
print(gfg.Age)
```

**输出:**

> [101 102 103 104]
> [' jitender ' ' purnima ' ' ruhi ' ' varun '][21 22 12 35]