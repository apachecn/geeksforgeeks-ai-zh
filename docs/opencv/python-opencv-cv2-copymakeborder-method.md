# Python OpenCV | cv2 . copymakedborder()方法

> 原文:[https://www . geeksforgeeks . org/python-opencv-cv2-copy make border-method/](https://www.geeksforgeeks.org/python-opencv-cv2-copymakeborder-method/)

**OpenCV-Python** 是一个 Python 绑定库，旨在解决计算机视觉问题。cv2.copyMakeBorder()方法用于在图像周围创建像相框一样的边框。

> **语法:** cv2.copyMakeBorder(src，上，下，左，右，borderType，值)
> 
> **参数:**
> **src:** 它是源图像。
> **顶部:**是顶部方向以像素数表示的边框宽度。
> **底部:**是底部方向以像素数表示的边框宽度。
> **左:**是左边方向的边框宽度，以像素为单位。
> **右:**是右边方向的边框宽度，以像素为单位。
> **边框类型:**描绘需要添加什么样的边框。它由类似 **cv2 的标志定义。**， **cv2。BORDER_REFLECT** 等 **dest:** 是目的图像
> **值:**如果边框类型为 **cv2，则是描述边框颜色的可选参数。边框 _ 常量**。
> 
> **返回值:**返回图像。

边框类型标志描述如下:

> **cv2。BORDER_CONSTANT:** 增加一个不变的彩色边框。该值应作为关键字参数
> **cv2 给出。**边界将是边界元素的镜像。假设，如果图像包含字母“ **abcdefg** ，那么输出将是“ **gfedcba|abcdefg|gfedcba** ”。
> **cv2。BOrder _ REFLOW _ 101**或 **cv2。BORDER_DEFAULT:** 它的工作原理与 **cv2 相同。**但略有变化。假设，如果图像包含字母“ **abcdefgh** ”，那么输出将是“**gfedcb | abcdefgh | gfedcba**”。
> **cv2。BORDER_REPLICATE:** 它复制最后一个元素。假设，如果图像包含字母“ **abcdefgh** ”，那么输出将是“ **aaaaa|abcdefgh|hhhhh** ”。

**图像用于以下所有示例:**

![](img/c8773af5d93591c46b33a4bf4342545d.png)

**示例#1:**

## 蟒蛇 3

```
# Python program to explain cv2.copyMakeBorder() method

# importing cv2
import cv2

# path
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks\geeks.png'

# Reading an image in default mode
image = cv2.imread(path)

# Window name in which image is displayed
window_name = 'Image'

# Using cv2.copyMakeBorder() method
image = cv2.copyMakeBorder(image, 10, 10, 10, 10, cv2.BORDER_CONSTANT, None, value = 0)

# Displaying the image
cv2.imshow(window_name, image)
```

**输出:**

![](img/cdeaf76c677eeb656641dd94c861d3a5.png)

**例 2:**

## 蟒蛇 3

```
# Python program to explain cv2.copyMakeBorder() method

# importing cv2
import cv2

# path
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks\geeks.png'

# Reading an image in default mode
image = cv2.imread(path)

# Window name in which image is displayed
window_name = 'Image'

# Using cv2.copyMakeBorder() method
image = cv2.copyMakeBorder(image, 100, 100, 50, 50, cv2.BORDER_REFLECT)

# Displaying the image
cv2.imshow(window_name, image)
```

**输出:**

![](img/4247b5a3b4e7eccf0a87ac3fc3ddb8e5.png)