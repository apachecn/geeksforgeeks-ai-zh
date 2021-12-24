# Python | OpenCV 程序读取并保存图像

> 原文:[https://www . geesforgeks . org/python-opencv-程序读取和保存图像/](https://www.geeksforgeeks.org/python-opencv-program-to-read-and-save-an-image/)

OpenCV(开源计算机视觉)是一个主要针对实时计算机视觉的编程函数库。这是一个跨平台的库，它提供了多种语言使用的功能。

说到图像处理，OpenCV 使我们能够对图像执行多种操作，但是为了做到这一点，我们需要读取一个图像文件作为输入，然后我们可以执行所需的操作并保存它。

让我们看一个简单的操作，使用 OpenCV 库读取图像文件，然后保存。

**使用的功能:**

> **->imread(Location _ of _ image，整数):**第二个参数是用于更改图像颜色的整数。-1 读取图像不变，0 读取灰度图像。
> 
> **->imwrite(Name _ after _ save，variable _ containing _ read _ image)**
> 
> **- >等待键(0):** 执行后将保持窗口打开，直到按下一个键
> 
> **- > destroyAllWindow():** 它将关闭程序运行期间打开的所有窗口。

下面是 Python 实现:

```py
# Python Program To Read And Save image 
import numpy as np
import cv2

# This will give error if you don't have a cv2 module
img = cv2.imread("G:\demo.jpg", -1)

# img is object of cv2 and stores the image read demo.jpg
cv2.imwrite("outputimage.jpg", img)

# The image is saved in folder where program is stored
cv2.waitKey(0)

cv2.destroyAllWindow()
```

**输入:**
![](img/7969db4b869728704b5e0ba57486bc7a.png)

**输出:**
![](img/1e59aeed3621625f38035a8f731c3d9f.png)