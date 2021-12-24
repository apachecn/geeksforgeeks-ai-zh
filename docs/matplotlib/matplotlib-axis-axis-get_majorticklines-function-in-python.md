# Python 中的 matplotlib . axis . axis . get _ major chirines()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-axis-get _ major chirines-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-get_majorticklines-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . get _ major 怕痒()函数

matplotlib 库的 Axis 模块中的**axis . get _ major clinicnes()函数**用来获取一个主刻度线作为 Line2D 实例的列表。

> **语法:**axis . get _ major 怕痒(自我)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回值:**该方法将主要刻度线作为线 2D 实例列表返回

下面的例子说明了 matplotlib.axis . axis . get _ major chirines()函数在 matplotlib . axis 中的作用:

**例 1:**

## 蟒蛇 3

```
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

tellme("Matplotlib.axis.Axis.get_majorticklines()\n\
Function Example")
ax.grid()

print("Value of get_majorticklines() :")
for i in ax.xaxis.get_majorticklines():
    print(i)

plt.show()
```

**输出:**

![](img/abf6222b0e095f7459f93cc7f814689e.png)

```
Value of get_majorticklines() :
Line2D((0,0))
Line2D()
Line2D((0.2,0))
Line2D()
Line2D((0.4,0))
Line2D()
Line2D((0.6,0))
Line2D()
Line2D((0.8,0))
Line2D()
Line2D((1,0))
Line2D()

```

**例 2:**

## 蟒蛇 3

```
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

fig.suptitle('Matplotlib.axis.Axis.get_majorticklines()\n\
Function Example')  
ax.grid()

print("Value of get_majorticklines() :")
for i in ax.xaxis.get_majorticklines():
    print(i)

plt.show()
```

**输出:**

![](img/f207a1a18c00950fc9a0ce37141995d7.png)

```
Value of get_majorticklines() :
Line2D()
Line2D()
Line2D((0.0666078,-0.049272),(0.0682987,-0.0502952))
Line2D()
Line2D((0.0554732,-0.0546),(0.0571602,-0.0556407))
Line2D()
Line2D((0.0441478,-0.0600194),(0.0458304,-0.0610781))
Line2D()
Line2D((0.0326263,-0.0655326),(0.0343043,-0.0666097))
Line2D()
Line2D((0.0209039,-0.071142),(0.0225766,-0.072238))
Line2D()
Line2D((0.00897501,-0.0768502),(0.0106422,-0.0779655))
Line2D()
Line2D((-0.00316569,-0.0826597),(-0.00150454,-0.083795))
Line2D()
Line2D()
Line2D()

```