# python | pandas time delta index . transponte()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫-时间增量索引应答/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

Pandas **TimedeltaIndex .转置()**函数返回给定 TimedeltaIndex 对象的转置，根据定义，该对象是自身。

> **语法:** TimedeltaIndex .转置(*args，**kwargs)
> **参数:** *args，**kwargs
> **返回:**同类型对象

**示例#1:** 使用 TimedeltaIndex.transpose()函数查找给定 TimedeltaIndex 对象的转置。

## 蟒蛇 3

```py
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(data =['06:05:01.000030', '+23:59:59.999999',
                        '22 day 2 min 3us 10ns', '+23:29:59.999999',
                        '+12:19:59.999999'])

# Print the TimedeltaIndex object
print(tidx)
```

**输出:**

![](img/708240dfe9aedf867ac5c12c98b02393.png)

现在我们将使用 TimedeltaIndex .转置()函数来查找 tidx 对象的转置。

## 蟒蛇 3

```py
# find transpose
tidx.transpose()
```

**输出:**

![](img/708240dfe9aedf867ac5c12c98b02393.png)

正如我们在输出中看到的，TimedeltaIndex .转置()函数返回了 tidx 对象的转置，根据定义，该对象是自身。

**示例#2:** 使用 TimedeltaIndex .转置()函数查找给定 TimedeltaIndex 对象的转置。

## 蟒蛇 3

```py
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(start ='1 days 02:00:12.001124',
                        periods = 5, freq ='D', name ='Koala')

# Print the TimedeltaIndex object
print(tidx)
```

**输出:**

![](img/4b1498214e3c6e8c3ca75b1dc780223c.png)

现在我们将使用 TimedeltaIndex .转置()函数来查找 tidx 对象的转置。

## 蟒蛇 3

```py
# find transpose
tidx.transpose()
```

**输出:**

![](img/4b1498214e3c6e8c3ca75b1dc780223c.png)

正如我们在输出中看到的，TimedeltaIndex .转置()函数返回了 tidx 对象的转置，根据定义，该对象是自身。