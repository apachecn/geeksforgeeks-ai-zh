# 如何逆序获取 NumPy 多维数组的索引？

> 原文:[https://www . geeksforgeeks . org/如何逆序获取 numpy 多维数组索引/](https://www.geeksforgeeks.org/how-to-get-index-of-numpy-multidimensional-array-in-reverse-order/)

在本文中，我们将看到如何以相反的顺序获取 NumPy 多维数组的索引。

**接近**

*   首先，我们导入 NumPy 库，并初始化必要的参数，包括我们需要处理的矩阵和其他所需的参数。
*   现在，我们将循环每一行，翻转它，并在每一行中以相反的顺序找到所需元素的索引，并将其存储在我们创建的列表(结果)中。
*   现在，我们从数组中的行的反面获取所有索引。我们现在需要将适合读取的索引从左向右转换，因此，我们用每个索引减去行的长度，并进一步减少 1，以获得适合零索引的数组。

> 最终索引=行中的元素总数-当前索引-1

示例:

> **输入:**
> 
> [[1,2,3,4,2],
> 
> [2,3,4,1,5],
> 
> [2,2,4,3,2],
> 
> [1,3,4,2,4]]
> 
> **输出:**
> 
> [4 0 4 3]
> 
> **解释:**在上面的例子中，我们试图以相反的顺序找到‘2’的第一次出现索引，我们每行有 5 个元素，在反向索引之后，我们得到了像[0，4，0，1]这样的数组，现在使用我们上面的公式。
> 
> final_list[0] = >行中的总元素–当前索引- 1 => 5-0-1 =>4
> 
> final_list[1] = >行中的总元素–当前索引- 1 => 5-4-1 =>0
> 
> final_list[2] = >行中的总元素–当前索引- 1 => 5-0-1 =>4
> 
> final_list[3] = >行中的总元素–当前索引- 1 => 5-1-1 =>3

**例 1:**

## 蟒蛇 3

```py
#import Modules
import numpy as np

# initialize parameters
x = np.array([[1, 2, 3, 4, 2],
              [2, 3, 4, 1, 5],
              [2, 2, 4, 3, 2],
              [1, 3, 4, 2, 4]])  
num_cols = len(x[0])  
result = []  

# loop over each row
for row in x:  
    row = np.flip(row)  
    index = np.where(row == 2)  
    result.append(index[0][0])  

# get the final indexes
# Store the result as of the initial arrays
final_list = num_cols-np.array(result)-1

# print
print(final_list)  
```

**输出:**

> [4 0 4 3]

**例 2:**

上述方法同样适用于字符串。在下面的示例中，我们试图以相反的顺序找到“Sam”的第一个出现索引。

## 蟒蛇 3

```py
#import Modules
import numpy as np

# initialize parameters
x = np.array([["Sam", "John", "Lilly"],
              ["Sam", "Sam", "Kate"],
              ["Jack", "John", "Sam"],
              ["Sam", "Jack", "Rose"]]) 
num_cols = len(x[0]) 
result = [] 

# loop over each row
for row in x: 
    row = np.flip(row)  
    index = np.where(row == "Sam")  
    result.append(index[0][0]) 

# get the final indexes
# Store the result as of the initial arrays
final_list = num_cols-np.array(result)-1

# print
print(final_list)  
```

**输出:**

> [0 1 2 ]

**例 3:**

对于布尔数据，我们有相同的方法，但是由于它只有 0 或 1 作为值，我们可以使用 [argmax()](https://www.geeksforgeeks.org/numpy-argmax-python/) 来找到最高值的索引(对于轴=1 的每一行)。因为真等于 1，假等于 0，所以它会记录第一个真值的索引。

## 蟒蛇 3

```py
# import Modules
import numpy as np

# initialize parameters
a = np.array([[True, False, True, True],
              [False, False, True, False],
              [False, True, True, True],
              [True, False, False, True]])

reversed_array = a[:, ::-1]
max_val = np.argmax(reversed_array, axis=1)
num_rows = a.shape[1]  
final_list = num_rows-1-max_val  

print(final_list)  
```

**输出:**

> [3 2 3 3]