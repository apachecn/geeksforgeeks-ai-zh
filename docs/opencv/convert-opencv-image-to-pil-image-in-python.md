# 将 OpenCV 图像转换为 Python 中的 PIL 图像

> 原文:[https://www . geesforgeks . org/convert-opencv-image-to-pil-image-in-python/](https://www.geeksforgeeks.org/convert-opencv-image-to-pil-image-in-python/)

[OpenCV](https://www.geeksforgeeks.org/opencv-python-tutorial/) 是一个巨大的开源库，用于计算机视觉、机器学习和图像处理。OpenCV 支持多种编程语言，如 Python、C++、Java 等。它可以处理图像和视频来识别物体、人脸，甚至是人类的笔迹。当它与各种库集成时，比如 Numpy，这是一个高度优化的数值操作库，那么你的武器库中的武器数量就会增加，也就是说，无论你在 Numpy 中能做什么操作，都可以与 OpenCV 相结合。

[Python 图像库(PIL 的扩展)](https://www.geeksforgeeks.org/python-pillow-a-fork-of-pil/)是 Python 语言事实上的图像处理包。它集成了轻量级图像处理工具，有助于编辑、创建和保存图像。对 Python 图像库的支持在 2011 年停止了，但是一个名为枕头的项目分叉了最初的 PIL 项目，并增加了对 Python3.x 的支持。枕头被宣布为 PIL 未来使用的替代品。枕头支持多种图像文件格式，包括 BMP、PNG、JPEG 和 TIFF。该库鼓励通过创建新的文件解码器来增加对库中新格式的支持。

OpenCV 图像和 PIL 图像的基本区别是 OpenCV 遵循 BGR 颜色惯例，PIL 遵循 RGB 颜色惯例，转换的方法将基于这种差异。

### **进场:**

*   导入模块
*   我们将使用 cv2 库的 [**imread**](https://www.geeksforgeeks.org/python-opencv-cv2-imread-method/) 方法获取输入图像。

**语法:**

```
imread(path, flag)
```

**参数:**

1.  **路径:**表示要读取的图像的路径的字符串。
2.  **标志:**指定应该如何读取图像。它的默认值是 cv2。IMREAD_COLOR。

**返回值:**该方法返回从指定文件加载的图像。

*   然后我们将使用 cv2 库的 [**cv2.cvtColor()**](https://www.geeksforgeeks.org/python-opencv-cv2-cvtcolor-method/) 方法来改变颜色约定。

**语法:**

```
cvtColor(src, code[, dst[, dstCn]])
```

**参数:**

1.  **src:** 是要改变颜色空间的图像。
2.  **代码:**是色彩空间转换代码。
3.  **dst:** 是与 src 图像大小和深度相同的输出图像。这是一个可选参数。
4.  **dstCn:** 是目的图像中的通道数。如果参数为 0，则通道数自动从 src 和代码中导出。这是一个可选参数。

**返回值:**返回图像。

*   显示图像。

您会注意到，即使在转换之后，这两幅图像也是相同的。因此，我们可以说我们已经成功地将 OpenCV 图像转换为 PIL 图像。

下面给出了使用上述方法的实现。

**程序:**

## 蟒蛇 3

```
# Python program to convert from openCV2 to PIL

import cv2
from PIL import Image

# Open image using openCV2
opencv_image = cv2.imread("logo.png")

# Notice the COLOR_BGR2RGB which means that the color is
# converted from BGR to RGB
color_coverted = cv2.cvtColor(opencv_image, cv2.COLOR_BGR2RGB)

# Displaying the Scanned Image by using cv2.imshow() method
cv2.imshow("OpenCV Image", opencv_image)

# Displaying the converted image
pil_image = Image.fromarray(color_coverted)
pil_image.show()

# waits for user to press any key
# (this is necessary to avoid Python kernel form crashing)
cv2.waitKey(0)

# closing all open windows
cv2.destroyAllWindows()
```

**输入:**

![](img/4dbb0f54608329250455b44fecfb5652.png)

**输出:**

*   **OpenCV 图像:**

![](img/5cfe78701c4a086fc9f74ef5502082c5.png)

*   **GDP 形象:**

![](img/756802e51972ad2c27eefdcc3e0e94ee.png)