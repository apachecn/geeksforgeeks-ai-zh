# 旋转 Seaborn 和 Matplotlib 中的轴刻度标签

> 原文:[https://www . geesforgeks . org/rotate-axis-tick-labels-in-seaborn-and-matplotlib/](https://www.geeksforgeeks.org/rotate-axis-tick-labels-in-seaborn-and-matplotlib/)

[Seaborn](https://www.geeksforgeeks.org/boxplot-using-seaborn-in-python/) 和 [Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 都是 Python 中数据可视化常用的库。我们可以使用 Matplotlib 绘制各种类型的图，如散点图、线图、条形图、直方图等等。另一方面，Seaborn 提供了多种可视化模式。它使用简单的语法，并有简单有趣的默认主题。它专门研究统计可视化。

**在 Matplotlib 中创建基本剧情**

## python 3

```py
import numpy as np
import matplotlib.pyplot as plt

data = {'Cristopher': 20, 'Agara': 15, 'Jayson': 30,
        'Peter': 35}
names = list(data.keys())
age = list(data.values())

fig = plt.figure(figsize=(10, 5))

# creating the bar plot
plt.bar(names, age, color='blue', width=0.4)

plt.xlabel("Names")
plt.ylabel("Age of the person")
plt.show()
```