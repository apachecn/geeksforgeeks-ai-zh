# Python OpenCV–cv2 .转置()方法

> 原文:[https://www . geesforgeks . org/python-opencv-cv2-转置-method/](https://www.geeksforgeeks.org/python-opencv-cv2-transpose-method/)

**[OpenCV](https://www.geeksforgeeks.org/opencv-python-tutorial/)** 是一个主要针对实时计算机视觉的编程函数库。`cv2.transpose()`方法用于转置 2D 阵列。函数 cv::转置将图像逆时针旋转 90 度。

> **语法:** cv2.cv .转置(src[，dst])
> 
> **参数:**
> **src:** 是矩阵要转置的图像。
> **dst:** 是与 src 图像大小和深度相同的输出图像。这是一个可选参数。
> 
> **返回值:**返回图像。

**图像用于以下所有示例:**
![](img/c8773af5d93591c46b33a4bf4342545d.png)

**示例:**

```py
# Python program to explain cv2.transpose() method

# importing cv2
import cv2

# path
path = r'C:\Users\user\Desktop\geeks14.png'

# Reading an image in default mode
src = cv2.imread(path)

# Window name in which image is displayed
window_name = 'Image'

# Using cv2.transpose() method
image = cv2.transpose(src)

# Displaying the image
cv2.imshow(window_name, image)
cv2.waitKey(0)
```

**输出:**

![](img/37bfdc004186a4b85b1a69c6f7d56f1f.png)