# 使用 OpenCV 和 Python 对图像进行水印处理

> 原文:[https://www . geesforgeks . org/水印-images-with-opencv-and-python/](https://www.geeksforgeeks.org/watermarking-images-with-opencv-and-python/)

在本文中，我们将看到如何使用 Python 中的 OpenCV 制作水印图像。

水印是故意留在图像上的文本/徽标。艺术家通常使用水印来保护图像的版权。使用水印，我们可以确保图像的所有者是将水印印在图像上的人。

**让我们借助一个例子来理解这一点，我们所说的图像上的水印是什么意思:**

![](img/d5bfed61973a8c7dbbd7dfa33c8b98c0.png)

水印前的图像

标志:

![](img/b6304666addc056095dfc6e62d8da627.png)

很快. jpg

### **分步实施:**

**第一步:**导入 OpenCV，读取要应用水印的 logo 和图片。

## 蟒蛇 3

```py
# watermarking image using OpenCV

# importing cv2
import cv2

# importing logo that we are going to use
logo = cv2.imread("logo.jpg")

# importing image on which we are going to 
# apply watermark
img = cv2.imread("dark.png")
```

**第二步:**计算两幅图像的高度和宽度，并保存到其他变量中。我们需要计算宽度和高度，因为我们将把水印放在图像的某个地方，为此，我们只需要知道徽标和图像的适当宽度和高度。

## 蟒蛇 3

```py
# calculating dimensions
# height and width of the logo
h_logo, w_logo, _ = logo.shape

# height and width of the image
h_img, w_img, _ = img.shape
```

这里，我们使用了 OpenCV 中的 **shape** 函数，该函数返回图像的高度和宽度的元组。

**第三步:**现在我们要计算图像中心的坐标，因为我们要把水印放在图像的中心。

## 蟒蛇 3

```py
# calculating coordinates of center
# calculating center, where we are going 
# to place our watermark
center_y = int(h_img/2)
center_x = int(w_img/2)

# calculating from top, bottom, right and left
top_y = center_y - int(h_logo/2)
bottom_y = top_y + h_logo
right_x = left_x + w_logo
left_x = center_x - int(w_logo/2)
```