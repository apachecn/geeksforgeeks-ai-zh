# Python Bokeh–绘制竖条图

> 原文:[https://www . geesforgeks . org/python-bokeh-绘图-竖条-图表/](https://www.geeksforgeeks.org/python-bokeh-plotting-vertical-bar-graphs/)

Bokeh 是一个 Python 交互式数据可视化工具。它使用 HTML 和 JavaScript 来渲染它的图。它以现代网络浏览器为呈现目标，提供优雅、简洁的新颖图形结构和高性能交互性。
Bokeh 可用于绘制垂直条形图。可以使用绘图模块的 vbar()方法绘制垂直条形图。

## 标绘. figure.vbar()

> **语法:** vbar(参数)
> T3】参数:T5】
> 
> *   **x :** 竖条中心的 x 坐标
> *   **宽度:**竖条的厚度
> *   **顶部:**顶部边缘的 y 坐标
> *   **底部:**底部边缘的 y 坐标，默认为 0
> *   **填充α:**填充竖线的α值
> *   **填充颜色:**竖线的填充颜色值
> *   **阴影阿尔法:**垂直条的阴影阿尔法值，默认为 1
> *   **阴影 _ 颜色:**竖线的阴影颜色值，默认为黑色
> *   **阴影 _ 额外:**垂直条的阴影额外值
> *   **阴影 _ 图案:**竖线的阴影图案值
> *   **阴影 _ 比例:**竖线的阴影比例值，默认为 12
> *   **阴影 _ 重量:**垂直条的阴影重量值，默认为 1
> *   **line _ alpha:**line alpha 的百分比值，默认为 1
> *   **线帽:**线的线帽值，默认为对接
> *   **线条 _ 颜色:**线条的颜色，默认为黑色
> *   **线划:**线划的值如:
>     *   固体
>     *   虚线
>     *   有点的
>     *   dotdash！dotdash！dotdash
>     *   达什特
> 
> 默认为实心
> 
> *   **线划偏移量:**线划偏移量的值，默认为 0
> *   **线连接:**线连接的值，默认为斜角
> *   **线宽:**线宽值，默认为 1
> *   **名称:**用户提供的型号名称
> *   **标签:**用户为模型提供的值
> 
> **其他参数:**
> 
> *   **alpha :** 一次性设置所有 alpha 关键字参数
> *   **颜色:**一次性设置所有颜色关键字参数
> *   **legend_field :** 数据源中应使用的列的名称
> *   **legend_group :** 数据源中应使用的列的名称
> *   **图例 _ 标签:**标记图例条目
> *   **静音:**确定字形是否应该渲染为静音，默认为假
> *   **名称:**附加到渲染器的可选用户提供的名称
> *   **来源:**用户提供的数据源
> *   **视图:**用于过滤数据源的视图
> *   **可见:**决定是否渲染字形，默认为真
> *   **x_range_name :** 用于映射 x 坐标的额外范围的名称
> *   **y_range_name :** 用于映射 y 坐标的额外范围的名称
> *   **等级:**指定此字形的渲染等级顺序
> 
> **返回:**类的一个对象

**示例 1 :** 在本例中，我们将使用默认值绘制图表。

## 蟒蛇 3

```py
# importing the modules
from bokeh.plotting import figure, output_file, show

# file to save the model
output_file("gfg.html")

# instantiating the figure object
graph = figure(title = "Bokeh Vertical Bar Graph")

# x-coordinates to be plotted
x = [1, 2, 3, 4, 5]

# x-coordinates of the top edges
top = [1, 2, 3, 4, 5]

# width / thickness of the bars
width = 0.5

# plotting the graph
graph.vbar(x,
           top = top,
           width = width)

# displaying the model
show(graph)
```

**输出:**

![](img/1c267759574875d6491d57719a073fc4.png)

**示例 2 :** 在本例中，我们将绘制具有不同参数的竖线。

## 蟒蛇 3

```py
# importing the modules
from bokeh.plotting import figure, output_file, show

# file to save the model
output_file("gfg.html")

# instantiating the figure object
graph = figure(title = "Bokeh Vertical Bar Graph")

# name of the x-axis
graph.xaxis.axis_label = "x-axis"

# name of the y-axis
graph.yaxis.axis_label = "y-axis"

# x-coordinates to be plotted
x = [1, 2, 3, 4, 5]

# x-coordinates of the top edges
top = [1, 2, 3, 4, 5]

# width / thickness of the bars
width = [0.5, 0.4, 0.3, 0.2, 0.1]

# color values of the bars
fill_color = ["yellow", "pink", "blue", "green", "purple"]

# plotting the graph
graph.vbar(x,
           top = top,
           width = width,
           fill_color = fill_color)

# displaying the model
show(graph)
```

**输出:**

![](img/1284bb7c33e1d86737a02d6bc235ea2c.png)