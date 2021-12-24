# 使用 OpenCV 的隐形斗篷| Python 项目

> 原文:[https://www . geesforgeks . org/隐形-斗篷-使用-opencv-python-project/](https://www.geeksforgeeks.org/invisible-cloak-using-opencv-python-project/)

你看过《哈利·波特的隐形斗篷》吗；很棒吗？你曾经想要穿那件斗篷吗？如果是！！然后在这篇文章中，我们将建造哈利·波特用来隐形的斗篷。是的，我们不是以真实的方式构建它，但这一切都是关于图形欺骗。

在这篇文章中，我们将学习如何在 **OpenCV** 中使用简单的计算机视觉技术来创建我们自己的“隐身衣”。在这里，我们用 Python 编写了这段代码，因为它为构建这个程序提供了详尽而充足的库。

在这里，我们将使用名为 ***颜色检测和分割*** 的图像处理技术来创造这种神奇的体验。为了运行这段代码，您需要一个名为“`video.mp4`”的 mp4 视频。你必须有一块相同颜色的布，并且在那块布上看不到其他颜色。我们拿着红布。如果你使用其他布料，代码将保持不变，但会有细微的变化。

**为什么是红色？绿色是我最喜欢的？**
当然，我们可以用绿色，红色不是魔术师的颜色吗？撇开笑话不谈，像绿色或蓝色这样的颜色也可以在稍微修改代码的情况下正常工作。
该技术与**绿色筛选**相反。在绿色筛选，我们删除背景，但这里我们将删除前景帧。让我们开始我们的代码。

**算法:**

> 1.捕捉并存储背景帧[这将持续几秒钟]
> 2。使用颜色检测和分割算法检测红色布料。
> 3。通过生成一个遮罩来分割红色布料。【用于法典】
> 4。生成最终的增强输出，以创造神奇的效果。[video.mp4]

**下面是代码:**

```
import cv2
import numpy as np
import time

# replace the red pixels ( or undesired area ) with
# background pixels to generate the invisibility feature.

## 1\. Hue: This channel encodes color information. Hue can be
# thought of an angle where 0 degree corresponds to the red color, 
# 120 degrees corresponds to the green color, and 240 degrees 
# corresponds to the blue color.

## 2\. Saturation: This channel encodes the intensity/purity of color.
# For example, pink is less saturated than red.

## 3\. Value: This channel encodes the brightness of color.
# Shading and gloss components of an image appear in this 
# channel reading the videocapture video  

# in order to check the cv2 version
print(cv2.__version__)   

# taking video.mp4 as input.
# Make your path according to your needs 
capture_video = cv2.VideoCapture("video.mp4")

# give the camera to warm up
time.sleep(1) 
count = 0 
background = 0 

# capturing the background in range of 60
# you should have video that have some seconds
# dedicated to background frame so that it 
# could easily save the background image
for i in range(60):
    return_val, background = capture_video.read()
    if return_val == False :
        continue 

background = np.flip(background, axis = 1) # flipping of the frame 

# we are reading from video 
while (capture_video.isOpened()):
    return_val, img = capture_video.read()
    if not return_val :
        break 
    count = count + 1
    img = np.flip(img, axis = 1)

    # convert the image - BGR to HSV
    # as we focused on detection of red color 

    # converting BGR to HSV for better 
    # detection or you can convert it to gray
    hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV) 

    #-------------------------------------BLOCK----------------------------#
    # ranges should be carefully chosen
    # setting the lower and upper range for mask1
    lower_red = np.array([100, 40, 40])       
    upper_red = np.array([100, 255, 255])
    mask1 = cv2.inRange(hsv, lower_red, upper_red)
    # setting the lower and upper range for mask2 
    lower_red = np.array([155, 40, 40])
    upper_red = np.array([180, 255, 255])
    mask2 = cv2.inRange(hsv, lower_red, upper_red)
    #----------------------------------------------------------------------#

    # the above block of code could be replaced with
    # some other code depending upon the color of your cloth 
    mask1 = mask1 + mask2

    # Refining the mask corresponding to the detected red color
    mask1 = cv2.morphologyEx(mask1, cv2.MORPH_OPEN, np.ones((3, 3),
                                         np.uint8), iterations = 2)
    mask1 = cv2.dilate(mask1, np.ones((3, 3), np.uint8), iterations = 1)
    mask2 = cv2.bitwise_not(mask1)

    # Generating the final output
    res1 = cv2.bitwise_and(background, background, mask = mask1)
    res2 = cv2.bitwise_and(img, img, mask = mask2)
    final_output = cv2.addWeighted(res1, 1, res2, 1, 0)

    cv2.imshow("INVISIBLE MAN", final_output)
    k = cv2.waitKey(10)
    if k == 27:
        break
```

**输出:**

您可以在 github 项目资源库上查看源代码，获取输入视频和更多详细信息–[此处](https://github.com/AdityaAtri/invisible_man.git)

**参考:**[http://datasciencenthusiast.com/?p=71](http://datasciencenthusiast.com/?p=71)