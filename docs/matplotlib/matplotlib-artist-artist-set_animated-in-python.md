# Python 中的 matplotlib . artist . artist . set _ animated()

> 原文:[https://www . geesforgeks . org/matplotlib-artist-artist-set _ 动画-python/](https://www.geeksforgeeks.org/matplotlib-artist-artist-set_animated-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**艺术家类**包含抽象基类，用于渲染到图形画布中的对象。图形中所有可见的元素都是艺术家的子类。

## matplotlib . artist . artist . set _ animated()方法

matplotlib 库的 artist 模块中的 **set_animated()方法**用于设置艺术家的动画状态。

> **语法:** Artist.set_animated(self，b)
> 
> **参数:**该方法接受以下参数。
> 
> *   **b:** 该参数为布尔值。
> 
> **返回:**该方法不返回值。

下面的例子说明了 matplotlib 中的 matplotlib . artist . artist . set _ animated()函数:

**例 1:**

```
# Implementation of matplotlib function
from matplotlib.artist import Artist
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

Artist.set_animated(annotation, True) 

def init(): 
    return line, annotation 

def update(num): 
    newData = np.array([[1 + num, 
                         2 + num / 2, 
                         3, 
                         4 - num / 4, 
                         5 + num], 
                        [7, 4,  
                         9 + num / 3, 
                         2, 3]]) 

    line.set_data(newData) 
    return line, annotation 

anim = animation.FuncAnimation(fig, 
                               update,  
                               frames = 25, 
                               init_func = init, 
                               interval = 200, 
                               blit = True)
fig.suptitle('matplotlib.artist.Artist.set_animated()\
function Example', fontweight ="bold") 

plt.show()
```

**输出:**

<video class="wp-video-shortcode" id="video-411629-1" width="665" height="374" preload="metadata" controls=""><source type="video/webm" src="https://media.geeksforgeeks.org/wp-content/uploads/20200513163228/python-matplotlib-get-animation-1.webm?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200513163228/python-matplotlib-get-animation-1.webm](https://media.geeksforgeeks.org/wp-content/uploads/20200513163228/python-matplotlib-get-animation-1.webm)</video>

**例 2:**

```
# Implementation of matplotlib function
from matplotlib.artist import Artist  
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
Artist.set_animated(annotation, False) 

def update(i): 

    new_x = x[i % L] 
    new_y = y[i % L] 
    line.set_data(new_x, new_y) 

    annotation.set_position((-new_x, -new_y)) 
    annotation.xy = (new_x, new_y) 

    return line, annotation 

ani = animation.FuncAnimation( 
    fig, update, interval = 500, blit = False
)

fig.suptitle('matplotlib.artist.Artist.set_animated()\
function Example', fontweight ="bold") 

plt.show()
```

**输出:**

<video class="wp-video-shortcode" id="video-411629-2" width="665" height="374" preload="metadata" controls=""><source type="video/webm" src="https://media.geeksforgeeks.org/wp-content/uploads/20200513163514/python-matplotlib-get-animation-2.webm?_=2">[https://media.geeksforgeeks.org/wp-content/uploads/20200513163514/python-matplotlib-get-animation-2.webm](https://media.geeksforgeeks.org/wp-content/uploads/20200513163514/python-matplotlib-get-animation-2.webm)</video>