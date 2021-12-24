# Python OpenCV–imdecode()函数

> 原文:[https://www . geesforgeks . org/python-opencv-im decode-function/](https://www.geeksforgeeks.org/python-opencv-imdecode-function/)

**Python cv2.imdecode()** **函数**用于从内存缓存中读取图像数据，并将其转换为图像格式。这通常用于从互联网有效地加载图像。

> **语法:** cv2.imdecode(buf，flags)
> 
> **参数:**
> 
> *   **buf–**是以字节为单位接收的图像数据
> *   **标志–**指定读取图像的方式。它的默认值是 cv2。IMREAD_COLOR
> 
> **返回:**图像数组

**注意:**如果给定的 buf 不是图像数据，则返回空值。

**例 1:**

## 蟒蛇 3

```py
#import modules
import numpy as np
import urllib.request
import cv2

# read the image url
url = 'https://media.geeksforgeeks.org/wp-content/uploads/20211003151646/geeks14.png'

with urllib.request.urlopen(url) as resp:

    # read image as an numpy array
    image = np.asarray(bytearray(resp.read()), dtype="uint8")

    # use imdecode function
    image = cv2.imdecode(image, cv2.IMREAD_COLOR)

    # display image
    cv2.imwrite("result.jpg", image)
```

**输出:**

![](img/20648dd36df67499fbbaf373412b93d0.png)

**例 2:** 如果需要灰度，那么 0 可以作为标志。

## 蟒蛇 3

```py
# import necessary modules
import numpy as np
import urllib.request
import cv2

# read image url
url = 'https://media.geeksforgeeks.org/wp-content/uploads/20211003151646/geeks14.png'

with urllib.request.urlopen(url) as resp:

    # convert to numpy array
    image = np.asarray(bytearray(resp.read()), dtype="uint8")

    # 0 is used for grayscale image
    image = cv2.imdecode(image, 0)

    # display image
    cv2.imwrite("result.jpg", image)
```