# 使用 Matplotlib

计算图像的面积

> 原文:[https://www . geeksforgeeks . org/使用-matplotlib/](https://www.geeksforgeeks.org/calculate-the-area-of-an-image-using-matplotlib/) 计算图像面积

让我们看看如何使用 Matplotlib 在 Python 中计算图像的面积。

**算法:**

1.  导入 matplotlib.pyplot 模块。
2.  使用 imread()方法导入图像。
3.  使用图像的形状属性获取图像的高度和宽度。它获取图像中的通道数。
4.  面积计算为，面积=高度*宽度。
5.  显示区域。

**示例 1:** 考虑以下图像:

![](img/a1184afd4777e62c0ad57095dd848bf6.png)

" GFG.jpg "

## 蟒蛇 3

```py
# import necessary library
import matplotlib.pyplot as plt

# read an image
img = plt.imread("GFG.jpg")

# fetch the height and width
height, width, _ = img.shape

# area is calculated as “height x width”
area = height * width

# display the area
print("Area of the image is : ", area)
```

**输出:**

```py
Area of the image is : 50244
```

**示例 2:** 考虑以下图像:

![](img/025fa5029c9f85b1949b8650968da322.png)

" image.jpg "

## 蟒蛇 3

```py
# import necessary library
import matplotlib.pyplot as plt

# read an image
img = plt.imread("image.jpg")

# fetch the height and width
height, width, _ = img.shape

# area is calculated as “height x width”
area = height * width

# display the area
print("Area of the image is : ", area)
```

**输出:**

```py
Area of the image is : 213200
```