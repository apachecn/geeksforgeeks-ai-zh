# Python Bokeh–制作互动传说

> 原文:[https://www . geesforgeks . org/python-bokeh-making-interactive-legends/](https://www.geeksforgeeks.org/python-bokeh-making-interactive-legends/)

Bokeh 是一个 Python 交互式数据可视化工具。它使用 HTML 和 JavaScript 来渲染它的图。它以现代网络浏览器为呈现目标，提供优雅、简洁的新颖图形结构和高性能交互性。

## 如何制作互动传奇？

图表的图例反映了图表 Y 轴中显示的数据。在博克，传说对应于字形。有两种方法可以使图例互动:

*   隐藏
*   叛变

### 隐藏字形

通过将图例 click_policy 属性设置为“隐藏”，可以从图例中隐藏字形。

**示例:**

## 蟒蛇 3

```py
# importing the modules 
from bokeh.plotting import figure, output_file, show 

# file to save the model 
output_file("gfg.html") 

# instantiating the figure object 
graph = figure(title = "Bokeh Hiding Glyphs") 

# plotting the graph
graph.vbar(x = 1,  top = 5,
           width = 1, color = "violet",
           legend_label = "Violet Bar")
graph.vbar(x = 2,  top = 5,
           width = 1, color = "green",
           legend_label = "Green Bar")
graph.vbar(x = 3,  top = 5,
           width = 1, color = "yellow",
           legend_label = "Yellow Bar")
graph.vbar(x = 4,  top = 5,
           width = 1, color = "red",
           legend_label = "Red Bar")

# enable hiding of the glyphs
graph.legend.click_policy = "hide"

# displaying the model 
show(graph) 
```

**输出:**

<video class="wp-video-shortcode" id="video-453468-1" width="665" height="374" preload="metadata" controls=""><source type="video/webm" src="https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200716161208/python-bokeh-interactive-legend.webm?_=1">[https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200716161208/python-bokeh-interactive-legend.webm](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200716161208/python-bokeh-interactive-legend.webm)</video>

### 屏蔽字形

隐藏字形使其完全消失，另一方面，静音字形只是根据参数取消强调字形。通过将图例 click_policy 属性设置为“静音”，可以将图例中的字形静音。

## 蟒蛇 3

```py
# importing the modules 
from bokeh.plotting import figure, output_file, show 

# file to save the model 
output_file("gfg.html") 

# instantiating the figure object 
graph = figure(title = "Bokeh Hiding Glyphs") 

# plotting the graph
graph.vbar(x = 1,  top = 5,
           width = 1, color = "violet",
           legend_label = "Violet Bar",
           muted_alpha=0.2)
graph.vbar(x = 2,  top = 5,
           width = 1, color = "green",
           legend_label = "Green Bar",
           muted_alpha=0.2)
graph.vbar(x = 3,  top = 5,
           width = 1, color = "yellow",
           legend_label = "Yellow Bar",
           muted_alpha=0.2)
graph.vbar(x = 4,  top = 5,
           width = 1, color = "red",
           legend_label = "Red Bar",
           muted_alpha=0.2)

# enable hiding of the glyphs
graph.legend.click_policy = "mute"

# displaying the model 
show(graph) 
```

**输出:**

<video class="wp-video-shortcode" id="video-453468-2" width="665" height="374" preload="metadata" controls=""><source type="video/webm" src="https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200716161409/python-interactive-legend-bokeh.webm?_=2">[https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200716161409/python-interactive-legend-bokeh.webm](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200716161409/python-interactive-legend-bokeh.webm)</video>