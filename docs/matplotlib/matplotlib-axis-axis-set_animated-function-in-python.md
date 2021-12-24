# Python 中的 matplotlib . axis . axis . set _ animated()函数

> 原文:[https://www . geesforgeks . org/matplotlib-axis-axis-set _ animated-function-in-python/](https://www.geeksforgeeks.org/matplotlib-axis-axis-set_animated-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . set _ animated()函数

matplotlib 库的 Axis 模块中的 **Axis.set_animated()函数**用于设置艺术家的动画状态。

> **语法:** Axis.set_animated(self，b)
> 
> **参数:**该方法接受以下参数。
> 
> *   **b:** 该参数为布尔值。
> 
> **返回值:**此方法不返回值。

以下示例说明 matplotlib . axis . axis . set _ animated()函数在 matplotlib.axis:
**示例 1:**

## 蟒蛇 3

```py
# Implementation of matplotlib function
from matplotlib.axis import Axis
import numpy as np  
import matplotlib.pyplot as plt  
import matplotlib.animation as animation  

data = np.array([[1, 2, 3, 4, 5],   
                 [7, 4, 9, 2, 3]])  

fig = plt.figure()  
ax = plt.axes(xlim =(0, 20), ylim =(0, 20))  

line, = ax.plot([], [], 'r-')  
annotation = ax.annotate('',  
                         xy =(data[0][0],  
                              data[1][0]))  

Axis.set_animated(annotation, True)  

def init():  
    return line, annotation  

def update(num):  
    newData = np.array([[1 + num,  
                         2 + num // 2,  
                         3,  
                         4 - num // 4,  
                         5 + num],  
                        [7, 4,   
                         9 + num // 3,  
                         2, 3]])  

    line.set_data(newData)  
    return line, annotation  

anim = animation.FuncAnimation(fig,  
                               update,   
                               frames = 25,  
                               init_func = init,  
                               interval = 60,  
                               blit = True) 

fig.suptitle('matplotlib.axis.Axis.set_animated() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

<video class="wp-video-shortcode" id="video-429063-1" width="665" height="374" preload="metadata" controls=""><source type="video/webm" src="https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200611141943/python-matplotlib-set-animation-tick-11.webm?_=1">[https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200611141943/python-matplotlib-set-animation-tick-11.webm](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200611141943/python-matplotlib-set-animation-tick-11.webm)</video>

**例 2:**

## 蟒蛇 3

```py
# Implementation of matplotlib function
from matplotlib.axis import Axis
import numpy as np  
import matplotlib.pyplot as plt  
import matplotlib.animation as animation  

fig, ax = plt.subplots()  

ax.set_xlim([-1, 1])  
ax.set_ylim([-1, 1])  

L = 50
theta = np.linspace(0, 2 * np.pi, L)  
r = np.ones_like(theta)  

x = r * np.cos(theta)  
y = r * np.sin(theta)  

line, = ax.plot(1, 0, 'ro')  

annotation = ax.annotate(  
    'annotation', xy =(1, 0), xytext =(-1, 0),  
    arrowprops = {'arrowstyle': "->"}  
)  
Axis.set_animated(annotation, False)  

def update(i):  

    new_x = x[i % L]  
    new_y = y[i % L]  
    line.set_data(new_x, new_y)  

    annotation.set_position((-new_x, -new_y))  
    annotation.xy = (new_x, new_y)  

    return line, annotation  

ani = animation.FuncAnimation(  
    fig, update, interval = 50, blit = False
) 

fig.suptitle('matplotlib.axis.Axis.set_animated() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

<video class="wp-video-shortcode" id="video-429063-2" width="665" height="374" preload="metadata" controls=""><source type="video/webm" src="https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200611142147/python-matplotlib-set-animated-axis.webm?_=2">[https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200611142147/python-matplotlib-set-animated-axis.webm](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200611142147/python-matplotlib-set-animated-axis.webm)</video>