# Python OpenCV | cv2.erode()方法

> 原文:[https://www . geesforgeks . org/python-opencv-cv2-erode-method/](https://www.geeksforgeeks.org/python-opencv-cv2-erode-method/)

**OpenCV-Python** 是一个 Python 绑定库，旨在解决计算机视觉问题。`cv2.erode()`方法用于对图像进行腐蚀。侵蚀的基本思想就像土壤侵蚀一样，它侵蚀掉前景物体的边界(总是尽量保持前景为白色)。它通常在二进制图像上执行。它需要两个输入，一个是我们的原始图像，第二个是决定操作性质的结构元素或核。只有当内核下的所有像素都为 1 时，原始图像中的像素(1 或 0)才会被视为 1，否则它会被侵蚀(变为零)。

> **语法:** cv2.erode(src，kernel[，dst[，anchor[，iterations[，borderType[，border value]]]])
> **参数:**
> **src:** 就是要被腐蚀的图像。
> **内核:**用于腐蚀的结构元素。如果元素= Mat()，则使用 3×3 的矩形结构元素。可以使用[getstructuriangelement](https://docs.opencv.org/4.1.2/d4/d86/group__imgproc__filter.html#gac342a1bb6eabf6f55c803b09268e36dc)创建内核。
> **dst:** 是与 src 大小和类型相同的输出图像。
> **锚点:**是表示锚点的整型变量，默认值为 Point(-1，-1)，表示锚点在内核中心。
> **边框类型:**描绘需要添加什么样的边框。它由类似 **cv2 的标志定义。BORDER_CONSTANT** ， **cv2。BORDER _ REFLOW**等。
> **迭代次数:**是应用侵蚀的次数。
> **边框值:**是恒定边框情况下的边框值。
> **返回值:**返回图像。

**图像用于以下所有示例:**
![](img/e638a8aba84706d59fd64004a669dca6.png)
**示例#1:**

```
# Python program to explain cv2.erode() method 

# importing cv2 
import cv2

# importing numpy 
import numpy as np

# path 
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks\geeks.png'

# Reading an image in default mode 
image = cv2.imread(path) 

# Window name in which image is displayed 
window_name = 'Image'

# Creating kernel
kernel = np.ones((5, 5), np.uint8)

# Using cv2.erode() method 
image = cv2.erode(image, kernel) 

# Displaying the image 
cv2.imshow(window_name, image) 
```

**输出:**
![](img/ce4b605736fb4c5d8b7b7b977b9e44e8.png)

**例 2:**

```
# Python program to explain cv2.erode() method 

# importing cv2 
import cv2

# importing numpy 
import numpy as np

# path 
path = r'C:\Users\Rajnish\Desktop\geeksforgeeks\geeks.png'

# Reading an image in default mode 
image = cv2.imread(path) 

# Window name in which image is displayed 
window_name = 'Image'

# Creating kernel
kernel = np.ones((6, 6), np.uint8)

# Using cv2.erode() method 
image = cv2.erode(image, kernel, cv2.BORDER_REFLECT) 

# Displaying the image 
cv2.imshow(window_name, image) 
```

**输出:**
![](img/6116469011c000eb6d871265e8726d24.png)