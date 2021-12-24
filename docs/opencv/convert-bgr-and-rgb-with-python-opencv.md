# 用 Python 转换 BGR 和 RGB–OpenCV

> 原文:[https://www . geesforgeks . org/convert-bgr-and-RGB-with-python-opencv/](https://www.geeksforgeeks.org/convert-bgr-and-rgb-with-python-opencv/)

**先决条件:** [OpenCV](https://www.geeksforgeeks.org/opencv-python-tutorial/)

**OpenCV** 是一个巨大的开源库，用于计算机视觉、机器学习和图像处理。OpenCV 支持多种编程语言，如 Python、C++、Java 等。它可以处理图像和视频来识别物体、人脸，甚至是人类的笔迹。  在本文中，我们将使用 **python** 和 **OpenCV** 将一个 **BGR** 图像转换为 **RGB** 。

OpenCV 使用 BGR 图像格式。因此，当我们使用 cv2.imread()读取图像时，默认情况下它会以 BGR 格式进行解释。

我们可以使用 cvtColor()方法将 BGR 图像转换为 RGB，反之亦然。

> **语法:** cv2.cvtColor(代码)
> 
> **参数:**
> 
> *   **cv 2 . color _ bgr 2 RGB**bgr──bgr。
> *   **cv 2 . color _ RGB 2 bgr**–RGBürürürürürürürürürürürürürürürürürürürürürürürürürürürürürürürürürürürürürürürürü

将 BGR 图像转换为 RGB(反之亦然)可能有几个原因，其中之一是几个图像处理库具有不同的像素顺序。

### 方法

*   导入模块
*   读取图像
*   使用 cvtColor()进行转换
*   添加等待键
*   添加销毁窗口机制

**图片使用:** [苹果](https://www.applesfromny.com/varieties/fortune/)

首先，我们将显示导入的图像，也就是 BGR 格式。

**例:**

## 蟒 3

```py
import cv2

image = cv2.imread("/content/gfg.jpeg")
cv2.imshow('image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```