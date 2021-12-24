# 使用 Python–OpenCV

更改图像的对比度和亮度

> 原文:[https://www . geeksforgeeks . org/使用 python-opencv/](https://www.geeksforgeeks.org/changing-the-contrast-and-brightness-of-an-image-using-python-opencv/) 改变图像的对比度和亮度

改变任何图像的亮度和对比度是每个人对图像做的最基本的事情。这意味着改变图像的每个像素的值，可以通过乘以或除以图像的像素值来实现。在本文中，我们将看到如何使用 OpenCV Python 在漂亮的代码中实现我们的理论，

在开始之前，让我们试着理解一些基本概念，比如，什么是亮度？什么是对比？什么是像素？什么是 OpenCV？

*   **亮度:**当调节亮度时，图像内的整个色调范围会相应升高或降低。
*   **对比度:**提高对比度调整时，中间色调消除。该图像将具有较高的黑色或黑色和白色百分比，或者具有最少中间色调的高光。
*   **像素:**像素通常用于表示计算机显示器或屏幕的显示分辨率。像素越大，图像中的细节越多。
*   **OpenCV:** OpenCV 是用于计算机视觉、机器学习和图像处理的巨大开源库，现在它在实时操作中发挥着重要作用

**议程:**学习如何使用 OpenCV 调整图像的亮度和对比度。

**要求:** OpenCV

安装:

```py
pip install openCV
```

**进场:**

*   导入所需模块。
*   定义主要功能，定义其中需要的数据。
*   创建一个函数 brightness_contrast，以创建一个跟踪条来调整亮度和对比度。
*   创建另一个功能来更改亮度和对比度。
*   显示原始和编辑过的图像。
*   用“电子稳定控制”终止程序，或简单地关闭窗口。

**让我们逐步实现这个:**

**第一步:**这里我们将加载一个图像并创建一个跟踪条。

> **语法:** imread(文件名):filename(图像文件的名称)。
> 
> 名称窗口(winname): winname(窗口的名称)。

**代码:**

## 蟒蛇 3

```py
if __name__ == '__main__':
    # The function imread loads an
    # image from the specified file and returns it.
    original = cv2.imread("pic.jpeg")

    # Making another copy of an image.
    img = original.copy()

    # The function namedWindow creates
    # a window that can be used as
    # a placeholder for images.
    cv2.namedWindow('GEEK')

    # The function imshow displays
    # an image in the specified window.
    cv2.imshow('GEEK', original)

    # createTrackbar(trackbarName,
    # windowName, value, count, onChange)
    # Brightness range -255 to 255
    cv2.createTrackbar('Brightness', 'GEEK',
                       255, 2 * 255,
                       BrightnessContrast)

    # Contrast range -127 to 127
    cv2.createTrackbar('Contrast', 'GEEK',
                       127, 2 * 127,
                       BrightnessContrast) 

    BrightnessContrast(0)

# The function waitKey waits for
# a key event infinitely  or for
# delay milliseconds, when it is positive.
cv2.waitKey(0)
```

**第二步:**通过调用控制器功能，返回编辑后的图像，之后 imshow()功能将显示受影响的图像。

> **语法:** getTrackbarPos(trackbarname，winname):trackbarname(track bar 的名称)，winname(窗口的名称)

**代码:**

## 蟒蛇 3

```py
def BrightnessContrast(brightness=0):

    # getTrackbarPos returns the
    # current position of the specified trackbar.
    brightness = cv2.getTrackbarPos('Brightness',
                                    'GEEK')

    contrast = cv2.getTrackbarPos('Contrast',
                                  'GEEK')

    effect = controller(img,
                        brightness,
                        contrast)

    # The function imshow displays
    # an image in the specified window
    cv2.imshow('Effect', effect)
```

**第三步:**控制器功能会根据轨迹球位置控制图像的亮度和对比度，并返回编辑后的图像。

> **语法:**加权(src1、alpha、src2、beta、gamma)
> 
> **参数:**
> 
> **src1:** 第一个输入数组。
> **阿尔法:**(第一阵元素的权重。
> **src2:** 第二个输入数组，大小和通道号与 src1 相同。
> **β:**第二阵元的权重。
> **伽马:**标量加到每个和上。
> 
> 文字(图像、文字、组织、字体、字体比例、颜色、粗细、线型、底部左侧原点)
> 
> **img:** 图像。
> **文字:**待画文字串。
> **org:** 图像中文本字符串的左下角。
> **fontFace:** 字体类型，参见#HersheyFonts。
> **字体比例:**字体比例因子乘以特定字体的基本大小。
> **颜色:**文字颜色。
> **粗细:**用于绘制文字的线条粗细。
> l **ineType:** 线型。请参见#线型。
> **左下角原点:**为真时，图像数据原点在左下角。否则，它在左上角。

## 蟒蛇 3

```py
def controller(img, brightness=255, contrast=127):
    brightness = int((brightness - 0) * (255 - (-255)) / (510 - 0) + (-255))

    contrast = int((contrast - 0) * (127 - (-127)) / (254 - 0) + (-127))

    if brightness != 0:

        if brightness > 0:

            shadow = brightness

            max = 255

        else:

            shadow = 0
            max = 255 + brightness

        al_pha = (max - shadow) / 255
        ga_mma = shadow

        # The function addWeighted
        # calculates the weighted sum
        # of two arrays
        cal = cv2.addWeighted(img, al_pha,
                              img, 0, ga_mma)

    else:
        cal = img

    if contrast != 0:
        Alpha = float(131 * (contrast + 127)) / (127 * (131 - contrast))
        Gamma = 127 * (1 - Alpha)

        # The function addWeighted calculates
        # the weighted sum of two arrays
        cal = cv2.addWeighted(cal, Alpha,
                              cal, 0, Gamma)

    # putText renders the specified
    # text string in the image.
    cv2.putText(cal, 'B:{},C:{}'.format(brightness,
                                        contrast),
                (10, 30), cv2.FONT_HERSHEY_SIMPLEX,
                1, (0, 0, 255), 2)

    return cal
```

**以下是全部实现:**

## 蟒蛇 3

```py
import cv2

def BrightnessContrast(brightness=0):

    # getTrackbarPos returns the current
    # position of the specified trackbar.
    brightness = cv2.getTrackbarPos('Brightness',
                                    'GEEK')

    contrast = cv2.getTrackbarPos('Contrast',
                                  'GEEK')

    effect = controller(img, brightness,
                        contrast)

    # The function imshow displays an image
    # in the specified window
    cv2.imshow('Effect', effect)

def controller(img, brightness=255,
               contrast=127):

    brightness = int((brightness - 0) * (255 - (-255)) / (510 - 0) + (-255))

    contrast = int((contrast - 0) * (127 - (-127)) / (254 - 0) + (-127))

    if brightness != 0:

        if brightness > 0:

            shadow = brightness

            max = 255

        else:

            shadow = 0
            max = 255 + brightness

        al_pha = (max - shadow) / 255
        ga_mma = shadow

        # The function addWeighted calculates
        # the weighted sum of two arrays
        cal = cv2.addWeighted(img, al_pha,
                              img, 0, ga_mma)

    else:
        cal = img

    if contrast != 0:
        Alpha = float(131 * (contrast + 127)) / (127 * (131 - contrast))
        Gamma = 127 * (1 - Alpha)

        # The function addWeighted calculates
        # the weighted sum of two arrays
        cal = cv2.addWeighted(cal, Alpha,
                              cal, 0, Gamma)

    # putText renders the specified text string in the image.
    cv2.putText(cal, 'B:{},C:{}'.format(brightness,
                                        contrast), (10, 30),
                cv2.FONT_HERSHEY_SIMPLEX, 1, (0, 0, 255), 2)

    return cal

if __name__ == '__main__':
    # The function imread loads an image
    # from the specified file and returns it.
    original = cv2.imread("pic.jpeg")

    # Making another copy of an image.
    img = original.copy()

    # The function namedWindow creates a
    # window that can be used as a placeholder
    # for images.
    cv2.namedWindow('GEEK')

    # The function imshow displays an
    # image in the specified window.
    cv2.imshow('GEEK', original)

    # createTrackbar(trackbarName,
    # windowName, value, count, onChange)
     # Brightness range -255 to 255
    cv2.createTrackbar('Brightness',
                       'GEEK', 255, 2 * 255,
                       BrightnessContrast)

    # Contrast range -127 to 127
    cv2.createTrackbar('Contrast', 'GEEK',
                       127, 2 * 127,
                       BrightnessContrast) 

    BrightnessContrast(0)

# The function waitKey waits for
# a key event infinitely  or for delay
# milliseconds, when it is positive.
cv2.waitKey(0)
```

**输出:**

<video class="wp-video-shortcode" id="video-523776-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20201207182308/e68dedce-8798-4642-b6d7-2280a741a81c.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20201207182308/e68dedce-8798-4642-b6d7-2280a741a81c.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20201207182308/e68dedce-8798-4642-b6d7-2280a741a81c.mp4)</video>