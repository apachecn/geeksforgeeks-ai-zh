# Python |找到 Numpy 数组列表的平均值

> 原文:[https://www . geesforgeks . org/python-find-mean-of-list-numpy-array/](https://www.geeksforgeeks.org/python-find-mean-of-a-list-of-numpy-array/)

给定一个 numpy 数组列表，任务是找到每个 Numpy 数组的平均值。让我们看看我们可以做这项任务的几种方法。

**方法#1:使用 np.mean()**

```
# Python code to find mean of every numpy array in list

# Importing module
import numpy as np

# List Initialization
Input = [np.array([1, 2, 3]),
         np.array([4, 5, 6]),
         np.array([7, 8, 9])]

# Output list initialization
Output = []

# using np.mean()
for i in range(len(Input)):
   Output.append(np.mean(Input[i]))

# Printing output
print(Output)
```

**Output:**

```
[2.0, 5.0, 8.0]

```

**方法 2:使用 np.average()**

```
# Python code to find mean of 
# every numpy array in list

# Importing module
import numpy as np

# List Initialization
Input = [np.array([11, 12, 13]),
         np.array([14, 15, 16]),
         np.array([17, 18, 19])]

# Output list initialization
Output = []

# using np.mean()
for i in range(len(Input)):
   Output.append(np.average(Input[i]))

# Printing output
print(Output)
```

**Output:**

```
[12.0, 15.0, 18.0]

```