# Python 中的 matplotlib . axes . axes . get _ default _ bbox _ extra _ artists()

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-get _ default _ bbox _ extra _ artists-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-get_default_bbox_extra_artists-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib . axes . axes . get _ default _ bbox _ extra _ artists()函数

matplotlib 库的 Axes 模块中的**axes . get _ default _ bbox _ extra _ artists()函数**用于获取用于边界框计算的默认艺术家列表..

> **语法:**axes . get _ default _ bbox _ extra _ artists(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回:**该方法返回用于边界框计算的默认艺术家列表。

下面的例子说明了 matplotlib.axes . axes . get _ default _ bbox _ extra _ artists()函数在 matplotlib . axes 中的作用:

**例 1:**

```
# ImpleIn Reviewtation of matplotlib function  
import matplotlib.pyplot as plt
import matplotlib.tri as tri
import numpy as np

n_angles = 36
n_radii = 10
min_radius = 2
radii = np.linspace(min_radius, 0.95, n_radii)

angles = np.linspace(0, 2 * np.pi,
                     n_angles,
                     endpoint = False)

angles = np.repeat(angles[..., np.newaxis],
                   n_radii, axis = 1)

angles[:, 1::2] += 2 * np.pi / n_angles

x = (radii * np.cos(angles)).flatten()
y = (radii * np.sin(angles)).flatten()

triang = tri.Triangulation(x, y)

triang.set_mask(np.hypot(x[triang.triangles].mean(axis = 1),
                         y[triang.triangles].mean(axis = 1))
                < min_radius)
fig, ax = plt.subplots()

ax.triplot(triang, 'bo-', lw = 1, color = "green")

w = ax.get_default_bbox_extra_artists()

print("Value Return by get_default_bbox_extra_artists() :")

for i in w:
    print(i)

fig.suptitle('matplotlib.axes.Axes.get_default_bbox_extra_artists()\
 function Example\n\n', fontweight ="bold")

fig.canvas.draw()
plt.show()
```

**输出:**

![](img/3729fa081f56d3396b21111f65a13b6e.png)

```
Value Return by get_default_bbox_extra_artists() :
Line2D(_line0)
Line2D(_line1)
Spine
Spine
Spine
Spine
XAxis(80.0, 52.8)
YAxis(80.0, 52.8)
Text(0.5, 1.0, '')
Text(0.0, 1.0, '')
Text(1.0, 1.0, '')
Rectangle(xy=(0, 0), width=1, height=1, angle=0)

```

**例 2:**

```
# ImpleIn Reviewtation of matplotlib function  
import matplotlib.pyplot as plt

fig, ax1 = plt.subplots( )
ax1.set_xscale("log")
ax1.set_yscale("log")
ax1.set_adjustable("datalim")

ax1.plot([1, 3, 34, 4, 46, 3, 7, 45, 10],
         [1, 9, 27, 8, 29, 84, 78, 19, 48], 
         "o-", color ="green")

ax1.set_xlim(1e-1, 1e2)
ax1.set_ylim(1, 1e2)

w = ax1.get_default_bbox_extra_artists()

print("Value Return by get_default_bbox_extra_artists() :")

for i in w:
    print(i)

fig.suptitle('matplotlib.axes.Axes.get_default_bbox_extra_artists()\
 function Example\n\n', fontweight ="bold")

fig.canvas.draw()

plt.show()
```

**输出:**

![](img/d90b5273a63833b3157d2036866fed99.png)

```
Value Return by get_default_bbox_extra_artists() :
Line2D(_line0)
Spine
Spine
Spine
Spine
XAxis(80.0, 52.8)
YAxis(80.0, 52.8)
Text(0.5, 1.0, '')
Text(0.0, 1.0, '')
Text(1.0, 1.0, '')
Rectangle(xy=(0, 0), width=1, height=1, angle=0)

```