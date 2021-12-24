# 如何将 NumPy 数组保存为文本文件？

> 原文:[https://www . geeksforgeeks . org/如何将 numpy 数组保存为文本文件/](https://www.geeksforgeeks.org/how-to-save-a-numpy-array-to-a-text-file/)

让我们看看如何将 numpy 数组保存到文本文件中。

**方法 1:** 使用[文件处理](https://www.geeksforgeeks.org/file-handling-python/)
使用内置的 open()函数创建文本文件，然后将数组转换为字符串，并使用 write()函数将其写入文本文件。最后使用 close()函数关闭文件。以下是这种方法的一些程序:

*   **例 1:**

## 蟒蛇 3

```py
# Program to save a NumPy array to a text file

# Importing required libraries
import numpy

# Creating an array
List = [1, 2, 3, 4, 5]
Array = numpy.array(List)

# Displaying the array
print('Array:\n', Array)
file = open("file1.txt", "w+")

# Saving the array in a text file
content = str(Array)
file.write(content)
file.close()

# Displaying the contents of the text file
file = open("file1.txt", "r")
content = file.read()

print("\nContent in file1.txt:\n", content)
file.close()
```