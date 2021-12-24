# Python 中的 matplotlib . animation . func animation 类

> 原文:[https://www . geesforgeks . org/matplotlib-animation-func animation-python 中的类/](https://www.geeksforgeeks.org/matplotlib-animation-funcanimation-class-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-matplotlib-an-overview/) 是 Python 中一个惊人的可视化库，用于数组的 2D 图。Matplotlib 是一个多平台数据可视化库，构建在 NumPy 数组上，旨在与更广泛的 SciPy 堆栈一起工作。

## matplotlib . animation 动画

**matplotlib . animation . FuncTion**类用于通过重复调用同一个函数(即 func)来制作动画。

> **语法:**class matplotlib . animation . func animation(fig，func，frames=None，init_func=None，fargs=None，save_count=None，* cache _ frame _ data = True，* * kwargs)
> **Paramwrite.geeksforgeeks.org/wp-admin/post.php?post=1675187&动作=编辑器:**
> 
> 1.  **图:**是用于绘图、调整大小或任何其他需要的事件的图形对象。
>     任何额外的位置参数都可以通过 fargs 参数提供。
>     
> 2.  **func:** 是每次被调用的可调用函数。帧中的下一个值通过第一个参数给出。任何其他位置参数都是通过 fargs 参数给出的。如果 blit 值等于 True，则 func 返回要修改或创建的所有艺术家的列表。块传送算法使用这些数据来决定图形的哪些部分需要更新。如果 blit== False，则返回的值未被使用或被省略。
>     
> 3.  **帧:**它可以是可迭代的、整数、生成器函数或无。这是一个可选的参数。它是传递给 func 和动画每一帧的数据源。
>     
> 4.  **init_func:** 是一个可选的可调用函数，用于绘制清晰的框架。
>     
> 5.  **fargs:** 它是一个可选参数，要么是元组，要么是无，这是一个额外的参数，需要传递给 func 的每个调用。
>     
> 6.  **save_count:** 它是一个整数，作为从帧到缓存的值数量的后备。仅当无法从帧中推断出帧数时，即当它是一个没有长度的迭代器或生成器时，才使用此选项。它的默认值是 100。
>     
> 7.  **间隔:**是可选的整数值，表示每帧之间的延迟，单位为毫秒。它的默认值是 100。
>     
> 8.  **repeat_delay:** 它是一个可选的整数值，在重复动画之前增加一个延迟(以毫秒为单位)。默认为无。
>     
> 9.  **blit:** 这是一个可选的布尔参数，用于控制 blitting 以优化绘图。
>     
> 10.  **cache_frame_data:** 是一个可选的布尔参数，用于控制数据的缓存。默认为真。

**该类方法:**

<figure class="table">

| **方法** | **描述** |
| --- | --- |
| __init__(self，fig，func[，frames，…]) | 初始化自我。 |
| 新框架序列(自身) | 返回新的帧信息序列。 |
| 新建 _ 保存 _ 框架 _ 序列(自身) | 返回保存/缓存的帧信息的新序列。 |
| 保存(自身、文件名[、写入程序、fps、dpi、…]) | 通过绘制每一帧，将动画保存为电影文件。 |
| to_html5_video(self[，embed_limit]) | 将动画转换为 HTML5 <video>标记。</video> |
| to_jshtml(self[，fps，embed_frames，…]) | 生成动画的 HTML 表示形式 |

</figure>

**例 1:**

## 蟒蛇 3

```
import matplotlib.animation as animation
import matplotlib.pyplot as plt
import numpy as np

# creating a blank window
# for the animation
fig = plt.figure()
axis = plt.axes(xlim =(-50, 50),
                ylim =(-50, 50))

line, = axis.plot([], [], lw = 2)

# what will our line dataset
# contain?
def init():
    line.set_data([], [])
    return line,

# initializing empty values
# for x and y co-ordinates
xdata, ydata = [], []

# animation function
def animate(i):
    # t is a parameter which varies
    # with the frame number
    t = 0.1 * i

    # x, y values to be plotted
    x = t * np.sin(t)
    y = t * np.cos(t)

    # appending values to the previously
    # empty x and y data holders
    xdata.append(x)
    ydata.append(y)
    line.set_data(xdata, ydata)

    return line,

# calling the animation function    
anim = animation.FuncAnimation(fig, animate,
                            init_func = init,
                            frames = 500,
                            interval = 20,
                            blit = True)

# saves the animation in our desktop
anim.save('growingCoil.mp4', writer = 'ffmpeg', fps = 30)
```

**输出:**

<video class="wp-video-shortcode" id="video-399838-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200418035925/growingCoil1.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200418035925/growingCoil1.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200418035925/growingCoil1.mp4)</video>

**例 2:**

## 蟒蛇 3

```
from matplotlib import pyplot as plt
import numpy as np
from matplotlib.animation import FuncAnimation

# initializing a figure in
# which the graph will be plotted
fig = plt.figure()

# marking the x-axis and y-axis
axis = plt.axes(xlim =(0, 4),
                ylim =(-2, 2))

# initializing a line variable
line, = axis.plot([], [], lw = 3)

# data which the line will
# contain (x, y)
def init():
    line.set_data([], [])
    return line,

def animate(i):
    x = np.linspace(0, 4, 1000)

    # plots a sine graph
    y = np.sin(2 * np.pi * (x - 0.01 * i))
    line.set_data(x, y)

    return line,

anim = FuncAnimation(fig, animate,
                    init_func = init,
                    frames = 200,
                    interval = 20,
                    blit = True)

anim.save('continuousSineWave.mp4',
          writer = 'ffmpeg', fps = 30)
```

**输出:**

<video class="wp-video-shortcode" id="video-399838-2" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200418035707/continuousSineWave.mp4?_=2">[https://media.geeksforgeeks.org/wp-content/uploads/20200418035707/continuousSineWave.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200418035707/continuousSineWave.mp4)</video>