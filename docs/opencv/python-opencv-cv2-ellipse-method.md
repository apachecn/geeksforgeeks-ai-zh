# Python OpenCV | cv2.ellipse()方法

> 原文:[https://www . geesforgeks . org/python-opencv-cv2-ellipse-method/](https://www.geeksforgeeks.org/python-opencv-cv2-ellipse-method/)

**OpenCV-Python** 是一个 Python 绑定库，旨在解决计算机视觉问题。`cv2.ellipse()`方法用于在任意图像上绘制椭圆。

> **语法:** cv2 .椭圆(图像、中心坐标、轴长度、角度、起始角度、角度、颜色[、厚度[、线型[、偏移]])
> 
> **参数:**
> **图像:**就是要画椭圆的图像。
> **中心坐标:**是椭圆的中心坐标。坐标表示为两个值的元组(即 **X** 坐标值、 **Y** 坐标值)。
> **axesLength:** 它包含包含椭圆长轴和短轴(长轴长度、短轴长度)的两个变量的元组。
> **角度:**椭圆旋转角度，单位为度。
> **起始角度:**椭圆弧的起始角度，单位为度。
> **endAngle:** 椭圆弧的终止角，单位为度。
> **颜色:**是要绘制的形状的边框线的颜色。对于 **BGR** ，我们传递一个元组。例如:(255，0，0)代表蓝色。
> **厚度:**是 **px** 中形状边框线的厚度。 **-1 px** 的厚度会以指定的颜色填充形状。
> **线型:**这是可选参数。它给出了椭圆边界的类型。
> **换挡:**这是可选参数。它表示中心坐标中的小数位数和轴的值。
> 
> **返回值:**返回图像。

**图像用于以下所有示例:**
![](img/c8773af5d93591c46b33a4bf4342545d.png)

**示例#1:**

```py
# Python program to explain cv2.ellipse() method 

# importing cv2 
import cv2 

# path 
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks\geeks.png'

# Reading an image in default mode
image = cv2.imread(path)

# Window name in which image is displayed
window_name = 'Image'

center_coordinates = (120, 100)

axesLength = (100, 50)

angle = 0

startAngle = 0

endAngle = 360

# Red color in BGR
color = (0, 0, 255)

# Line thickness of 5 px
thickness = 5

# Using cv2.ellipse() method
# Draw a ellipse with red line borders of thickness of 5 px
image = cv2.ellipse(image, center_coordinates, axesLength,
           angle, startAngle, endAngle, color, thickness)

# Displaying the image 
cv2.imshow(window_name, image) 
```

**输出:**
![](img/973b146c0dcf2cf91f57af07ff21d5ed.png)

**示例#2:**
使用-1 px 的厚度和 30 度的旋转。

```py
# Python program to explain cv2.ellipse() method

# importing cv2
import cv2

# path
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks\geeks.png'

# Reading an image in default mode
image = cv2.imread(path)

# Window name in which image is displayed
window_name = 'Image'

center_coordinates = (120, 100)

axesLength = (100, 50)

angle = 30

startAngle = 0

endAngle = 360

# Blue color in BGR
color = (255, 0, 0)

# Line thickness of -1 px
thickness = -1

# Using cv2.ellipse() method
# Draw a ellipse with blue line borders of thickness of -1 px
image = cv2.ellipse(image, center_coordinates, axesLength, angle,
                          startAngle, endAngle, color, thickness)

# Displaying the image
cv2.imshow(window_name, image) 
```

**输出:**
![](img/4365ec5f79c9e9b2b701980f3c5fcf44.png)