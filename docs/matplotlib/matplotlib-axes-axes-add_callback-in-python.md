# Python 中的 matplotlib . axes . axes . add _ callback()

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-add _ callback-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-add_callback-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib . axes . axes . add _ callback()方法

matplotlib 库的 axes 模块中的 **add_callback()方法**用于获取每次出图命令后是否重绘。

> **语法:** Axes.add_callback(self，func)
> 
> **参数:**该方法接受以下参数。
> 
> *   **功能:**该参数为回调函数
> 
> **返回:**这个方法返回与回调相关联的观察者 id。

下面的例子说明了 matplotlib 中的 matplotlib . axes . axes . add _ callback()函数:

**例 1:**

```py
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import numpy as np
import time

def update():
    plt.get_current_fig_manager().canvas.figure.patch.set_facecolor(str(np.random.random()))
    plt.draw()
    print("Draw at time :", time.time())

def start_animation():

    timer = fig.canvas.new_timer(interval = 50)
    timer.add_callback(update)
    timer.start()

fig, ax = plt.subplots()
start_animation()

ax.set_title('matplotlib.axes.Axes.add_callback() function\
 Example', fontweight ="bold") 

plt.show()
```

**输出:**

![python-matplotlib-add-callback1](img/c202c0a5b5298d59d32ff98fad40b76a.png)

**例 2:**

```py
# Implementation of matplotlib function  
from random import randint, choice 
import time 
import matplotlib.pyplot as plt 
import matplotlib.patches as mpatches 

back_color = "black"
colors = ['red', 'green', 'blue', 'purple'] 
width, height = 4, 4

fig, ax = plt.subplots() 
ax.set(xlim =[0, width], ylim =[0, height]) 

fig.canvas.draw() 

def update(): 
    x = randint(0, width - 1) 
    y = randint(0, height - 1) 

    arti = mpatches.Rectangle( 
        (x, y), 1, 1, 
        facecolor = choice(colors), 
        edgecolor = back_color 
    ) 
    ax.add_artist(arti)

    ax.draw_artist(arti) 
    fig.canvas.blit(ax.bbox) 
    print("Draw at time :", time.time()) 

timer = fig.canvas.new_timer(interval = 1) 
timer.add_callback(update) 
timer.start() 

ax.set_title('matplotlib.axes.Axes.add_callback() \
function Example', fontweight ="bold") 

plt.show()
```

**输出:**

<video class="wp-video-shortcode" id="video-407179-1" width="665" height="374" preload="metadata" controls=""><source type="video/webm" src="https://media.geeksforgeeks.org/wp-content/uploads/20200504222646/python-matplotlib-call-back-axes-class.webm?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200504222646/python-matplotlib-call-back-axes-class.webm](https://media.geeksforgeeks.org/wp-content/uploads/20200504222646/python-matplotlib-call-back-axes-class.webm)</video>