# Python 中的 matplotlib . axis . axis . get _ minorticklocs()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-axis-get _ minorticklocs-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-get_minorticklocs-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . get _ minorticklocs()函数

matplotlib 库的 Axis 模块中的 **Axis.get_minorticklocs()函数**用于获取数据坐标中的小刻度位置数组。

> **语法:**axis . get _ min articlocs(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回值:**此方法返回数据坐标中次要刻度位置的数组。

下面的例子说明了 matplotlib.axis . axis . get _ minorticklocs()函数在 matplotlib . axis 中的作用:

**例 1:**

## 蟒蛇 3

```py
# Implementation of matplotlib function 
from matplotlib.axis import Axis  
from matplotlib.artist import Artist 
from mpl_toolkits.mplot3d import axes3d   
import matplotlib.pyplot as plt
import matplotlib

fig, ax = plt.subplots()   

def tellme(s):   
    ax.set_title(s, fontsize = 16)   
    fig.canvas.draw()  
    renderer = fig.canvas.renderer  
    Artist.draw(ax, renderer)  

tellme("Matplotlib.axis.Axis.get_minorticklocs()\n\
Function Example")
ax.grid()  

print("Value of get_minorticklocs() :")
ax.xaxis.set_minor_locator(matplotlib.ticker.MultipleLocator(1))
for i in ax.xaxis.get_minorticklocs():
    print(i)

plt.show()
```

**输出:**

![](img/6f1a5e3a1224c63e0aa77b9caad8fddf.png)

```py
Value of get_minorticklocs() :
-1.0
2.0

```

**例 2:**

## 蟒蛇 3

```py
# Implementation of matplotlib function 
from matplotlib.axis import Axis  
from matplotlib.artist import Artist 
from mpl_toolkits.mplot3d import axes3d   
import matplotlib.pyplot as plt
import matplotlib

fig = plt.figure()   
ax = fig.add_subplot(111, projection ='3d')   

X, Y, Z = axes3d.get_test_data(0.1)   
ax.plot_wireframe(X, Y, Z, rstride = 5,    
                  cstride = 5)   

ax.view_init(30, 50)  
fig.canvas.draw()  
renderer = fig.canvas.renderer  
Artist.draw(ax, renderer)
ax.xaxis.set_minor_locator(matplotlib.ticker.MultipleLocator(8))

fig.suptitle('Matplotlib.axis.Axis.get_minorticklocs()\n\
Function Example')  
ax.grid()

print("Value of get_minorticklocs() :")
for i in ax.xaxis.get_minorticklocs():
    print(i)

plt.show()
```

**输出:**

![](img/17ae6333f4ae5b8b800e47288e4bab67.png)

```py
Value of get_minorticklocs() :
-32.0
-24.0
-16.0
-8.0
8.0
16.0
24.0
32.0

```