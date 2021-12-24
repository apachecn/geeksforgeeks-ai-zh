# Python 中的 matplotlib . axis . axis . get _ minarticlines()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-axis-get _ minorticklines-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-get_minorticklines-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . get _ minarticlines()函数

matplotlib 库的 Axis 模块中的 **Axis.get_minorticklines()函数**用于获取一个小刻度线作为 Line2D 实例的列表。

> **语法:**axis . get _ minarticlines(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回值:**该方法将次要刻度线作为线 2D 实例列表返回

下面的例子说明了 matplotlib.axis . axis . get _ minarticlines()函数在 matplotlib . axis 中的作用:

**例 1:**

## 蟒蛇 3

```py
# Implementation of matplotlib function 
from matplotlib.axis import Axis  
from matplotlib.artist import Artist 
from mpl_toolkits.mplot3d import axes3d   
import matplotlib.pyplot as plt   

fig, ax = plt.subplots()   

def tellme(s):   
    ax.set_title(s, fontsize = 16)   
    fig.canvas.draw()  
    renderer = fig.canvas.renderer  
    Artist.draw(ax, renderer)  

tellme("Matplotlib.axis.Axis.get_minorticklines()\n\
Function Example")
ax.grid()

print("Value of get_minorticklines() :",
      ax.xaxis.get_minorticklines())

plt.show()
```

**输出:**

![](img/5f18c34fc41ede35208093902584539e.png)

```py
Value of get_minorticklines() : <a list of 0 Line2D ticklines objects>
```

**例 2:**

## 蟒蛇 3

```py
# Implementation of matplotlib function 
from matplotlib.axis import Axis  
from matplotlib.artist import Artist 
from mpl_toolkits.mplot3d import axes3d   
import matplotlib.pyplot as plt   

fig = plt.figure()   
ax = fig.add_subplot(111, projection ='3d')   

X, Y, Z = axes3d.get_test_data(0.1)   
ax.plot_wireframe(X, Y, Z, rstride = 5,    
                  cstride = 5)   

ax.view_init(30, 50)  
fig.canvas.draw()  
renderer = fig.canvas.renderer  
Artist.draw(ax, renderer)   

fig.suptitle('Matplotlib.axis.Axis.get_minorticklines()\n\
Function Example')  
ax.grid()

print("Value of get_minorticklines() :",
      ax.xaxis.get_minorticklines())

plt.show()
```

**输出:**

![](img/d7994f4853daf150bdc489c476730d6f.png)

```py
Value of get_minorticklines() : <a list of 0 Line2D ticklines objects>

```