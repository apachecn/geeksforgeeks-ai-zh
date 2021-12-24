# 使用 Python–OpenCV 为图像添加边框

> 原文:[https://www . geesforgeks . org/add-borders-to-images-use-python-opencv/](https://www.geeksforgeeks.org/adding-borders-to-the-images-using-python-opencv/)

图像处理是当今人工智能和机器学习时代的一个有趣领域。我们可以看到图像处理在日常生活中的应用，比如每当我们对任何图像(自拍)应用滤镜时，或者当我们想要应用一些效果(比如模糊图像等)时。

在本文中，我们将讨论如何使用 Python 为图像添加边框。Python 提供了一个名为 **OpenCV** 的模块，可以用于同样的目的。所以在添加边框之前，让我们看一个关于 OpenCV 的小介绍。

[**OpenCV**](https://www.geeksforgeeks.org/opencv-python-tutorial/) **(开源计算机视觉库)**

*   这是一个开源图书馆。
*   旨在解决计算机视觉问题。
*   它利用高度优化的数值操作库，即[](https://www.geeksforgeeks.org/python-numpy/)**以及 [**MATLAB**](https://www.geeksforgeeks.org/applications-of-matlab/) 风格语法。**

**要给图像添加边框 **OpenCV** 有一个包 [**copyMakeBorder**](https://www.geeksforgeeks.org/python-opencv-cv2-copymakeborder-method/) 可以帮助在图像周围制作边框。**

> ****语法:**cv 2 . copy makefile()**
> 
> ****复制边框参数:****
> 
> *   **输入影像**
> *   **topBorderWidth**
> *   **底部边框宽度**
> *   **左边框宽度**
> *   **右边框宽度**
> *   **cv2。边框 _ 常数**
> *   **值=边框颜色**

****输入图像:****

**![](img/796a1e9dbe79940ef20693960b818abc.png)**

****示例:****

## **蟒蛇 3**

```
# importing required packages

import cv2

# reading the image
virat_img = cv2.imread('geek.jpg')

# making border around image using copyMakeBorder
borderoutput = cv2.copyMakeBorder(
    virat_img, 20, 20, 20, 20, cv2.BORDER_CONSTANT, value=[255, 255, 0])

# showing the image with border
cv2.imwrite('output.png', borderoutput)
```

****输出:****

**![](img/ce8af37fabd16c2083ba738e299616c5.png)**