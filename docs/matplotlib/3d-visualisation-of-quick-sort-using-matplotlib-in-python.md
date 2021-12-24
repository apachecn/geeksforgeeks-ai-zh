# Python 中使用 Matplotlib 快速排序的三维可视化

> 原文:[https://www . geeksforgeeks . org/3d-visualization-of-quick-sort-use-matplotlib-in-python/](https://www.geeksforgeeks.org/3d-visualisation-of-quick-sort-using-matplotlib-in-python/)

通过分析和比较为比较和交换元素而进行的操作数量，可视化算法使理解它们变得更加容易。算法的三维可视化不太常见，为此，我们将使用 [Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 绘制条形图并制作动画来表示数组的元素。

让我们看看[快速排序](https://www.geeksforgeeks.org/quick-sort/)的三维可视化:

## **进场:**

> 1.  We will generate an array with random elements.
> 2.  The algorithm will be called on the array, and for visualization purposes, the yield statement will be used instead of the return statement.
> 3.  We will get the current state of the array after comparison and exchange. Therefore, the algorithm will return a generator object.
> 4.  Matplotlib animation will be used to compare and exchange visual arrays.
> 5.  Then we will draw a graph, which will return a Poly3dCollection object, which will be used for further animation.

下面是实现:

## 蟒蛇 3

```py
# importing all required  modules
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation
from mpl_toolkits.mplot3d import axes3d
import matplotlib as mp
import numpy as np
import random

# quicksort function
def quicksort(a, l, r):
    if l>=r:
        return
    x=a[l]
    j=l
    for i in range(l+1, r+1):
        if a[i]<=x:
            j+=1
            a[j], a[i] = a[i], a[j]
        yield a
    a[l], a[j]=a[j], a[l]
    yield a

    # yield from statement used to yield
    # the array after dividing
    yield from quicksort(a, l, j-1)
    yield from quicksort(a, j+1, r)

# function to plot bars
def showGraph():

    # for random unique values
    n=int(input("enter array size\n"))
    a=[i for i in range(1, n+1)]
    random.shuffle(a)
    datasetName='Random'

    # generator object returned
    # by the function
    generator = quicksort(a, 0, n-1)

    algoName='Quick Sort'

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

    fig = plt.figure()

    ax = fig.add_subplot(projection='3d')

    # z values and posistions of the bars
    z = np.zeros(n)
    dx = np.ones(n)
    dy = np.ones(n)

    dz = [i for i in range(len(a))]
    # Poly3dCollection returned
    # into variable rects
    rects = ax.bar3d(range(len(a)), a, z, dx,
                     dy, dz,
                     color = color_map(data_normalizer(range(n))))

    # setting and x and y limits
    # equal to the length of the array
    ax.set_xlim(0, len(a))
    ax.set_ylim(0, int(1.1*len(a)))

    ax.set_title("ALGORITHM : "+algoName+"\n"+"DATA SET : "+datasetName,
                 fontdict={'fontsize': 13, 'fontweight': 'medium',
                           'color' : '#E4365D'})
    # text to plot on the chart
    text = ax.text2D(0.1,0.95, "", horizontalalignment = 'center',
                     verticalalignment = 'center',
                     transform=ax.transAxes,
                     color = "#E4365D")
    iteration = [0]

    # animation function to be
    # repeatedly called
    def animate(A, rects, iteration):

        # to clear the bars from
        # the Poly3DCollection object
        ax.collections.clear()
        ax.bar3d(range(len(a)), A, z, dx,
                 dy, dz,
                 color = color_map(data_normalizer(range(n))))

        iteration[0] += 1
        text.set_text("iterations : {}".format(iteration[0]))

    # animate function is called here
    # and the generator object is passed
    anim = FuncAnimation(fig, func=animate,
        fargs = (rects, iteration),
       frames = generator, interval=50,
        repeat=False)

    # show the plot
    plt.show()

# function call
showGraph()
```

**输出:**

对于阵列大小 20

<video class="wp-video-shortcode" id="video-458040-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20200723004918/quicksort3d.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20200723004918/quicksort3d.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20200723004918/quicksort3d.mp4)</video>