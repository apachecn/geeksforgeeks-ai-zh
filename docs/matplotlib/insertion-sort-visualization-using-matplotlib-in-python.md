# Python 中使用 Matplotlib 的插入排序可视化

> 原文:[https://www . geeksforgeeks . org/insert-sort-visualization-using-matplotlib-in-python/](https://www.geeksforgeeks.org/insertion-sort-visualization-using-matplotlib-in-python/)

**先决条件:** [插入排序](https://www.geeksforgeeks.org/insertion-sort/)[使用 Matplotlib 制作动画](https://www.geeksforgeeks.org/using-matplotlib-for-animations/)

通过分析和比较为比较和交换元素而进行的操作数量，可视化算法使理解它们变得更加容易。为此我们将使用 matplotlib，以[绘制条形图](https://www.geeksforgeeks.org/bar-plot-in-matplotlib/)来表示数组的元素，

**进场:**

1.  我们将生成一个包含随机元素的数组。
2.  将在该数组上调用该算法，并将使用 yield 语句而不是 return 语句来实现可视化。
3.  在比较和交换之后，我们将得出阵列的当前状态。因此，算法将返回一个生成器对象。
4.  [Matplotlib 动画](https://www.geeksforgeeks.org/using-matplotlib-for-animations/)将用于可视化数组的比较和交换。
5.  数组将存储在 matplotlib bar 容器对象(“rects”)中，其中每个 bar 的大小将等于数组中元素的相应值。
6.  matplotlib 动画的内置 FuncAnimation 方法将容器和生成器对象传递给用于创建动画的函数。动画的每一帧对应于生成器的一次迭代。
7.  重复调用动画函数会将矩形的高度设置为等于元素的值。

## 蟒蛇 3

```
# import all the modules
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation
import matplotlib as mp
import numpy as np
import random

# set the style of the graph
plt.style.use('fivethirtyeight')

# input the size of the array (list here)
# and shuffle the elements to create
# a random list
n = int(input("enter array size\n"))
a = [i for i in range(1, n+1)]
random.shuffle(a)

# insertion sort

def insertionsort(a):
    for j in range(1, len(a)):
        key = a[j]
        i = j-1

        while(i >= 0 and a[i] > key):
            a[i+1] = a[i]
            i -= 1

            # yield the current position
            # of elements in a
            yield a
        a[i+1] = key
        yield a

# generator object returned by the function
generator = insertionsort(a)

# to set the colors of the bars.
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

fig, ax = plt.subplots()

# the bar container
rects = ax.bar(range(len(a)), a, align="edge",
               color=color_map(data_normalizer(range(n))))

# setting the view limit of x and y axes
ax.set_xlim(0, len(a))
ax.set_ylim(0, int(1.1*len(a)))

# the text to be shown on the upper left
# indicating the number of iterations
# transform indicates the position with
# relevance to the axes coordinates.
text = ax.text(0.01, 0.95, "", transform=ax.transAxes)
iteration = [0]

# function to be called repeatedly to animate

def animate(A, rects, iteration):

    # setting the size of each bar equal
    # to the value of the elements
    for rect, val in zip(rects, A):
        rect.set_height(val)

    iteration[0] += 1
    text.set_text("iterations : {}".format(iteration[0]))

anim = FuncAnimation(fig, func=animate,
                     fargs=(rects, iteration), frames=generator, interval=50,
                     repeat=False)

plt.show()
```

**输出:**

<video class="wp-video-shortcode" id="video-449332-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200709151609/insertionsort.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200709151609/insertionsort.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200709151609/insertionsort.mp4)</video>