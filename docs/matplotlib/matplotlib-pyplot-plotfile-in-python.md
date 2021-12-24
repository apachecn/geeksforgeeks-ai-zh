# Matplotlib.pyplot.plotfile()用 Python

表示

> 哎哎哎:# t0]https://www . geeksforgeeks . org/matplotlib-pyplot-python 打印文件/

借助`**pyplot.plotfile()**`方法，我们可以直接从给定的 csv 文件中绘制图形，我们不必使用`pyplot.plotfile()`方法为特定属性制作单独的数据框。

> **语法:** `pyplot.plotfile(datafile, (attr1, attr2, .....attrn))`
> 
> **返回:**返回图形上的属性图。

**示例#1:**
在这个示例中，我们可以看到，通过使用`pyplot.plotfile()`方法，我们能够通过使用`pyplot.plotfile()`方法给定的属性在图形上绘制 csv 文件数据。

```py
# import matplotlib
import matplotlib.pyplot as plt

# Provide the location of datafile
data = 'location_of_data_file'

# Using pyplot.plotfile() method
plt.plotfile(data, ('x_axis', 'y_axis'))
plt.show()
```

**示例#1 的数据文件:**

![](img/b0c35723969f3d179b52f0235e37dbf0.png)

**输出:**

![](img/e2f01b9746ba45497a6aeb4ee2e5b3ab.png)

**例 2 :**

```py
# import matplotlib
import matplotlib.pyplot as plt

# Provide the location of datafile
data = 'location_of_data_file'

# Using pyplot.plotfile() method
plt.plotfile(data, ('x_axis', 'y_axis', 'z_axis'))
plt.show()
```

**示例#2 的数据文件:**

![](img/0badbb4df64b371033d30d0f483460d0.png)

**输出:**

![](img/e008d7fda4080f011b5b81118ab6b2f0.png)