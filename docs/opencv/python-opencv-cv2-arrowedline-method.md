# Python OpenCV | cv2 . arrowedline()方法

> 原文:[https://www . geesforgeks . org/python-opencv-cv2-arrowed line-method/](https://www.geeksforgeeks.org/python-opencv-cv2-arrowedline-method/)

**OpenCV-Python** 是一个 Python 绑定库，旨在解决计算机视觉问题。
cv2.arrowedLine()方法用于绘制从起点指向终点的箭头线段。

> **语法:** cv2.arrowedLine(图像、起点、终点、颜色、粗细、线型、移位、tipLength)
> **参数:**
> **图像:**是要画线的图像。
> **起点:**是直线的起始坐标。坐标表示为两个值的元组(即 **X** 坐标值， **Y** 坐标值)。
> **终点:**是直线的终点坐标。坐标表示为两个值的元组(即 **X** 坐标值， **Y** 坐标值)。
> **颜色:**是待画线条的颜色。对于 **BGR** ，我们传递一个元组。例如:(255，0，0)代表蓝色。
> **厚度:**是 **px** 中线条的厚度。
> **line_type:** 表示要绘制的线的类型。
> **移位:**表示点坐标中的小数位数。
> **提示长度:**表示箭头相对于箭头长度的长度。
> **返回值:**返回一个图像。

**图像用于以下所有示例:**

![](img/c8773af5d93591c46b33a4bf4342545d.png)

**示例#1:**

## 蟒蛇 3

```py
# Python program to explain cv2.arrowedLine() method

# importing cv2
import cv2

# path
path = r'C:\Users\Atomix\Desktop\geeksforgeeks\geeks.png'

# Reading an image in default mode
image = cv2.imread(path)

# Window name in which image is displayed
window_name = 'Image'

# Start coordinate, here (0, 0)
# represents the top left corner of image
start_point = (0, 0)

# End coordinate
end_point = (200, 200)

# Green color in BGR
color = (0, 255, 0)

# Line thickness of 9 px
thickness = 9

# Using cv2.arrowedLine() method
# Draw a diagonal green arrow line
# with thickness of 9 px
image = cv2.arrowedLine(image, start_point, end_point,
                                     color, thickness)

# Displaying the image
cv2.imshow(window_name, image)
```

**输出:**

![](img/2dce4f49c9a58170e39f507ce7d5369c.png)

**例 2:**

## 蟒蛇 3

```py
# Python program to explain cv2.arrowedLine() method

# importing cv2
import cv2

# path
path = r'C:\Users\Atomix\Desktop\geeksforgeeks\geeks.png'

# Reading an image in default mode
image = cv2.imread(path)

# Window name in which image is displayed
window_name = 'Image'

# Start coordinate, here (225, 0)
# represents the top right corner of image
start_point = (225, 0)

# End coordinate
end_point = (0, 90)

# Red color in BGR
color = (0, 0, 255)

# Line thickness of 9 px
thickness = 9

# Using cv2.arrowedLine() method
# Draw a red arrow line
# with thickness of 9 px and tipLength = 0.5
image = cv2.arrowedLine(image, start_point, end_point,
                    color, thickness, tipLength = 0.5)

# Displaying the image
cv2.imshow(window_name, image)
```

**输出:**

![](img/a2c570aa86d9f9ee222dd40e5a516e72.png)