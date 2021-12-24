# 使用 Python–OpenCV

检查图像是否为空

> 原文:[https://www . geesforgeks . org/check-if-the-image-is-empty-python-opencv/](https://www.geeksforgeeks.org/check-if-the-image-is-empty-using-python-opencv/)

**先决条件:**[OpenCV 基础知识](https://www.geeksforgeeks.org/set-opencv-anaconda-environment/)

OpenCV(开放源代码计算机视觉)是一个计算机视觉库，包含对图片或视频执行操作的各种功能。它最初由英特尔开发，但后来由 Willow Garage 维护，现在由 Itseez 维护。这个库是跨平台的，它有多种编程语言，如 Python、C++等。在本文中，我们将尝试使用 OpenCV **(开源计算机视觉)**来检查打开的图像是否为空。

为此，需要安装 OpenCV 库:

```py
pip install opencv-python
```

为了实现这个目标，我们将使用 [cv2.imread()](https://www.geeksforgeeks.org/python-opencv-cv2-imread-method/) 方法，如果这个方法读取图像，那么它将返回图像坐标矩阵，否则它将返回 None。

**输入图像:**

![](img/0308512ac34f6e672923afcbe025ad78.png)

Gfg.png

**示例:**

在这个例子中，我们将读取图像并检查是否找到。

## 蟒蛇 3

```py
# Importing OpenCV library
import cv2

# user define function
# that return None or
def check_empty_img(img):
    # Reading Image
    # You can give path to the
    # image as first argument
    image = cv2.imread(img)

    # Checking if the image is empty or not
    if image is None:
        result = "Image is empty!!"
    else:
        result = "Image is not empty!!"

    return result

# driver node
img = "Gfg.png"

# Calling and printing
# the function
print(check_empty_img(img))
```

**输出:**

```py
Image is not empty!!
```

**例 2:**

在这个例子中，这里没有找到图像。

## 蟒蛇 3

```py
# Importing OpenCV library
import cv2

# user define function
# that return None or
def check_empty_img(url):
    # Reading Image
    # You can give path to the
    # image as first argument
    image = cv2.imread(url)

    # Checking if the image is empty or not
    if image is None:
        result = "Image is empty!!"
    else:
        result = "Image is not empty!!"

    return result

# driver node
img = "geek.png"

# Calling and printing
# the function
print(check_empty_img(img))
```

**输出:**

```py
Image is empty!!
```