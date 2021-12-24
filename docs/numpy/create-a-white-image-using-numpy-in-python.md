# 使用 Python 中的 NumPy 创建白色图像

> 原文:[https://www . geeksforgeeks . org/create-a-white-image-using-numpy-in-python/](https://www.geeksforgeeks.org/create-a-white-image-using-numpy-in-python/)

让我们看看如何使用 NumPy 和 cv2 创建一个白色图像。白色图像的所有像素都是 255。

**方法 1:** 使用 [np.full()](https://www.geeksforgeeks.org/numpy-full-python/#:~:text=full(shape%2C%20fill_value%2C%20dtype,Data%20type%20of%20returned%20array.) 方法:

## 蟒蛇 3

```py
# importing the libraries
import cv2
import numpy as np

# creating an array using np.full 
# 255 is code for white color
array_created = np.full((500, 500, 3),
                        255, dtype = np.uint8)

# displaying the image
cv2.imshow("image", array_created)
```