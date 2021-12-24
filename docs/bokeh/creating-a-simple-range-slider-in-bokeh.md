# 在 Bokeh 中创建一个简单的范围滑块

> 原文:[https://www . geesforgeks . org/creating-a-simple-range-slider-in-bokeh/](https://www.geeksforgeeks.org/creating-a-simple-range-slider-in-bokeh/)

范围滑块小部件允许您从具有起点和终点的滑块中选择浮点范围。Bokeh 小部件范围滑块由开始和结束值、步长、初始值和标题组成。

**语法:**

> range_slider = RangeSlider(开始、结束、值、步骤、标题)
> 
> range_slider.js_on_change(“值”，CustomJS(代码))

让我们看看创建范围滑块的过程。

*   **从 bokeh.models** 导入范围滑块部件

在这一步中，我们将从 bokeh .绘图界面导入图形和显示方法。Bokeh .绘图界面允许您通过组合各种元素(如网格、轴和其他工具)来创建绘图。figure()方法允许您向绘图中添加不同类型的字形，show()方法允许您在浏览器中显示可视化效果。同样，我们从 bokeh.layouts 导入布局来创建布局对象。最后，我们正在导入范围滑块来创建一个范围滑块，并使我们的可视化交互。

*   **设置数据和图形。**

在这一步中，我们将创建一个输出文件，它是一个 HTML 文件，并在浏览器的新窗口中打开。输出将显示在这个 HTML 文件中。figure 方法创建具有给定范围、高度和宽度的图形。

*   **创建范围滑块对象**

> **语法:**
> 
> 范围滑块(标题、开始、结束、步骤、值)
> 
> **参数:**
> 
> *   **标题:**表示范围滑块的标题。
> *   **Start** :表示范围的下限，类型为 float。
> *   **end** :表示范围的上限，类型为 float。
> *   **步骤**:表示数值之间的间隔，为浮点型。
> *   **值**:表示包含所选范围上下限值的元组。

*   **链接到 JavaScript**

javaScript 的链接是通过使用 link_js()函数将 RangeSlider 生成的值链接到您的绘图中来提供的。

**语法:**

> RangeSliderObject.js_link(值，p.x_range，开始/结束，attr_selector)

*   **创建所有想要在浏览器上显示的元素的布局。**

最后，我们使用布局方法来显示仪表板的所有元素，并在浏览器中显示布局。

**程序:**

## 计算机编程语言

```
from bokeh.plotting import figure, show

from bokeh.layouts import layout
from bokeh.models import RangeSlider

x = list(range(12))
y = [i**2 for i in x]

output_file = ('range_slider.html')
p = figure(x_range=(1, 9), plot_width=600, plot_height=300)
points = p.circle(x=x, y=y, size=40, fill_color="red")

range_slider = RangeSlider(
    title=" Adjust X-Axis range",
    start=0,
    end=12,
    step=1,
    value=(p.x_range.start, p.x_range.end),
)

range_slider.js_link("value", p.x_range, "start", attr_selector=0)
range_slider.js_link("value", p.x_range, "end", attr_selector=1)

layout = layout([range_slider], [p])
show(layout)
```

**输出:**

![](img/0448776c2dd31b1fbfa14d4e070f627c.png)