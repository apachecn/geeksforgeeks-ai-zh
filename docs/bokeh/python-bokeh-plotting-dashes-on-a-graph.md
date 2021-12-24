# Python Bokeh–在图形上绘制虚线

> 原文:[https://www . geesforgeks . org/python-bokeh-绘图-图形上的破折号/](https://www.geeksforgeeks.org/python-bokeh-plotting-dashes-on-a-graph/)

Bokeh 是一个 Python 交互式数据可视化工具。它使用 HTML 和 JavaScript 来渲染它的图。它以现代网络浏览器为呈现目标，提供优雅、简洁的新颖图形结构和高性能交互性。

Bokeh 可用于在图形上绘制虚线。可以使用`plotting`模块的`dash()`方法在图形上绘制虚线。

## 标绘.图.虚线()

> **语法:**破折号(参数)
> 
> **参数:**
> 
> *   **x :** 虚线标记中心的 x 坐标
> *   **y :** 虚线标记中心的 y 坐标
> *   **尺寸:**虚线标记的直径，默认为 4
> *   **角度:**虚线标记的旋转角度，默认值为 0
> *   **角度 _ 单位:**角度的单位，默认为弧度
> *   **填充阿尔法:**填充破折号的阿尔法值
> *   **填充颜色:**虚线标记的填充颜色值
> *   **line _ alpha:**line alpha 的百分比值，默认为 1
> *   **线帽:**线的线帽值，默认为对接
> *   **线条 _ 颜色:**线条的颜色，默认为黑色
> *   **line_dash :** value of line dash such as :
>     *   固体
>     *   虚线
>     *   有点的
>     *   dotdash！dotdash！dotdash
>     *   达什特
>     
>     默认为实心
>     
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
> **返回:**类的一个对象`GlyphRenderer`

**示例 1 :** 在本例中，我们将使用默认值绘制图表。

```py
# importing the modules
from bokeh.plotting import figure, output_file, show

# file to save the model
output_file("gfg.html")

# instantiating the figure object
graph = figure(title = "Bokeh Dash Graph")

# the points to be plotted
x = [-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5]
y = [25, 16, 9, 4, 1, 0, 1, 4, 9, 16, 25]

# plotting the dashes
graph.dash(x, y)

# displaying the model
show(graph)
```

**输出:**
![](img/07f6c7aaae9350b9028603885f003a71.png)

**示例 2 :** 在本例中，我们将在其他参数旁边绘制虚线。

```py
# importing the modules
from bokeh.plotting import figure, output_file, show

# file to save the model
output_file("gfg.html")

# instantiating the figure object
graph = figure(title = "Bokeh Dash Graph")

# name of the x-axis
graph.xaxis.axis_label = "x-axis"

# name of the y-axis
graph.yaxis.axis_label = "y-axis"

# the points to be plotted
x = [-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5]
y = [25, 16, 9, 4, 1, 0, 1, 4, 9, 16, 25]

# size of the dashes
size = 20

# angle of the dashes
angle = 10

# color of the line
line_color = "red"

# type of line
line_dash = "dotted"

# offset of line dash
line_dash_offset = 1

# width of the dashes
line_width = 10

# name of the legend
legend_label = "Sample Dashes"

# plotting the line graph for AAPL
graph.dash(x, y,
           size = size,
           angle = angle,
           line_color = line_color,
           line_dash = line_dash,
           line_dash_offset = line_dash_offset,
           line_width = line_width,
           legend_label = legend_label)

# plotting the dashes
graph.dash(x, y)

# displaying the model
show(graph)
```

**输出:**
![](img/e878841bc849a3a6a0646a40a7181983.png)