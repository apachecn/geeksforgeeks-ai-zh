# ML |原始和中心时刻

> 原文:[https://www.geeksforgeeks.org/ml-raw-and-central-moments/](https://www.geeksforgeeks.org/ml-raw-and-central-moments/)

**矩**是一组统计参数，用于描述频率分布的不同特征和特性，即频率曲线的中心趋势、色散、对称性和峰值(驼峰)。

对于*未分组数据*即离散数据，变量 X 的观测值作为![x_1, x_2, x_3, ...., x_n](img/83e60de86ff59e29912de39359afbdbe.png "Rendered by QuickLaTeX.com")获得，对于*分组数据*即连续数据，变量 X 的观测值作为频率表中的 K 类区间获得并列表。区间的中点由![x_1, x_2, x_3, ...., x_n](img/83e60de86ff59e29912de39359afbdbe.png "Rendered by QuickLaTeX.com")表示，它们分别以频率![f_1, f_2, f_3, ...., f_n](img/287d68ec8f289fb69973ebceb93c7b61.png "Rendered by QuickLaTeX.com")和![n=f_1, f_2, f_3, ...., f_n](img/7425bfbccd870ac98ad34d37ba9bf61d.png "Rendered by QuickLaTeX.com")出现。

| 班级间隔 | 中点(![x_i](img/8ac565c17d653ce28930ec7ba781fe6f.png "Rendered by QuickLaTeX.com")) | 绝对频率(![f_i](img/9998cf27e46043123bf986d15d935dae.png "Rendered by QuickLaTeX.com")) |
| --- | --- | --- |
| ![c_1 - c_2](img/bfa58ec863359f712b2654a084c736ba.png "Rendered by QuickLaTeX.com") | ![x_1 = (c_1 + c_2)/2](img/1c80feb79b0c05776601b6931ca6f423.png "Rendered by QuickLaTeX.com") | ![f_1](img/ea5909d7b0a42b32e115d9b4b16e571c.png "Rendered by QuickLaTeX.com") |
| ![c_2 - c_3](img/92296873b1d0ab26b53fa5828f12ac72.png "Rendered by QuickLaTeX.com") | ![x_2 = (c_2 + c_3)/2](img/6c3ae1b964c572beebd1d66fe00b681b.png "Rendered by QuickLaTeX.com") | ![f_2](img/0530f61ef82a6b31df8a7d68684eb5a7.png "Rendered by QuickLaTeX.com") |
| ![c_3 - c_4](img/4622f1af5233dd8e4570df77b902684c.png "Rendered by QuickLaTeX.com") | ![x_3 = (c_3 + c_4)/2](img/753ff4d7c215b9689c430c5cbf98157a.png "Rendered by QuickLaTeX.com") | ![f_3](img/c40f3210ca97516fd0bc8f913883bf51.png "Rendered by QuickLaTeX.com") |
| … | … | … |
| … | … | … |
| ![c_k_-_1 - c_k](img/8654a9be15528dc8ebc17b7682dc6181.png "Rendered by QuickLaTeX.com") | ![x_k = (c_k_-_1 + c_k)/2](img/26247f8cc29e6d7b711399d892b11fe9.png "Rendered by QuickLaTeX.com") | ![f_k](img/2d612028a21d985bc85ea5d42ba62f5b.png "Rendered by QuickLaTeX.com") |

**关于任意点 A 的力矩**
关于观测值上任意点 A 的变量 X 的![r^t^h](img/e33aaac65415e15b94bc5159f3c76cf6.png "Rendered by QuickLaTeX.com")力矩![x_1, x_2, x_3, ...., x_n](img/83e60de86ff59e29912de39359afbdbe.png "Rendered by QuickLaTeX.com")定义为:

> **对于未分组的数据** ![ \mu^'_r = \frac{1}{n}\sum_{i=1}^{n}(x_i - A)^r ](img/02a918a14c3a8f5e3e23fba9766bea31.png "Rendered by QuickLaTeX.com")
> 
> **分组数据** ![ \mu^'_r = \frac{1}{n}\sum_{i=1}^{n}f_i(x_i - A)^r ](img/cd762809df75a8c4f76af7f292c8c667.png "Rendered by QuickLaTeX.com")
> 
> 其中
> ![ n = \sum_{i=1}^{k}f_i](img/7bd3df3be61c0bd0ed887fd11972f886.png "Rendered by QuickLaTeX.com")

**关于 Python 中任意点的时刻–**

考虑给定的数据点。以下是 20 个不同的人每周在极客博客门户网站上花费的时间(以小时为单位)。

```
15, 25, 18, 36, 40, 28, 30, 32, 23, 22, 21, 27, 31, 20, 14, 10, 33, 11, 7, 13
```

```
# data points
time = [15, 25, 18, 36, 40, 28, 30, 32, 23, 22, 
        21, 27, 31, 20, 14, 10, 33, 11, 7, 13]

# Arbitrary point 
A = 22

# Moment for r = 1
moment = (sum([(item-A) for item in time]))/len(time)
```

## 原始时刻–

原点 A = 0 周围的![r^t^h](img/e33aaac65415e15b94bc5159f3c76cf6.png "Rendered by QuickLaTeX.com")力矩称为原始力矩，定义为:

> 对于未分组的数据，![\mu^'_r = \frac{1}{n}\sum_{i=1}^{n}x_i^r ](img/6c61f0fa2a2292f2cf65a84d49f4a52d.png "Rendered by QuickLaTeX.com")
> 对于分组的数据，![ \mu^'_r = \frac{1}{n}\sum_{i=1}^{n}f_i x_i^r ](img/21a943fd4f250f56dcd7a9aa7d6fd19f.png "Rendered by QuickLaTeX.com")
> 
> 其中，![n = \sum_{i=1}^{k}f_i](img/3e5a667eca9fac1f0fa79f6414a2e2f7.png "Rendered by QuickLaTeX.com")

**备注:**

> **- >** 我们可以通过用 1 替换 r 来找到第一个原始时刻(![\mu^'_1](img/0d63e9f4a20e0bc044f9dde9b24385cb.png "Rendered by QuickLaTeX.com"))，通过用 2 替换 r 来找到第二个原始时刻(![\mu^'_2](img/1f755b637b2ec8f169e2a3eb97a9582d.png "Rendered by QuickLaTeX.com"))以此类推。
> **- >** 当 r = 0 时，分组和非分组数据的时刻![\mu^'_0 = 1](img/391d4e2d063045a4ae8516463b67c0e3.png "Rendered by QuickLaTeX.com")。

**Python 中的原始时刻–**

```
# data points
time = [15, 25, 18, 36, 40, 28, 30, 32, 23,
       22, 21, 27, 31, 20, 14, 10, 33, 11, 7, 13]

# Moment for r = 1
moment = sum(time)/len(time)
```

## 中心时刻–

变量 X 关于算术平均值(![\overline{x}](img/649ae0f2e2132baae2c163de2f4f1fae.png "Rendered by QuickLaTeX.com"))的矩称为中心矩，定义为:

> 对于未分组的数据，![\mu_r = \frac{1}{n}\sum_{i=1}^{n}(x_i-\overline{x})^r ](img/61d5da5e9374ba7843ce7e13e9f4bdbe.png "Rendered by QuickLaTeX.com")
> 
> 对于分组数据，![\mu_r = \frac{1}{n}\sum_{i=1}^{n}f_i (x_i-\overline{x})^r ](img/015d11ba28833526d92e5899875448f2.png "Rendered by QuickLaTeX.com")
> 
> 其中![n = \sum_{i=1}^{k}f_i ](img/8eed141cdede295b26bd56933865457f.png "Rendered by QuickLaTeX.com")和![ \overline{x} = \sum_{i=1}^{k}f_ix_i ](img/11bacf037875583c5189298d115e6de1.png "Rendered by QuickLaTeX.com")

**备注:**

> **- >** 我们用 1 代替 r 就可以找到第一个原始矩(![\mu_1](img/ff897729479644ae3d7509319cde01da.png "Rendered by QuickLaTeX.com"))，用 2 代替 r 就可以找到第二个原始矩(![\mu_2](img/bd9f0bd95fc90a90a59835dd6f0e59a6.png "Rendered by QuickLaTeX.com"))以此类推。
> **- >** 当 r = 0 时的时刻![\mu_0 = 1](img/aae8a1a445c63ae79b1702c288cbe5c5.png "Rendered by QuickLaTeX.com")，以及当 r = 1 时的时刻![\mu_1 = 0](img/a92d745a19560d1895415b36f76719e6.png "Rendered by QuickLaTeX.com")对于分组和未分组的数据。

```
# data points
time = [15, 25, 18, 36, 40, 28, 30, 32, 23, 22,
       21, 27, 31, 20, 14, 10, 33, 11, 7, 13]

# Mean 
A = sum(time)/len(time)

# Moment for r = 1
moment = (sum([(item-A) for item in time]))/len(time)
```

**原始时刻和中心时刻之间的关系–**
![](img/739d787e7be26e62795ee44c776f4d51.png)