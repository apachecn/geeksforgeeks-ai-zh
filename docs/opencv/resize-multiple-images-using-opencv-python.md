# 使用 OpenCV-Python 调整多个图像的大小

> 原文:[https://www . geesforgeks . org/resize-multi-images-use-opencv-python/](https://www.geeksforgeeks.org/resize-multiple-images-using-opencv-python/)

在本文中，我们将使用 OpenCV 库编写一个 python 脚本来调整多个图像的大小，并将它们保存为图像文件。调整图像大小指的是图像的增长。测量在使用多幅图像和机器学习应用中效果最好。它有助于减少图像的像素数量，并且具有几个好处，例如，它可以减少神经网络训练时间，因为图像中的像素数量大大增加了输入节点的数量，这也提高了模型的难度。

**进场:**

*   首先，将所需的库加载到 Python 文件中(argparse、OpenCV 等)。).
*   我们使用 [**argparse()**](https://www.geeksforgeeks.org/python-key-value-pair-using-argparse/) 函数来获取我们需要对其执行大小调整的图像目录的路径。
*   用于循环迭代目录中的每个**图像**。
*   使用 [**cv2.imread()**](https://www.geeksforgeeks.org/python-opencv-cv2-imread-method/) 函数加载图像中的一个变量。
*   定义调整大小的比例，并设置计算的高度和宽度。
*   使用 [**cv2.resize()**](https://www.geeksforgeeks.org/image-resizing-using-opencv-python/) 功能调整图像大小。
*   使用 [**cv2.imwrite()**](https://www.geeksforgeeks.org/python-opencv-cv2-imwrite-method/) 功能将输出文件放入输出文件夹中。

“图像”文件夹中的所有图像都将被调整大小，并保存在输出文件夹中。

**下面是实现:**

## 蟒蛇 3

```
# Required Libraries
import cv2
import numpy as np
from os import listdir
from os.path import isfile, join
from pathlib import Path
import argparse
import numpy

# Argument parsing variable declared
ap = argparse.ArgumentParser()

ap.add_argument("-i", "--image",
                required=True,
                help="Path to folder")

args = vars(ap.parse_args())

# Find all the images in the provided images folder
mypath = args["image"]
onlyfiles = [f for f in listdir(mypath) if isfile(join(mypath, f))]
images = numpy.empty(len(onlyfiles), dtype=object)

# Iterate through every image
# and resize all the images.
for n in range(0, len(onlyfiles)):

    path = join(mypath, onlyfiles[n])
    images[n] = cv2.imread(join(mypath, onlyfiles[n]),
                           cv2.IMREAD_UNCHANGED)

    # Load the image in img variable
    img = cv2.imread(path, 1)

    # Define a resizing Scale
    # To declare how much to resize
    resize_scaling = 50
    resize_width = int(img.shape[1] * resize_scaling/100)
    resize_hieght = int(img.shape[0] * resize_scaling/100)
    resized_dimensions = (resize_width, resize_hieght)

    # Create resized image using the calculated dimensions
    resized_image = cv2.resize(img, resized_dimensions,
                               interpolation=cv2.INTER_AREA)

    # Save the image in Output Folder
    cv2.imwrite(
      'output/' + str(resize_width) + str(resize_hieght) + str(n) + '_resized.jpg', resized_image)

print("Images resized Successfully")
```

在保存 Python 脚本的文件夹中打开终端，并键入以下命令。

```
python resize.py --image path/to/images/folder/
```

**输出:**

<video class="wp-video-shortcode" id="video-574029-1" width="640" height="360" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20210316174229/resize.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20210316174229/resize.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20210316174229/resize.mp4)</video>