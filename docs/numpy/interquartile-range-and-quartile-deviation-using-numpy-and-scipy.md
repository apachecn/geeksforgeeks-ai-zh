# 使用 NumPy 和 SciPy 的四分位数范围和四分位数偏差

> 原文:[https://www . geesforgeks . org/inter-quartle-range-and-quartle-variance-using-numpy-and-scipy/](https://www.geeksforgeeks.org/interquartile-range-and-quartile-deviation-using-numpy-and-scipy/)

**四分位数:**
四分位数是分位数的一种。**第一个四分位数(Q1)** ，定义为数据集最小数和中值之间的中间数，给定数据集的**第二个四分位数(Q2)**–**中值**，而**第三个四分位数(Q3)** ，是数据集中值和最大值之间的中间数。

**求四分位数的算法:**
四分位数是借助中位数计算的。如果条目数是偶数，即 2n 形式，则第一个四分位数(Q1)等于最小条目 **n** 的中间值，第三个四分位数(Q3)等于最大条目 **n** 的中间值。

如果条目的数量是奇数，即形式为(2n + 1)，那么

*   第一个四分位数(Q1)等于最小条目的中间值
*   第三个四分位数(Q3)等于 **n** 个最大条目的中间值
*   第二个四分位数(Q2)与普通中位数相同。

**范围:**是给定数据集中最大值和最小值的差值。
**四分位数区间:**
四分位数区间(IQR)，也称为**中间延伸或中间 50%** ，或技术上的 H-spread 是第三个四分位数(Q3)和第一个四分位数(Q1)的差值。它覆盖了分布的中心，包含了 50%的观测值。**IQR = Q3–Q1**

**用途:**

*   四分位数区间的细分点为 25%，因此通常比总区间更受青睐。
*   IQR 用于构建箱线图，概率分布的简单图形表示。
*   IQR 也可以用来识别给定数据集中的异常值。
*   IQR 给出了数据的中心趋势。

**决策**

*   数据集具有更高的四分位数范围值(IQR)具有更大的可变性。
*   具有较低值的四分位数范围(IQR)的数据集是优选的。

假设我们有两个数据集，它们的四分位数范围是 IR1 和 IR2，如果 IR1 > IR2，那么据说 IR1 中的数据比 IR2 中的数据更具可变性，IR2 中的数据更可取。

**示例:**

*   以下是过去 20 天每天报名参加本课程的考生人数–
    数据结构&算法- [DSA Online 3](https://practice.geeksforgeeks.org/courses/dsa-online-2?utm_source=mautic&utm_medium=email&utm_campaign=DSA3_email) 在 GeeksforGeeks:
    75、69、56、46、47、79、92、97、89、88、36、96、105、32、116、101、79、93、91、112
*   对以上数据集进行排序后:
    32、36、46、47、56、69、75、79、79、88、89、91、92、93、96、97、101、105、112、116
*   这里术语的总数是 20。
*   上述数据的第二个四分位数(Q2)或中位数为(88 + 89) / 2 = 88.5
*   第一个四分位数(Q1)是前 n 个即 10 个项(或 n 个即 10 个最小值)= 62.5 的中值
*   第三个四分位数(Q3)是 n(即 10 个最大值)或最后 n(即 10 个值)的中位数= 96.5
*   那么，IQR = Q3–Q1 = 96.5–62.5 = 34.0

**使用数值中位数的四分位数范围**

```
# Import the numpy library as np
import numpy as np

data = [32, 36, 46, 47, 56, 69, 75, 79, 79, 88, 89, 91, 92, 93, 96, 97, 
        101, 105, 112, 116]

# First quartile (Q1)
Q1 = np.median(data[:10])

# Third quartile (Q3)
Q3 = np.median(data[10:])

# Interquartile range (IQR)
IQR = Q3 - Q1

print(IQR)
```

```
Output: 34.0
```

**使用数值百分位的四分位数范围**

```
# Import numpy library
import numpy as np

data = [32, 36, 46, 47, 56, 69, 75, 79, 79, 88, 89, 91, 92, 93, 96, 97, 
        101, 105, 112, 116]

# First quartile (Q1)
Q1 = np.percentile(data, 25, interpolation = 'midpoint')

# Third quartile (Q3)
Q3 = np.percentile(data, 75, interpolation = 'midpoint')

# Interquaritle range (IQR)
IQR = Q3 - Q1

print(IQR)
```

```
Output: 34.0
```

**使用 scipy.stats.iqr 的四分位数范围**

```
# Import stats from scipy library
from scipy import stats

data = [32, 36, 46, 47, 56, 69, 75, 79, 79, 88, 89, 91, 92, 93, 96, 97, 
        101, 105, 112, 116]

# Interquartile range (IQR)
IQR = stats.iqr(data, interpolation = 'midpoint')

print(IQR)
```

```
Output: 34.0
```

**四分位数偏差**
四分位数偏差是第三个四分位数(Q3)和第一个四分位数(Q1)之差的一半，即四分位数区间(IQR)的一半。**(Q3–Q1)/2 = IQR/2**

**决策**
四分位数离差值较高的数据集具有较高的变异性。

**使用数值中位数的四分位数偏差**

```
# import the numpy library as np
import numpy as np

data = [32, 36, 46, 47, 56, 69, 75, 79, 79, 88, 89, 91, 92, 93, 96, 97, 
        101, 105, 112, 116]

# First quartile (Q1)
Q1 = np.median(data[:10])

# Third quartile (Q3)
Q3 = np.median(data[10:])

# Interquartile range (IQR)
IQR = Q3 - Q1

# Quartile Deviation
qd = IQR / 2

print(qd)      
```

```
Output: 17.0
```