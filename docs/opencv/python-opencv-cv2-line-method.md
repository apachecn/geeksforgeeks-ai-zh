# Python OpenCV | cv2.line()方法

> 原文:[https://www . geesforgeks . org/python-opencv-cv2-line-method/](https://www.geeksforgeeks.org/python-opencv-cv2-line-method/)

**OpenCV-Python** 是一个 Python 绑定库，旨在解决计算机视觉问题。`cv2.line()`方法用于在任意图像上画线。

> **语法:** cv2.line(图像、起点、终点、颜色、厚度)
> 
> **参数:**
> **图像:**就是要画线的图像。
> **起点:**是直线的起始坐标。坐标表示为两个值的元组(即 **X** 坐标值、 **Y** 坐标值)。
> **终点:**是直线的终点坐标。坐标表示为两个值的元组(即 **X** 坐标值， **Y** 坐标值)。
> **颜色:**是要画的线的颜色。对于 **BGR** ，我们传递一个元组。例如:(255，0，0)代表蓝色。
> **厚度:**是 **px** 中线条的厚度。
> 
> **返回值:**返回图像。

**图像用于以下所有示例:**
![](img/c8773af5d93591c46b33a4bf4342545d.png)

**示例#1:**

```
# Python program to explain cv2.line() method 

# importing cv2 
import cv2 

# path 
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks\geeks.png'

# Reading an image in default mode
image = cv2.imread(path)

# Window name in which image is displayed
window_name = 'Image'

# Start coordinate, here (0, 0)
# represents the top left corner of image
start_point = (0, 0)

# End coordinate, here (250, 250)
# represents the bottom right corner of image
end_point = (250, 250)

# Green color in BGR
color = (0, 255, 0)

# Line thickness of 9 px
thickness = 9

# Using cv2.line() method
# Draw a diagonal green line with thickness of 9 px
image = cv2.line(image, start_point, end_point, color, thickness)

# Displaying the image 
cv2.imshow(window_name, image) 
```

**输出:**
![](img/18f753493319dc30e9283624c800dd92.png)

**例 2:**

```
# Python program to explain cv2.line() method 

# importing cv2 
import cv2 

# path 
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks\geeks.png'

# Reading an image in grayscale mode
image = cv2.imread(path, 0)

# Window name in which image is displayed
window_name = 'Image'

# Start coordinate, here (225, 0)
# represents the top right corner of image
start_point = (225, 0)

# End coordinate, here (0, 225)
# represents the bottom left corner of image
end_point = (0, 225)

# Black color in BGR
color = (0, 0, 0)

# Line thickness of 5 px
thickness = 5

# Using cv2.line() method
# Draw a diagonal black line with thickness of 5 px
image = cv2.line(image, start_point, end_point, color, thickness)

# Displaying the image 
cv2.imshow(window_name, image) 
```

**输出:**
![](img/2420ae246afae0a888bfd734f028b42f.png)