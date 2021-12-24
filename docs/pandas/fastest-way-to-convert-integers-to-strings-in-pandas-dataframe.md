# 熊猫数据框中整数转换成字符串的最快方法

> 原文:[https://www . geeksforgeeks . org/将整数转换为字符串的最快方法-熊猫-dataframe/](https://www.geeksforgeeks.org/fastest-way-to-convert-integers-to-strings-in-pandas-dataframe/)

熊猫——任何程序员都可以使用的开源库。这是一个有用的库，用于分析数据和操作数据。它快速、灵活、易懂，可以轻松处理丢失的数据。它不仅提供了强大的数据结构，还提高了数据操作和分析工具的性能。

熊猫中有四种将整数转换成字符串的方法。

**方法 1:图谱(str)**

> 框架['数据框列']=框架['数据框列']。地图(字符串)

**方法 2:应用(str)**

> 框架['数据框列']=框架['数据框列']。应用(字符串)

**方法 3:a 型(str)**

> 框架['数据框列']=框架['数据框列']。astype(字符串)

**方法 4:values . a type(str)**

> 框架['数据框列']=框架['数据框列']。值。类型(字符串)

为了找出最快的方法，我们找到了将整数转换为字符串所需的每种方法所花费的时间。需要最短转换时间的方法被认为是最快的方法。

```
import pandas as pd
import sys
import time
import numpy as np

print('Version Of Python: ' + sys.version)
print('Version Of Pandas: ' + pd.__version__)
print('Version Of Numpy: ' + np.version.version)

frame1 = pd.DataFrame(np.random.randint(0, 90, size =(5000000, 1)), columns =['random'])
frame2 = pd.DataFrame(np.random.randint(0, 90, size =(5000000, 1)), columns =['random'])
frame3 = pd.DataFrame(np.random.randint(0, 90, size =(5000000, 1)), columns =['random'])
frame4 = pd.DataFrame(np.random.randint(0, 90, size =(5000000, 1)), columns =['random'])

# Using map(str) method
t1 = time.time()
frame1['random'] = frame1['random'].map(str)
output1 = (time.time() - t1)  
print('Time taken in seconds using map(str): ' + str(output1))

# Using apply(str) method
t2 = time.time()
frame2['random'] = frame2['random'].apply(str)
output2 = (time.time() - t2)  
print('Time taken in seconds using apply(str): ' + str(output2))

# Using astype(str) method
t3 = time.time()
frame3['random'] = frame3['random'].astype(str)
output3 = (time.time() - t3)  
print('Time taken in seconds using astype(str): ' + str(output3))

# Using values.astype(str) method
t4 = time.time()
frame4['random'] = frame4['random'].values.astype(str)
output4 = (time.time() - t4)  
print('Time taken in seconds using values.astype(str): ' + str(output4))

l =[output1, output2, output3, output4]
m =['map(str)', 'apply(str)', 'astype(str)', 'values.astype(str)']

# Fastest way to convert into string
minimum = min(l)
k = l.index(minimum)
fastest = m[k]

# It will print the fastest conversion method.
print(fastest+" is the fastest method")
```

**输出:**

![pandas-into-to-string-fastest](img/6c705fb540aa686f8496f925db91475f.png)