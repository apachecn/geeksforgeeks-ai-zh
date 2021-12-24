# 如何在 seaborn 的各个子剧情图中添加居中对齐文字 it？

> 原文:[https://www . geesforgeks . org/如何添加-居中-对齐-每个子图中的文本-海洋中的图形/](https://www.geeksforgeeks.org/how-to-add-center-align-text-it-in-each-subplot-graph-in-seaborn/)

在这篇文章中，我们将看到如何使用 seaborn 在每个子剧情的中心添加文本。以标题为中心是表示数据可变性的好方法。它可以应用于图表，为所呈现的数据提供额外的信息层。

### 使用的功能:

[**FacetGrid**](https://www.geeksforgeeks.org/python-seaborn-facetgrid-method/)**:**这是一种基于函数绘制网格的通用方法。它帮助我们可视化变量的分布以及多个变量之间的关系。FacetGrid 对象使用数据框作为输入，以及构成网格的列、行、维度的变量的名称，语法如下:

> **语法:**海鸟。FacetGrid(数据，*\*kwargs)
> 
> *   **数据:**整齐的数据框，每一列为变量，每一行为观察值。
> *   **\*\*kwargs:** 它使用许多参数作为输入，例如行、列、色调、调色板等。

[**Map 方法:**](https://www.geeksforgeeks.org/python-map-function/)Map()方法广泛用于对一系列数据应用函数或操作。在对 iterable 和 return 的所有元素应用特定函数后，它会对作为输入的迭代器的所有项目应用函数

> **语法:**映射(函数，可迭代)
> 
> **参数:**
> 
> *   **所需功能:**为每个项目执行的功能
> *   **可迭代必选:**行列、序列或迭代器对象的集合。

**文字方法:**该功能用于在数据坐标中 x、y 位置的轴上添加文字。

> **语法:**文本(x，y，text，fontsize = int)
> 
> *   **x，y:** 放置文本的位置。
> *   **文字:**“你的文字”。
> *   **fontsize:** 整数形式的文本大小。

**以下是上述方法的实现:**

**例 1:** 这里我们通过调用 sns.regplot 绘制一个 regplot 图，这个方法用来绘制数据和一个线性回归模型。
这里我们有一个图表，我们在图表的内部某个区域添加了注释，我们在 x=10 和 y=120 的位置添加了文本，fontsize=12。请在下面找到我的代码:

## 蟒蛇 3

```
# Import Library
import seaborn as sns

# style must be one of white, dark,
# whitegrid, darkgrid (Optional)
sns.set_style("darkgrid") 

# Loading default data of seaborn
exercise = sns.load_dataset("exercise")
g = sns.FacetGrid(exercise, row="diet",
                  col="time", margin_titles = True)

g.map(sns.regplot, "id", "pulse", color = ".3")

# Set Title for each subplot
col_order=['Deltaic', 'Plains','Hummock',
           'Swale', 'Sand Dunes', 'Mountain']

# embedding center-text with its title
# using loop.
for txt, title in zip(g.axes.flat, col_order):
    txt.set_title(title)   

    # add text
    txt.text(10, 120,'Geeksforgeeks', fontsize = 12)
```