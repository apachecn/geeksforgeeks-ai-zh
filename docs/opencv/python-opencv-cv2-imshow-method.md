# Python OpenCV | cv2.imshow()方法

> 原文:[https://www . geesforgeks . org/python-opencv-cv2-im show-method/](https://www.geeksforgeeks.org/python-opencv-cv2-imshow-method/)

**OpenCV-Python** 是一个 Python 绑定库，旨在解决计算机视觉问题。方法用于在窗口中显示图像。窗口会自动适应图像大小。

> **语法:** cv2.imshow(window_name，image)
> **参数:**
> **window_name:** 表示要显示图像的窗口名称的字符串。
> **图像:**是要显示的图像。
> **返回值:**不返回任何东西。

**图像用于以下所有示例:**

![](img/c8773af5d93591c46b33a4bf4342545d.png)

**示例#1:**

```py
# Python program to explain cv2.imshow() method 

# importing cv2 
import cv2 

# path 
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks.png'

# Reading an image in default mode
image = cv2.imread(path)

# Window name in which image is displayed
window_name = 'image'

# Using cv2.imshow() method 
# Displaying the image 
cv2.imshow(window_name, image)

#waits for user to press any key 
#(this is necessary to avoid Python kernel form crashing)
cv2.waitKey(0) 

#closing all open windows 
cv2.destroyAllWindows() 
```

**输出:**

![](img/996f52713f26dd21ef93a947d4ed5ce4.png)

**例 2:**

```py
# Python program to explain cv2.imshow() method

# importing cv2
import cv2

# path
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks.png'

# Reading an image in grayscale mode
image = cv2.imread(path, 0)

# Window name in which image is displayed
window_name = 'image'

# Using cv2.imshow() method
# Displaying the image
cv2.imshow(window_name, image)

# waits for user to press any key
# (this is necessary to avoid Python kernel form crashing)
cv2.waitKey(0)

# closing all open windows
cv2.destroyAllWindows()
```

**输出:**

![](img/9eac563803dd3d586b153f5f3a5db1e4.png)