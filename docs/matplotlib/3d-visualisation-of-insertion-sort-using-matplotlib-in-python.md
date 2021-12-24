# 使用 Python 中的 Matplotlib 对插入排序进行三维可视化

> 原文:[https://www . geeksforgeeks . org/3d-可视化-插入-排序-使用-matplotlib-in-python/](https://www.geeksforgeeks.org/3d-visualisation-of-insertion-sort-using-matplotlib-in-python/)

**先决条件:** [插入排序](https://www.geeksforgeeks.org/insertion-sort/)[Matplotlib 简介](https://www.geeksforgeeks.org/python-introduction-matplotlib/)

通过分析和比较为比较和交换元素而进行的操作数量，可视化算法使理解它们变得更加容易。算法的三维可视化不太常见，为此，我们将使用 matplotlib 绘制条形图并制作动画来表示数组的元素。

**进场:**

1.  我们将生成一个包含随机元素的数组。
2.  将在该数组上调用该算法，并将使用 yield 语句而不是 return 语句来实现可视化。
3.  在比较和交换之后，我们将得出阵列的当前状态。因此，算法将返回一个生成器对象。
4.  Matplotlib 动画将用于可视化数组的比较和交换。
5.  然后我们将绘制图形，这将返回一个 Poly3dCollection 的对象，使用该对象可以进行进一步的动画制作。

下面是实现。

## 蟒蛇 3

```py
# import the modules
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation
from mpl_toolkits.mplot3d import axes3d
import matplotlib as mp
import numpy as np
import random

# Array size
n = 11

# insertion sort algorithm
def insertionsort(a):
    for j in range(1, len(a)):
        key = a[j]
        i = j-1

        while(i >= 0 and a[i] > key):
            a[i+1] = a[i]
            i -= 1
            yield a
        a[i+1] = key

        yield a

# method to plot graph
def showGraph(n):

    # for random unique values
    a = [i for i in range(1, n+1)]
    random.shuffle(a)
    datasetName = 'Random'
    algoName = 'Insertion Sort'

    # generator object returned by the function
    generator = insertionsort(a)

    # the style of the graph
    plt.style.use('fivethirtyeight')

    # set bar colors
    data_normalizer = mp.colors.Normalize()
    color_map = mp.colors.LinearSegmentedColormap(
        "my_map",
        {
            "red": [(0, 1.0, 1.0),
                    (1.0, .5, .5)],
            "green": [(0, 0.5, 0.5),
                      (1.0, 0, 0)],
            "blue": [(0, 0.50, 0.5),
                     (1.0, 0, 0)]
        }
    )

    # plot the array
    fig = plt.figure()
    ax = fig.add_subplot(projection='3d')

    # the z values and position of the bars
    z = np.zeros(n)
    dx = np.ones(n)
    dy = np.ones(n)
    dz = [i for i in range(len(a))]

    # plot 3d bars
    rects = ax.bar3d(range(len(a)), a, z, dx, dy, dz,
                     color=color_map(data_normalizer(range(n))))
    ax.set_xlim(0, len(a))
    ax.set_ylim(0, int(1.1*len(a)))
    ax.set_title("ALGORITHM : "+algoName+"\n"+"DATA SET : "+datasetName,
                 fontdict={'fontsize': 13, 
                           'fontweight': 'medium', 
                           'color': '#E4365D'})

    # 2D text placed on the upper left 
    # based on the axes fraction
    text = ax.text2D(0.1, 0.95, "", 
                     horizontalalignment='center',
                     verticalalignment='center', 
                     transform=ax.transAxes,
                     color="#E4365D")
    iteration = [0]

    # function for animating
    def animate(A, rects, iteration):

        # to clear the bars from the 
        # Poly3DCollection object
        ax.collections.clear()
        ax.bar3d(range(len(a)), A, z, dx, dy, dz,
                 color=color_map(data_normalizer(range(n))))
        iteration[0] += 1
        text.set_text("iterations : {}".format(iteration[0]))

    anim = FuncAnimation(fig, func=animate,
                         fargs=(rects, iteration),
                         frames=generator, interval=50,
                         repeat=False)
    plt.show()

# Driver Code
showGraph(n)
```

**输出:**

<video class="wp-video-shortcode" id="video-456504-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200716195218/3dgfg.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200716195218/3dgfg.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200716195218/3dgfg.mp4)</video>