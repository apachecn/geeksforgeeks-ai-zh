# 如何用 Python 中的 Matplotlib 创建一个空图？

> 原文:[https://www . geeksforgeeks . org/如何用 python 中的 matplotlib 创建空图形/](https://www.geeksforgeeks.org/how-to-create-an-empty-figure-with-matplotlib-in-python/)

显式创建图形是一种面向对象的 matplotlib 接口方式。图形是创建绘图的基本构件，因为 Matplotlib 将我们的数据绘制在图形上。此图跟踪所有其他组件，如子轴、图例、标题、轴等。

创建空图形的步骤:

*   首先，我们导入 matplotlib 库，特别是 matplotlib 的 pyplot 模块。
*   然后，我们使用 PLT . fig()创建一个 fig 对象，并通过将其设置为“fig”变量来保持对该对象的引用。这个图形对象是空的，因为我们没有添加任何图形组件，如轴、图例、轴等。
*   我们正在使用 jupyter 笔记本，我们必须将后端更改为 ipympl *( <u>交互式后端</u> )* 因为默认后端显示了非 Gui 后端错误。

**要安装 ipympl，请在您的终端中运行以下命令:**

对于康达环境。

```
conda install ipympl -c conda-forge
```

对于普通 python 终端:

```
pip install ipympl
```

**下面是实现:**

**示例 1 :**

## 蟒蛇 3

```
# importing the library
import matplotlib

# Enabling interactive backend ipympl in
# jupyter notebook or you can use
# any other backend
%matplotlib ipympl

import matplotlib.pyplot as plt

# an empty figure with no axes
fig = plt.figure()  
```

**输出:**

![](img/8d2477e2040df5553819ef18b71a7176.png)

**例 2 :**

您也可以使用另一个交互式后端来显示您的图形，如 TkAgg(需要安装 TkInter)。

## 蟒蛇 3

```
# using different backend
import matplotlib
%matplotlib tk
import matplotlib.pyplot as plt

#creating a figure
fig = plt.figure()
```

**输出:**

![](img/d15d494692db42f0973c085b62556688.png)

图 2_gfg

**注意:**在不同的编辑器或 python shell 中显示图形将需要您玩后端。

show()方法也显示一个空的图形，但是您必须在使用 show()命令之前保存该图形。

**示例:**

在下面的示例中，我使用 figsize 属性来更改图形的大小。

## 蟒蛇 3

```
import matplotlib

# changing backend
%matplotlib tk
import matplotlib.pyplot as plt

# saving the figure
plt.savefig('testfigure.png',
            dpi = 100)

# displaying the figure
plt.show()
```

**输出:**

![](img/8d2477e2040df5553819ef18b71a7176.png)

图 3_gfg