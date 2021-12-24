# Python OpenCV | cv2.rectangle()方法

> 原文:[https://www . geesforgeks . org/python-opencv-cv2-rectangle-method/](https://www.geeksforgeeks.org/python-opencv-cv2-rectangle-method/)

**OpenCV-Python** 是一个 Python 绑定库，旨在解决计算机视觉问题。`cv2.rectangle()`方法用于在任意图像上绘制矩形。

> **语法:** cv2 .矩形(图像、起点、终点、颜色、厚度)
> 
> **参数:**
> **图像:**就是要画矩形的图像。
> **起点:**是矩形的起始坐标。坐标表示为两个值的元组(即 **X** 坐标值、 **Y** 坐标值)。
> **end_point:** 是矩形的结束坐标。坐标表示为两个值的元组(即 **X** 坐标值， **Y** 坐标值)。
> **颜色:**是待画矩形边框线的颜色。对于 **BGR** ，我们传递一个元组。例如:(255，0，0)代表蓝色。
> **厚度:**是 **px** 中矩形边框线的厚度。 **-1 px** 的厚度会以指定的颜色填充矩形。
> 
> **返回值:**返回图像。

**图像用于以下所有示例:**
![](img/c8773af5d93591c46b33a4bf4342545d.png)

**示例#1:**

```py
# Python program to explain cv2.rectangle() method 

# importing cv2 
import cv2 

# path 
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks\geeks.png'

# Reading an image in default mode
image = cv2.imread(path)

# Window name in which image is displayed
window_name = 'Image'

# Start coordinate, here (5, 5)
# represents the top left corner of rectangle
start_point = (5, 5)

# Ending coordinate, here (220, 220)
# represents the bottom right corner of rectangle
end_point = (220, 220)

# Blue color in BGR
color = (255, 0, 0)

# Line thickness of 2 px
thickness = 2

# Using cv2.rectangle() method
# Draw a rectangle with blue line borders of thickness of 2 px
image = cv2.rectangle(image, start_point, end_point, color, thickness)

# Displaying the image 
cv2.imshow(window_name, image) 
```

**输出:**
![](img/ad6ce58ad89b4f413684e1a057007596.png)

**例 2:**

使用-1 像素的厚度用黑色填充矩形。

```py
# Python program to explain cv2.rectangle() method 

# importing cv2 
import cv2 

# path 
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks\geeks.png'

# Reading an image in grayscale mode
image = cv2.imread(path, 0)

# Window name in which image is displayed
window_name = 'Image'

# Start coordinate, here (100, 50)
# represents the top left corner of rectangle
start_point = (100, 50)

# Ending coordinate, here (125, 80)
# represents the bottom right corner of rectangle
end_point = (125, 80)

# Black color in BGR
color = (0, 0, 0)

# Line thickness of -1 px
# Thickness of -1 will fill the entire shape
thickness = -1

# Using cv2.rectangle() method
# Draw a rectangle of black color of thickness -1 px
image = cv2.rectangle(image, start_point, end_point, color, thickness)

# Displaying the image 
cv2.imshow(window_name, image) 
```

**输出:**
![](img/61ca26098f3257c2c354e0399b31c901.png)