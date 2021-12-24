# Python OpenCV–setWindowTitle()函数

> 原文:[https://www . geesforgeks . org/python-opencv-setwindowtitle-function/](https://www.geeksforgeeks.org/python-opencv-setwindowtitle-function/)

**Python OpenCV setWindowTitle()方法**用于给出窗口的标题。它需要 2 个参数，即窗口名和需要给出的标题。这两个参数都应该是字符串类型。

> **语法:** cv2.setWindowTitle( winname，Title)
> 
> **参数:**
> 
> *   **winname:** 窗口名称
> *   **标题:**标题我们要为窗口设置上面的名字。

## Python OpenCV setWindowTitle()方法示例

这里我们将看到一个示例代码。我们有一个名为“gfg_logo.png”的 gfg 徽标的 png 图像，对于本例，我们将使用 OpenCV 的 [imread()](https://www.geeksforgeeks.org/python-opencv-cv2-imread-method/) 和 [imshow()](https://www.geeksforgeeks.org/python-opencv-cv2-imshow-method/) 方法在窗口上显示它。我们将 Windows 标题从默认名称更改为“你好！”使用 setWindowTitle()方法。我们将传递参数窗口名“gfg”和我们想要设置为参数的标题。

## 计算机编程语言

```
# importing cv2 module
import cv2

# read the image
img = cv2.imread("gfg_logo.png")

# showing the image
cv2.imshow('gfg', img)

# Setting the windows title to "Hello!"
# using setWindowTitle method
cv2.setWindowTitle('gfg', 'Hello!')

# waiting using waitKey method
cv2.waitKey(0)
```

**输出:**

![](img/ba7d8239bd8a1bd4c0688bfaea932ac4.png)