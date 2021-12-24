# Python OpenCV–destroyAllWindows()函数

> 原文:[https://www . geesforgeks . org/python-opencv-destroyallwindows-function/](https://www.geeksforgeeks.org/python-opencv-destroyallwindows-function/)

**Python Opencv destroyAllWindow()功能**允许用户随时破坏**所有**窗口。它不接受任何参数，也不返回任何内容。它类似于 destroyWIndow()。destroyWindow()只销毁一个特定的窗口，但在 destroyAllWindow()的情况下，它会销毁所有窗口。

### **示例 1:使用 destroyWindow()**

我们制作了两个名为“P”和“Q”的窗口，其中有一个 gfg 徽标的图像，然后在调用 waitKey()函数延迟关闭窗口之前，我们将使用 destroyWindow()只销毁名为“P”的窗口。我们将看到窗口“Q”被延迟关闭。

## 巨蟒

```py
# importing cv2 module
import cv2

# read the image
img = cv2.imread("gfg_logo.png")

# showing the images
cv2.imshow('P', img)
cv2.imshow('Q', img)

# Destroying the window named P before
# calling the waitKey() function
cv2.destroyWindow('P')

# using the wait key function to delay the
# closing of windows till any ke is pressed
cv2.waitKey(0)
```