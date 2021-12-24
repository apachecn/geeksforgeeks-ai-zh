# Python OpenCV–cv2 . flip()方法

> 原文:[https://www . geesforgeks . org/python-opencv-cv2-flip-method/](https://www.geeksforgeeks.org/python-opencv-cv2-flip-method/)

**OpenCV-Python** 是一个主要针对实时计算机视觉的编程函数库。`cv2.flip()`方法用于翻转 2D 阵列。函数 cv::flip 围绕垂直、水平或两个轴翻转 2D 数组。

> **语法:** cv2.cv.flip(src、flipCode[、dst])
> 
> **参数:**
> **src:** 输入数组。
> **dst:** 与 src 大小和类型相同的输出数组。
> **翻转码:**指定如何翻转数组的标志；0 表示绕 x 轴翻转，正值(例如 1)表示绕 y 轴翻转。负值(例如，-1)表示绕两个轴翻转。
> 
> **返回值:**返回图像。

**图像用于以下所有示例:**
![](img/c8773af5d93591c46b33a4bf4342545d.png)

**示例:**

```
# Python program to explain cv2.flip() method

# importing cv2
import cv2

# path
path = r'C:\Users\user\Desktop\geeks14.png'

# Reading an image in default mode
src = cv2.imread(path)

# Window name in which image is displayed
window_name = 'Image'

# Using cv2.flip() method
# Use Flip code 0 to flip vertically
image = cv2.flip(src, 0)

# Displaying the image
cv2.imshow(window_name, image)
cv2.waitKey(0)
```

**输出:**

![](img/168019113f5507539969ad6e77cd37ba.png)