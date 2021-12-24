# Python OpenCV–name dwindow()函数

> 原文:[https://www . geesforgeks . org/python-opencv-namedwindow-function/](https://www.geeksforgeeks.org/python-opencv-namedwindow-function/)

**Python OpenCV namedWindow()方法**用于创建一个具有合适名称和大小的窗口，在屏幕上显示图像和视频。默认情况下，图像以其原始大小显示，因此我们可能需要调整图像大小以适合我们的屏幕。

创建的窗口由它们的名称引用，也可以用作占位符。如果存在同名窗口，该函数不执行任何操作。

> **语法:** cv2.namedWindow(window_name，flag)
> 
> **参数:**
> 
> *   **窗口名称:**将显示图像/视频的窗口的名称
> *   **标志:**表示窗口大小是否自动设置或可调。
> 
> **一些标志值为:**
> 
> *   **窗口 _ 正常–**允许手动更改窗口大小
> *   **WINDOW_AUTOSIZE(默认)–**自动设置窗口大小
> *   **窗口 _ 全屏–**将窗口大小更改为全屏
> 
> **返回值:**不返回任何东西

### **用于以下所有示例的图像:**

![](img/8372c3ba4ddb8fba8d2ea9bbefac462f.png)

### **示例 1:自动设置窗口大小的**工作方式

## 蟒蛇 3

```py
# Python program to explain cv2.namedWindow() method

# Importing OpenCV
import cv2

# Path to image in local directory
path = 'C:/Users/art/OneDrive/Desktop/geeks.png'

# Using cv2.imread() to read an image in default mode
image = cv2.imread(path)

# Using namedWindow()
# A window with 'Display' name is created
# with WINDOW_AUTOSIZE, window size is set automatically
cv2.namedWindow("Display", cv.WINDOW_AUTOSIZE)

# using cv2.imshow() to display the image
cv2.imshow('Display', image)

# Waiting 0ms for user to press any key
cv2.waitKey(0)

# Using cv2.destroyAllWindows() to destroy
# all created windows open on screen
cv2.destroyAllWindows()
```

**输出:**

![](img/8b538566ecfd93e11b82430f0c79cfb1.png)

**说明**:

*   在这段代码中，为了使用 namedWindow 函数，OpenCV python 库被导入。
*   然后，通过使用 cv2.imread，来自特定位置(路径)的文件在默认模式下被加载到“image”变量中。
*   现在创建一个有“显示”名称和图像自动大小的窗口。
*   通过使用 cv2.imshow，自定义窗口将显示在屏幕上。等待 0 毫秒后，用户可以通过按键盘上的任意键来破坏所有窗口。

### **示例 2: M** 手动更改窗口大小

## 蟒蛇 3

```py
# Python Program to explain namedWindow() method

# Importing OpenCV
import cv2

# Path to image in local directory
path = 'C:/Users/art/OneDrive/Desktop/geeks.png'

# Using cv2.imread() to read an image in grayscale mode
image = cv2.imread(path, 0)

# Using namedWindow()
# A window with 'Display_Image' name is created
# with WINDOW_NORMAL allowing us to have random size
cv2.namedWindow("Display_Image", cv.WINDOW_NORMAL)

# Using cv2.imshow() to display the image
cv2.imshow('Display_Image', image)

# Waiting 0ms for user to press any key
cv2.waitKey(0)

# Using cv2.destroyAllWindows() to destroy
# all created windows open on screen
cv2.destroyAllWindows()
```

**输出:**

![](img/c9b7321db384ec96ec24a02e6592e762.png)

**注意:**当用户随机改变大小时，窗口大小被改变图像的维度保持不变。