# 如何在 Kivy 中添加 Matplotlib 图？

> 原文:[https://www . geesforgeks . org/how-add-matplotlib-graph-in-kivy/](https://www.geeksforgeeks.org/how-to-add-matplotlib-graph-in-kivy/)

在本文中，我们将讨论如何在 kivy 应用程序中添加 matplotlib 图。

#### 方法:

*   Import matplotlib pyplot
*   导入 numpy
*   import figurecanvas kivyagg(导入角色)
*   导入鄙视应用
*   Import deska
*   创建应用程序类
*   返回生成器字符串
*   运行类的实例

下面是实现。

## 蟒 3

```py
# importing pyplot for graph plotting
from matplotlib import pyplot as plt

# importing numpy
import numpy as np
from kivy.garden.matplotlib import FigureCanvasKivyAgg

# importing kivyapp
from kivy.app import App

# importing kivy builder
from kivy.lang import Builder

# this is the main class which will 
# render the whole application
class uiApp(App):

    def build(self):
        self.str = Builder.load_string(""" 

BoxLayout:
    layout:layout

    BoxLayout:

        id:layout

                                """)

        signal = [7, 89.6, 45.-56.34]

        signal = np.array(signal)

        # this will plot the signal on graph
        plt.plot(signal)

        # setting x label
        plt.xlabel('Time(s)')

        # setting y label
        plt.ylabel('signal (norm)')
        plt.grid(True, color='lightgray')

        # adding plot to kivy boxlayout
        self.str.layout.add_widget(FigureCanvasKivyAgg(plt.gcf()))
        return self.str

# running the application
uiApp().run()
```