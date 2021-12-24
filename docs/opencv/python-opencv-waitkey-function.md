# Python OpenCV–waitKey()函数

> 原文:[https://www . geesforgeks . org/python-opencv-waitkey-function/](https://www.geeksforgeeks.org/python-opencv-waitkey-function/)

Python OpenCV 的 **waitkey()函数**允许用户在给定的毫秒内显示一个窗口，或者直到按下任何一个键。它以毫秒为单位作为一个参数，等待给定的时间来破坏窗口，如果在参数中传递 0，它会一直等到按下任何键。

### 示例 1:显示有时间限制的图像

使用 waitKey()方法，我们在图像自动关闭前显示图像 5 秒钟。代码如下:

## 【蟒蛇】

```py
# importing cv2 module
import cv2

# read the image
img = cv2.imread("gfg_logo.png")

# showing the image
cv2.imshow('gfg', img)

# waiting using waitKey method
cv2.waitKey(5000)
```