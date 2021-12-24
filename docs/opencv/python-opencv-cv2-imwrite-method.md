# Python OpenCV | cv2.imwrite()方法

> 原文:[https://www . geesforgeks . org/python-opencv-cv2-imwrite-method/](https://www.geeksforgeeks.org/python-opencv-cv2-imwrite-method/)

**OpenCV-Python** 是一个 Python 绑定库，旨在解决计算机视觉问题。`cv2.imwrite()`方法用于将图像保存到任何存储设备。这将根据当前工作目录中指定的格式保存图像。

> **语法:** cv2.imwrite(文件名，图像)
> 
> **参数:**
> **文件名:**代表文件名的字符串。文件名必须包括像**这样的图像格式。jpg，。png、**等。
> **图像:**是要保存的图像。
> 
> **返回值:**如果图像保存成功，则返回真。

**示例#1:**

```py
# Python program to explain cv2.imwrite() method

# importing cv2 
import cv2

# importing os module  
import os

# Image path
image_path = r'C:\Users\Rajnish\Desktop\GeeksforGeeks\geeks.png'

# Image directory
directory = r'C:\Users\Rajnish\Desktop\GeeksforGeeks'

# Using cv2.imread() method
# to read the image
img = cv2.imread(image_path)

# Change the current directory 
# to specified directory 
os.chdir(directory)

# List files and directories  
# in 'C:/Users/Rajnish/Desktop/GeeksforGeeks'  
print("Before saving image:")  
print(os.listdir(directory))  

# Filename
filename = 'savedImage.jpg'

# Using cv2.imwrite() method
# Saving the image
cv2.imwrite(filename, img)

# List files and directories  
# in 'C:/Users / Rajnish / Desktop / GeeksforGeeks'  
print("After saving image:")  
print(os.listdir(directory))

print('Successfully saved')
```

**输出:**

```py
Before saving image:
['geeks.png']
After saving image:
['geeks.png', 'savedImage.jpg']
Successfully saved

```