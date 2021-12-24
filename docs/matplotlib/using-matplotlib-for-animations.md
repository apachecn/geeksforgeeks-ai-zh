# 将 Matplotlib 用于动画

> 原文:[https://www . geeksforgeeks . org/using-matplotlib-for-animatics/](https://www.geeksforgeeks.org/using-matplotlib-for-animations/)

Python 的 Matplotlib 库是一个绘图工具，用于绘制函数或图形的图形。它也可以用作动画工具。当添加动画时，绘制的图表提供了更强大的可视化，并帮助演示者吸引更多的观众。Matplotlib 还可以轻松地与熊猫连接，创建更复杂的动画。

Matplotlib 中的动画可以通过两种方式使用`Animation`类制作:

*   **通过一遍又一遍地调用函数:**它使用一个预定义的函数，当这个函数一次又一次地运行时，会创建一个动画。
*   **通过使用固定对象:**一些动画艺术对象在与其他对象组合时产生动画场景。

需要注意的是，我们必须始终保持对动画对象的引用，否则动画将停止。这是因为`Animation class`保存了对动画对象的单个指针引用，并且随着时间的推移运行动画，必须保留该指针引用，否则它将作为垃圾值被收集。

虽然有两种方法，但第一种方法更常见、更方便，在这里，我们将只使用这种方法。不过，你也可以看其他的文档，这里。

让我们深入了解 Matplotlib 动画。

> **所需安装:**
> 
> 1.`Numpy`和`Matplotlib`
> 2。`ffmpeg`
> 
> *从[这里](https://pypi.org/project/ffmpeg-python/)下载 Python 的 ffmpeg。*

我们来看一个例子。在这里，我们将尝试使用动画和绘图工具制作连续正弦波。为此我们将利用`matplotlib`的`numpy`和`pyplot`。如前所述，我们将使用功能方法，而不是艺术对象。

**注意:**要将动画保存到电脑，请使用 **`anim.save(filename)`** 或 **`Animation.to_html5_video`** 。

```py
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

anim = FuncAnimation(fig, animate, init_func = init,
                     frames = 200, interval = 20, blit = True)

anim.save('continuousSineWave.mp4', 
          writer = 'ffmpeg', fps = 30))
```

首先，在导入必需品后，我们设置一个空白的图形或空白的窗口，在上面绘制整个动画。接下来，我们初始化一个变量`line`，它将包含图的 x 和 y 坐标。这些一开始是空的，因为其中的数据会因为动画而不断变化。最后，我们陈述动画函数`animate(i)`，它接受一个参数 **i** ，其中 **i** 被称为帧数，并使用它创建正弦波(或任何其他图形)，它将根据 **i** 的值不断变化。在最后一行`anim = FuncAnimation(fig, animate, init_func=init, frames=200, interval=20, blit=True)`中，我们使用`FuncAnimation`功能创建一个动画，该动画将每秒显示 200 帧，时间间隔为 20 微秒。

**输出:**

<video class="wp-video-shortcode" id="video-380113-1" width="665" height="447" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200113213401/sine.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200113213401/sine.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200113213401/sine.mp4)</video>

这是一个非常强大的可视化。需要注意的一点是，当我们查看保存的 gif 时，它将是一个连续的剪辑，不像我们输出中的视频会在几秒钟内终止。让我们再看一个例子。当我们编写程序时，试着猜测输出，因为它会澄清我们的概念。

```py
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
anim = animation.FuncAnimation(fig, animate, init_func = init, 
                               frames = 500, interval = 20, blit = True) 

# saves the animation in our desktop
anim.save('growingCoil.mp4', writer = 'ffmpeg', fps = 30)
```

正如我们可能已经猜到的，正如保存的文件名所示，这是一个不断增长的线圈动画。和以前一样，我们首先导入所有模块。但是这次，我们完全导入了`matplotlib.animation`库

```py
import matplotlib.animation as animation
```

然而，在前面的例子中，我们只从其中导入了`FuncAnimation`函数

```py
from matplotlib.animation import FuncAnimation
```

然而，这并没有真正做出任何改变，人们可以选择任何导入方式。然后我们创建一个将放置动画的图形。`animate`功能因帧数 **i** 而异。有一点要知道，线圈只不过是正弦和余弦的复合函数。我们取 x 轴上的正弦函数和 y 轴上的余弦函数，结果图给出了一个线圈。

**输出:**

<video class="wp-video-shortcode" id="video-380113-2" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200113213446/growingCoil.mp4?_=2">[https://media.geeksforgeeks.org/wp-content/uploads/20200113213446/growingCoil.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200113213446/growingCoil.mp4)</video>

因此，我们得出结论，利用`matplotlib`的一些基本知识可以制作许多有趣的动画。当一个人需要在不使用更高级别的动画工具(如 Blender)的情况下，用额外的动画力量呈现一些可视化效果时，这真的会很方便。