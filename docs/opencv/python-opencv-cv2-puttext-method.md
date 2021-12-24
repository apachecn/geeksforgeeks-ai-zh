# Python OpenCV | cv2.putText()方法

> 原文:[https://www . geesforgeks . org/python-opencv-cv2-puttext-method/](https://www.geeksforgeeks.org/python-opencv-cv2-puttext-method/)

**OpenCV-Python** 是一个 Python 绑定库，旨在解决计算机视觉问题。`cv2.putText()`方法用于在任意图像上绘制文本字符串。

> **语法:** cv2.putText(图像、文本、组织、字体、字体比例、颜色[、厚度[、线型[、底部左侧原点]])
> 
> **参数:**
> **图像:**就是要在上面画文字的图像。
> **文本:**要绘制的文本字符串。
> **org:** 是图像中文本字符串左下角的坐标。坐标表示为两个值的元组(即 **X** 坐标值， **Y** 坐标值)。
> **字体:**表示字体类型。字体类型有**FONT _ HERSHEY _ SIMPLY、FONT_HERSHEY_PLAIN、**等。
> **字体比例:**字体比例因子，乘以特定字体的基本大小。
> **颜色:**是要绘制的文本字符串的颜色。对于 **BGR** ，我们传递一个元组。例如:(255，0，0)代表蓝色。
> **厚度:**是 **px** 中线条的厚度。
> **线型:**这是可选参数。它给出了要使用的线的类型。
> **bottomLeftOrigin:** 这是可选参数。为真时，图像数据原点在左下角。否则，它在左上角。
> 
> **返回值:**返回图像。

**图像用于以下所有示例:**
![](img/c8773af5d93591c46b33a4bf4342545d.png)

**示例#1:**

```
# Python program to explain cv2.putText() method

# importing cv2
import cv2

# path
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks\geeks.png'

# Reading an image in default mode
image = cv2.imread(path)

# Window name in which image is displayed
window_name = 'Image'

# font
font = cv2.FONT_HERSHEY_SIMPLEX

# org
org = (50, 50)

# fontScale
fontScale = 1

# Blue color in BGR
color = (255, 0, 0)

# Line thickness of 2 px
thickness = 2

# Using cv2.putText() method
image = cv2.putText(image, 'OpenCV', org, font, 
                   fontScale, color, thickness, cv2.LINE_AA)

# Displaying the image
cv2.imshow(window_name, image) 
```

![](img/acd5502a8a02b5018a739cbda2451123.png)

**例 2:**

```
# Python program to explain cv2.putText() method

# importing cv2
import cv2

# path
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks\geeks.png'

# Reading an image in default mode
image = cv2.imread(path)

# Window name in which image is displayed
window_name = 'Image'

# text
text = 'GeeksforGeeks'

# font
font = cv2.FONT_HERSHEY_SIMPLEX

# org
org = (00, 185)

# fontScale
fontScale = 1

# Red color in BGR
color = (0, 0, 255)

# Line thickness of 2 px
thickness = 2

# Using cv2.putText() method
image = cv2.putText(image, text, org, font, fontScale, 
                 color, thickness, cv2.LINE_AA, False)

# Using cv2.putText() method
image = cv2.putText(image, text, org, font, fontScale,
                  color, thickness, cv2.LINE_AA, True) 

# Displaying the image
cv2.imshow(window_name, image) 
```

**输出:**
![](img/d149bb5b3980267111c2fd0c7ff05d04.png)