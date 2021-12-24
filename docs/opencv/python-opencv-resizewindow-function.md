# Python OpenCV–resizeWindow()函数

> 原文:[https://www . geesforgeks . org/python-opencv-resizewindow-function/](https://www.geeksforgeeks.org/python-opencv-resizewindow-function/)

**Python OpenCV 中的 resizeWindow()方法**用于将显示图像/视频的窗口调整到特定大小。指定的窗口大小适用于除工具栏之外的图像。这仅适用于创建的具有除 **CV_WINDOW_AUTOSIZE 以外的标志的窗口。**

> **语法:**cv2 . resizewindow(window _ name，width，height)
> 
> **参数:**
> 
> *   **窗口名称:**将显示图像/视频的窗口的名称
> *   **宽度:**新窗口宽度(整数型)**T3】**
> *   **高度:**新窗口高度(整数型)
> 
> **返回值:**不返回任何东西

**用于以下示例的图像:**

![](img/c443d6e70c63bf44b5da4595c5777d3b.png)

**例 1:**

## 蟒蛇 3

```py
# Python program to explain cv2.resizeWindow() method

# Importing cv2
import cv2

# Path
path = 'C:/Users/art/OneDrive/Desktop/geeks.png'

# Reading an image in default mode
image = cv2.imread(path)

# Naming a window
cv2.namedWindow("Resized_Window", cv2.WINDOW_NORMAL)

# Using resizeWindow()
cv2.resizeWindow("Resized_Window", 300, 700)

# Displaying the image
cv2.imshow("Resized_Window", image)
cv2.waitKey(0)
```

**输出:**

![](img/c585f2f4d5613541743cece550689d9f.png)

**例 2:**

## 蟒蛇 3

```py
# Python program to explain cv2.resizeWindow() method

# Importing cv2
import cv2

# Path
path = 'C:/Users/art/OneDrive/Desktop/geeks.png'

# Reading an image in grayscale mode
image = cv2.imread(path, 0)

# Naming a window
cv2.namedWindow("Resize", cv2.WINDOW_NORMAL)

# Using resizeWindow()
cv2.resizeWindow("Resize", 700, 200)

# Displaying the image
cv2.imshow("Resize", image)
cv2.waitKey(0)
```

**输出:**

![](img/0c6924c58dd9a9200ec70407d480088c.png)