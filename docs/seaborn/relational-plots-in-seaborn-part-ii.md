# 海伯恩的相关地块–第二部分

> 原文:[https://www . geeksforgeeks . org/relative-plot-in-seaborn-part-ii/](https://www.geeksforgeeks.org/relational-plots-in-seaborn-part-ii/)

先决条件:[Seaborn 中的关系图–第一部分](https://www.geeksforgeeks.org/relational-plots-in-seaborn-part-i/)
在本文的[前一部分](https://www.geeksforgeeks.org/relational-plots-in-seaborn-part-i/)中，我们了解了关系图()。现在，我们将阅读另外两个关系图，即 seaborn library 中提供的散点图()和 lineplot()。这两个图也可以借助 relplot()中的 kind 参数来绘制。基本上 relplot()，默认情况下只给我们散点图()，如果我们传递参数 *kind = "line"* ，它给我们 lineplot()。

**示例 1:** 使用 relplot()可视化 tips 数据集

## 蟒蛇 3

```
import seaborn as sns
sns.set(style ="ticks")

tips = sns.load_dataset('tips')
sns.relplot(x ="total_bill", y ="tip", data = tips)
```