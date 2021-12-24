# 如何用熊猫读取 JSON 文件？

> 原文:[https://www . geesforgeks . org/how-read-JSON-files-with-pandas/](https://www.geeksforgeeks.org/how-to-read-json-files-with-pandas/)

在本文中，我们将看到如何用熊猫读取 JSON 文件。

## 使用熊猫读取 JSON 文件

要读取文件，我们使用 **read_json()** 函数，并通过它传递我们想要读取的 json 文件的路径。一旦我们这样做了，它就会返回一个存储数据的“数据框架”(一个行和列的表)。如果我们想读取一个位于远程服务器上的文件，那么我们将链接传递到它的位置，而不是本地路径。

### **示例 1:读取 JSON 文件**

## 蟒蛇 3

```py
import pandas as pd

df = pd.read_json("FILE_JSON.json")
df.head()
```

**输出:**

```py
   One  Two
0   60  110
1   60  117
2   60  103
3   45  109
4   45  117
5   60  102
```

### 示例 2:创建 JSON 数据并读入数据帧

这里我们将创建 JSON 数据，然后使用 [**pd 通过它创建一个数据框架。Dataframe()方法。**T3】](https://www.geeksforgeeks.org/python-pandas-dataframe/)

## 蟒蛇 3

```py
import pandas as pd

data = {
    "One": {
        "0": 60,
        "1": 60,
        "2": 60,
        "3": 45,
        "4": 45,
        "5": 60
    },
    "Two": {
        "0": 110,
        "1": 117,
        "2": 103,
        "3": 109,
        "4": 117,
        "5": 102
    }
}

df = pd.DataFrame(data)

print(df)
```

**输出:**

```py
   One  Two
0   60  110
1   60  117
2   60  103
3   45  109
4   45  117
5   60  102
```