# 如何用摩丁一行变加速熊猫？

> 原文:[https://www . geeksforgeeks . org/如何加速-熊猫一行一换-使用-modin/](https://www.geeksforgeeks.org/how-to-speedup-pandas-with-with-one-line-change-using-modin/)

在这篇文章中，我们将看到如何使用 modin 库来提高熊猫的计算速度。Modin 是一个与 pandas 非常相似的 python 库(在语法方面几乎完全相同)，能够处理一个无法一次性装入 RAM 的巨大数据集。熊猫在 MB 和几 GB 大小的数据集的执行速度方面已经足够好了，但是当我们处理非常大的数据集时，处理数据的速度成为瓶颈。

熊猫库是为单核工作而设计的，因此随着现代计算能力的发展，每台个人笔记本电脑现在都至少有 2 个内核，Modin 正好利用了这个机会，在所有可用的内核上执行操作，从而加快了整个过程。

**要安装 Modin 及其所有依赖项，请使用以下任何 pip 命令。**

```py
pip install modin[ray] 
```

或者，

```py
pip install modin[dask] 
```

或者，

```py
pip install modin[all] 
```

**为了限制要使用的 CPU 数量，我们可以在您的脚本中添加下面两行代码**

```py
import os

# this specifies the number of
# CPUs to use. 
os.environ["MODIN_CPUS"] = "2"
```

**示例 1:数据帧追加操作:**

Append()操作在 pandas 中非常常见，在下面的代码中，我们使用 pandas 和 Modin 运行了 10 次，并对其进行了计时，以查看加速差异。显然，莫迪打败了熊猫，因为它使用了我的系统上所有可用的内核。还用时间模块测量运算速度互相比较，原来**摩丁在这种情况下比熊猫**快 25 倍。

**代码:**

## 蟒蛇 3

```py
import pandas as pd
import modin.pandas as mpd
import time

start = time.time()

# Creating a Custom Dataframe
data = {'Name': ['Tom', 'nick', 'krish', 'jack',
                 'ash', 'singh', 'shilpa', 'nav'],

        'Age': [20, 21, 19, 18, 6, 12, 18, 20]}

df = pd.DataFrame(data)

# Appending the dataframe to itself 10 times.
for _ in range(10):
    df = df.append(df)

end = time.time()
print(f"Pandas Appending Time :{end-start}")

start = time.time()
modin_df = mpd.DataFrame(data)

# Appending the dataframe to itself 10 times.
for _ in range(10):
    modin_df = modin_df.append(modin_df)

end = time.time()
print(f"Modin Appending Time :{end-start}")
```

**输出**:

```py
Pandas Appending Time :0.682852745056152
Modin Appending Time :0.027661800384521484
```

**例 2:摩丁比熊猫快 4.4 倍。**

这里我们使用的是 602 MB 大小的 CSV 文件，可以从这个[链接](https://www.kaggle.com/skihikingkevin/csgo-matchmaking-damage)下载。还将文件重命名为 demo.csv 以保持简短。在下面的代码中，我们使用了 fillna()方法，该方法遍历整个 DataFrame 并用所需的值填充所有 NaN 值，在我的示例中为 0。

**代码:**

## 蟒蛇 3

```py
import pandas as pd
import modin.pandas as mpd

# Reading demo.csv file into pandas df
df = pd.read_csv("demo.csv")

s = time.time()
df = df.fillna(value=0)

e = time.time()
print(f"Pandas fillna Time: {e-s})

# Reading demo.csv file into modin df
modin_df = mpd.read_csv("demo.csv")
s = time.time()

modin_df = modin_df.fillna(value=0)
e = time.time()
print(f"Modin fillna Time: {e - s})
```

**输出**:

```py
Pandas fillna Time: 1.2 sec
Modin fillna Time: 0.27 sec
```