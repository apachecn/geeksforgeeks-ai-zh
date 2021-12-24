# 使用 Python OpenCV 检测特定颜色(此处为蓝色)

> 原文:[https://www . geesforgeks . org/detection-specific-color blue-using-opencv-python/](https://www.geeksforgeeks.org/detection-specific-colorblue-using-opencv-python/)

python 中的以下代码使用了用于图像处理技术的 OpenCV 库。该程序允许检测实时流视频内容中的特定颜色。视频由不同时刻的无限帧组成。我们将逐个检测每一帧的颜色。
**代码只会在 linux 环境下编译。**T3】

运行程序前，确保系统中安装了 **openCV** 。
**安装:**

*   在您的终端上运行以下命令，从 Ubuntu 或 Debian 安装它。

```
sudo apt-get install libopencv-dev python-opencv
```

*   或者，要从官方网站下载 OpenCV，请运行以下命令:

```
bash install-opencv.sh
```

在你的终端上。键入您的 sudo 密码，您将安装 OpenCV。由于要安装的包和编译过程，此操作可能需要很长时间。

*   要安装 numpy，只需使用命令:

```
sudo pip install numpy
```

## 蟒蛇 3

```
# Python program for Detection of a
# specific color(blue here) using OpenCV with Python
import cv2
import numpy as np

# Webcamera no 0 is used to capture the frames
cap = cv2.VideoCapture(0)

# This drives the program into an infinite loop.
while(1):       
    # Captures the live stream frame-by-frame
    _, frame = cap.read()
    # Converts images from BGR to HSV
    hsv = cv2.cvtColor(frame, cv2.COLOR_BGR2HSV)
    lower_blue = np.array([110,50,50])
    upper_blue = np.array([130,255,255])

    # Here we are defining range of bluecolor in HSV
    # This creates a mask of blue coloured
    # objects found in the frame.
    mask = cv2.inRange(hsv, lower_blue, upper_blue)

    # The bitwise and of the frame and mask is done so
    # that only the blue coloured objects are highlighted
    # and stored in res
    res = cv2.bitwise_and(frame,frame, mask= mask)
    cv2.imshow('frame',frame)
    cv2.imshow('mask',mask)
    cv2.imshow('res',res)

    # This displays the frame, mask
    # and res which we created in 3 separate windows.
    k = cv2.waitKey(5) & 0xFF
    if k == 27:
        break

# Destroys all of the HighGUI windows.
cv2.destroyAllWindows()

# release the captured frame
cap.release()
```

**代码说明:**

*   **相机设置:**为了执行运行时操作，使用设备的网络相机。要捕捉视频，我们需要创建一个 VideoCapture 对象。它的参数可以是设备索引或视频文件的名称。设备索引只是指定哪个摄像机的数字。通常会连接一个摄像头，所以我们只需传递 0。您可以通过传递 1 来选择第二个摄像机，以此类推。之后，您可以逐帧捕捉。但最后，别忘了释放捕获。此外，如果有人想在任何图像上应用这种颜色检测技术，只需对代码稍加修改就可以完成，我将在后面讨论。
*   **捕捉帧:**使用无限循环，以便网络摄像机在每个实例中捕捉帧，并在整个程序过程中打开。
    在逐帧捕获实时流后，我们将 BGR 颜色空间(默认)中的每一帧转换为 HSV 颜色空间。OpenCV 中有 150 多种颜色空间转换方法。但是我们将只研究两个最广泛使用的，BGR 对格雷和 BGR 对 HSV。对于颜色转换，我们使用函数 cv2.cvtColor(input_image，flag)，其中 flag 决定转换的类型。对于 BGR 至 HSV，我们使用旗帜 cv2。COLOR_BGR2HSV。现在我们知道如何将 BGR 图像转换成 HSV，我们可以用它来提取彩色物体。在 HSV 中，表示一种颜色比 RGB 颜色空间更容易。
    在指定范围时，我们已经指定了蓝色的范围。而你可以输入任何你想要的颜色范围。
*   **蒙版技术:**蒙版基本上是按照一定的规则创建图像的某个特定区域。这里我们正在创建一个由蓝色物体组成的遮罩。之后，我在输入图像和阈值图像上使用了按位 and，这样只有蓝色的对象被突出显示并存储在 res.
    然后我们使用 imshow 函数在 3 个单独的窗口上显示帧、res 和遮罩。
*   **显示帧:**由于 imshow()是 HighGui 的一个功能，需要定期调用 waitKey，以处理其事件循环。【waitKey()函数等待按键事件“延迟”(这里是 5 毫秒)。如果不调用 waitKey，HighGui 就无法处理窗口事件，如重绘、调整大小、输入事件等。所以尽管有 1 毫秒的延迟，还是叫它吧。
*   **总结流程**:
    1.  拍下视频的每一帧。
    2.  将每一帧从 BGR 转换到 HSV 色彩空间。
    3.  阈值的 HSV 图像的蓝色范围。

本文由 **Pratima Upadhyay** 供稿。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[contribute.geeksforgeeks.org](http://www.contribute.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 contribute@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。