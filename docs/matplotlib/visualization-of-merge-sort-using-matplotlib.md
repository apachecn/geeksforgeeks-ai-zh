# 使用 Matplotlib 可视化合并排序

> 原文:[https://www . geesforgeks . org/visualization-of-merge-sort-using-matplotlib/](https://www.geeksforgeeks.org/visualization-of-merge-sort-using-matplotlib/)

**先决条件:**[Matplotlib 简介](https://www.geeksforgeeks.org/python-introduction-matplotlib/)[合并排序](https://www.geeksforgeeks.org/merge-sort/)

通过分析和比较为比较和交换元素而进行的操作数量，可视化算法使理解它们变得更加容易。为此，我们将使用 matplotlib 绘制条形图来表示数组的元素，

**进场:**

1.  我们将生成一个包含随机元素的数组。
2.  将在该数组上调用该算法，并将使用 yield 语句而不是 return 语句来实现可视化。
3.  在比较和交换之后，我们将得出阵列的当前状态。因此，算法将返回一个生成器对象。
4.  Matplotlib 动画将用于可视化数组的比较和交换。
5.  数组将存储在 matplotlib bar 容器对象(“bar_rects”)中，其中每个 bar 的大小将等于数组中元素的相应值。
6.  matplotlib 动画的内置 FuncAnimation 方法将容器和生成器对象传递给用于创建动画的函数。动画的每一帧对应于生成器的一次迭代。
7.  重复调用动画函数会将矩形的高度设置为等于元素的值。

下面是上述方法的实现。

## 蟒蛇 3

```
# import all the modules
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation
from mpl_toolkits.mplot3d import axes3d
import matplotlib as mp
import numpy as np
import random

# function to recursively divide the arra
def mergesort(A, start, end):
    if end <= start:
        return

    mid = start + ((end - start + 1) // 2) - 1

    # yield from statements have been used to yield 
    # the array from the functions 
    yield from mergesort(A, start, mid)
    yield from mergesort(A, mid + 1, end)
    yield from merge(A, start, mid, end)

# function to merge the array
def merge(A, start, mid, end):
    merged = []
    leftIdx = start
    rightIdx = mid + 1

    while leftIdx <= mid and rightIdx <= end:
        if A[leftIdx] < A[rightIdx]:
            merged.append(A[leftIdx])
            leftIdx += 1
        else:
            merged.append(A[rightIdx])
            rightIdx += 1

    while leftIdx <= mid:
        merged.append(A[leftIdx])
        leftIdx += 1

    while rightIdx <= end:
        merged.append(A[rightIdx])
        rightIdx += 1

    for i in range(len(merged)):
        A[start + i] = merged[i]
        yield A

# function to plot bars
def showGraph():

    # for random unique values
    n=20
    a=[i for i in range(1, n+1)]
    random.shuffle(a)
    datasetName='Random'

    # generator object returned by the function
    generator = mergesort(a, 0, len(a)-1)
    algoName='Merge Sort'

    # style of the chart
    plt.style.use('fivethirtyeight')

    # set colors of the bars
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

    # bar container 
    bar_rects = ax.bar(range(len(a)), a, align="edge", 
                       color=color_map(data_normalizer(range(n))))

    # setting the limits of x and y axes
    ax.set_xlim(0, len(a))
    ax.set_ylim(0, int(1.1*len(a)))
    ax.set_title("ALGORITHM : "+algoName+"\n"+"DATA SET : "+datasetName, 
                 fontdict={'fontsize': 13, 'fontweight': 'medium', 
                           'color' : '#E4365D'})

    # the text to be shown on the upper left
    # indicating the number of iterations
    # transform indicates the position with 
    # relevance to the axes coordinates.
    text = ax.text(0.01, 0.95, "", transform=ax.transAxes, 
                   color="#E4365D")
    iteration = [0]

    def animate(A, rects, iteration):
        for rect, val in zip(rects, A):

            # setting the size of each bar equal 
            # to the value of the elements
            rect.set_height(val)
        iteration[0] += 1
        text.set_text("iterations : {}".format(iteration[0]))

    # call animate function repeatedly
    anim = FuncAnimation(fig, func=animate,
        fargs=(bar_rects, iteration), frames=generator, interval=50,
        repeat=False)
    plt.show()

showGraph()
```

**输出:**

<video class="wp-video-shortcode" id="video-458740-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200723011743/merge2d.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200723011743/merge2d.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200723011743/merge2d.mp4)</video>