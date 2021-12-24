# 如何使用 Matplotlib 制作三维图形动画？

> 原文:[https://www . geeksforgeeks . org/how-animate-3d-graph-use-matplotlib/](https://www.geeksforgeeks.org/how-to-animate-3d-graph-using-matplotlib/)

**前提条件:**[【matplot lib】](https://www.geeksforgeeks.org/python-introduction-matplotlib/)、[【num py】](https://www.geeksforgeeks.org/python-numpy/)

图形表示总是容易理解，并且在任何书面或口头交流之前被采用和优选。使用 Matplotlib，我们可以绘制不同类型的图形数据。在这篇文章中，我们将试图理解，我们如何使用 matplotlib 创建一个美丽的图形，并使用 Matplotlib 创建一个三维动画图形。

**进场:**

*   导入所需模块。
*   创建三维图形
*   创建样本数据
*   制作 360 个视图的动画。
*   显示图形。

**第一步:**导入库。

## 蟒蛇 3

```py
from numpy import linspace
import matplotlib.pyplot as plt
from mpl_toolkits import mplot3d
```

**第二步:**使用 plt.figure()的目的是创建一个图形对象。我们将使用 plt.axes()创建单独的轴集，您将在其中绘制每一个轴。

## 蟒蛇 3

```py
from numpy import linspace
import matplotlib.pyplot as plt
from mpl_toolkits import mplot3d

fig = plt.figure(figsize = (8,8))
ax = plt.axes(projection = '3d')
```

**第三步:**在这一步中，我们将创建我们的数据并绘制不同的图表。

## 蟒蛇 3

```py
from numpy import linspace
import matplotlib.pyplot as plt
from mpl_toolkits import mplot3d
from scipy import signal

fig = plt.figure(figsize = (8,8))
ax = plt.axes(projection='3d')

t = np.linspace(0, 1, 1000, endpoint=True)
ax.plot3D(t, signal.square(2 * np.pi * 5 * t))
```

**第四步:**图形 360 度移动。

> view_init(elev=，azim=)这可用于以编程方式旋转轴。elev '存储 z 平面上的仰角。“azim”存储 x，y 平面中的方位角。构造函数。matplotlib 库 pyplot 模块中的 draw()函数用于重绘当前图形

## 蟒蛇 3

```py
from numpy import linspace
import matplotlib.pyplot as plt
from mpl_toolkits import mplot3d
from scipy import signal

fig = plt.figure(figsize = (8,8))
ax = plt.axes(projection='3d')

t = np.linspace(0, 1, 1000, endpoint=True)
ax.plot3D(t, signal.square(2 * np.pi * 5 * t))

for angle in range(0, 360):
   ax.view_init(angle,30)
   plt.draw()
   plt.pause(.001)
```

**例 1:** 在这个例子中，我们绘制了一个方波，我们将看到它的 360 度视图。

> linespace():linspace 函数是 Python 中用于创建数字序列的工具。matplotlib 库的 plot3D()功能用于进行三维绘图。

## 蟒蛇 3

```py
from numpy import linspace
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits import mplot3d
from scipy import signal

# Creating 3D figure
fig = plt.figure(figsize = (8, 8))
ax = plt.axes(projection = '3d')

# Creating Dataset
t = np.linspace(0, 1, 1000, endpoint = True)
ax.plot3D(t, signal.square(2 * np.pi * 5 * t))

# 360 Degree view
for angle in range(0, 360):
   ax.view_init(angle, 30)
   plt.draw()
   plt.pause(.001)

plt.show()
```

**输出:**

<video class="wp-video-shortcode" id="video-536148-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20201227002945/WhatsApp-Video-2020-12-27-at-12.25.28-AM.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20201227002945/WhatsApp-Video-2020-12-27-at-12.25.28-AM.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20201227002945/WhatsApp-Video-2020-12-27-at-12.25.28-AM.mp4)</video>

**示例 2:** 在本例中，我们绘制了一个螺旋图，我们将看到它的 360 度视图

## 蟒蛇 3

```py
from numpy import linspace
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits import mplot3d
from scipy import signal

# Creating 3D figure
fig = plt.figure(figsize = (8,8))
ax = plt.axes(projection='3d')

# Creating Dataset
z = np.linspace(0, 15, 1000)
x = np.sin(z)
y = np.cos(z)
ax.plot3D(x, y, z, 'green')

# 360 Degree view
for angle in range(0, 360):
    ax.view_init(angle, 30)
    plt.draw()
    plt.pause(.001)

plt.show()
```

**输出:**

<video class="wp-video-shortcode" id="video-536148-2" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20201227002947/WhatsApp-Video-2020-12-27-at-12.26.59-AM.mp4?_=2">[https://media.geeksforgeeks.org/wp-content/uploads/20201227002947/WhatsApp-Video-2020-12-27-at-12.26.59-AM.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20201227002947/WhatsApp-Video-2020-12-27-at-12.26.59-AM.mp4)</video>

**示例 3:** 在本例中，我们将显示抛物线图。

> PLT . rcparams(axes . prop _ cycle):-调用返回 itertoools . cycle .
> Linespace():linspace 函数是 Python 中创建数字序列的工具。

## 蟒蛇 3

```py
from numpy import linspace
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits import mplot3d
from scipy import signal

# Creating 3D figure
fig = plt.figure(figsize = (8,8))
ax = plt.axes(projection = '3d')

# Creating Dataset
color_cycle = plt.rcParams['axes.prop_cycle']()
x = linspace(0, 1, 51)
a = x*( 1 - x)    
b = 0.25 - a    
c = x*x*(1 - x)
d = 0.25-c    

ax.plot3D(x, a, **next(color_cycle))

# 360 Degree view
for angle in range(0, 360):
   ax.view_init(angle, 30)
   plt.draw()
   plt.pause(.001)

plt.show()
```

**输出:**

<video class="wp-video-shortcode" id="video-536148-3" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20201227002942/WhatsApp-Video-2020-12-27-at-12.24.39-AM.mp4?_=3">[https://media.geeksforgeeks.org/wp-content/uploads/20201227002942/WhatsApp-Video-2020-12-27-at-12.24.39-AM.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20201227002942/WhatsApp-Video-2020-12-27-at-12.24.39-AM.mp4)</video>