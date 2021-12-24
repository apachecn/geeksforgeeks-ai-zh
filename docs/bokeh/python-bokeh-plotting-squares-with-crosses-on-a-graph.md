# Python Bokeh–在图形上绘制带十字的正方形

> 原文:[https://www . geesforgeks . org/python-bokeh-绘图-图形上带十字的正方形/](https://www.geeksforgeeks.org/python-bokeh-plotting-squares-with-crosses-on-a-graph/)

Bokeh 是一个 Python 交互式数据可视化工具。它使用 HTML 和 JavaScript 来渲染它的图。它以现代网络浏览器为呈现目标，提供优雅、简洁的新颖图形结构和高性能交互性。

Bokeh 可用于在图形上绘制带有十字的正方形。可以使用`plotting`模块的`square_cross()`方法在图形上绘制带有十字的正方形。

## ploting . figure . square _ cross()

> **语法:** square_cross(参数)
> 
> **参数:**
> 
> *   **x :** 正方形中心的 x 坐标
> *   **y :** 正方形中心的 y 坐标
> 
> **返回:**类的一个对象`GlyphRenderer`

**示例 1 :** 在本例中，我们将使用默认值绘制图表。

```py
# importing the modules
from bokeh.plotting import figure, output_file, show

# file to save the model
output_file("gfg.html")

# instantiating the figure object
graph = figure(title = "Bokeh Square Cross Graph")

# the points to be plotted
x = 0
y = 0

# plotting the graph
graph.square_cross(x, y, size = 30, fill_color = None)

# displaying the model
show(graph)
```

**输出:**
![](img/f9a4b1cc03625e861d010292ceff3abc.png)

**示例 2 :** 在本例中，我们将使用各种其他参数绘制多个正方形

```py
# importing the modules 
from bokeh.plotting import figure, output_file, show 

# file to save the model 
output_file("gfg.html") 

# instantiating the figure object 
graph = figure(title = "Bokeh Square Cross Graph") 

# name of the x-axis 
graph.xaxis.axis_label = "x-axis"

# name of the y-axis 
graph.yaxis.axis_label = "y-axis"

# points to be plotted
x = [3, 3, 5]
y = [3, 3, 3]
size = [130, 100, 60]

# color value of the square
color = ["yellow", "red", "purple"]

# fill alpha value of the square
fill_alpha = [0.9, 0.7, 0.5]

# plotting the graph 
graph.square_cross(x, y,
                   size = size,
                   color = color,
                   fill_alpha = fill_alpha) 

# displaying the model 
show(graph)
```

**输出:**
![](img/e7ddcbe643ee22a38cf108c49ca3b453.png)