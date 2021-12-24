# 如何使用 Python 将图像转换为 NumPy 数组并保存为 CSV 文件？

> 原文:[https://www . geesforgeks . org/如何使用 python 将图像转换为 numpy 数组并将其保存为 csv 文件/](https://www.geeksforgeeks.org/how-to-convert-an-image-to-numpy-array-and-saveit-to-csv-file-using-python/)

让我们看看如何将图像转换成 NumPy 数组，然后用 Python 将该数组保存到 CSV 文件中？首先，我们将学习如何将图像转换为数字数组。将图像转换为数组的方法有很多种，其中很少几种是:

**方法 1:** 使用 **PIL** 和 **NumPy** 库。

我们将使用 PIL。Image.open() 和 [numpy.asarray()](https://www.geeksforgeeks.org/numpy-asarray-in-python/) 。

**示例:**

## 蟒蛇 3

```
# import required libraries
from PIL import Image
import numpy as gfg

# read an image
img = Image.open('geeksforgeeks.jpg')

# convert image object into array
imageToMatrice = gfg.asarray(img)

# printing shape of image
print(imageToMatrice.shape)
```

**输出:**

```
(251, 335, 3)
```

**方法二:**使用 **Matplotlib** 库。

我们将使用[matplotlib . image . imread()](https://www.geeksforgeeks.org/working-with-images-in-python-using-matplotlib/)方法。

**示例:**

## 蟒蛇 3

```
# import library
from matplotlib.image import imread

# read an image
imageToMatrice  = imread('geeksforgeeks.jpg')

# show shape of the image
print(imageToMatrice.shape)
```

**输出:**

```
(251, 335, 3)
```

现在，imageToMatrice 变量包含从给定图像转换后获得的数组。

获得的矩阵的维数取决于图像中存在多少通道:

*   **对于黑白或灰度图像:**只存在一个通道，因此，矩阵的形状为(n，n)，其中 n 代表图像的维度(像素)，矩阵内的值范围为 0 到 255。
*   **对于颜色或 RGB 图像:**它将渲染一个 3 通道的张量，因此矩阵的形状将是(n，n，3)。每个通道都是一个(n，n)矩阵，其中每个条目分别代表图像内实际位置的红色、绿色或蓝色级别。

我们将使用两种方法来做同样的事情，第一种方法使用 numpy 库，第二种方法使用 pandas 库:

**注意:**我们只能在文件中保存 1D 或 2D 矩阵，因此，灰度或黑白图像不会有问题，因为它是 2D 矩阵，但我们需要确保这适用于彩色或 RGB 图像，这是一个 3D 矩阵。

**方法 1:** 使用 **NumPy** 库。

我们将使用 [numpy.savetxt()](https://numpy.org/doc/stable/reference/generated/numpy.savetxt.html) 和 [numpy.loadtxt()。](https://numpy.org/doc/stable/reference/generated/numpy.loadtxt.html#numpy.loadtxt)

**示例:**

## 蟒蛇 3

```
# import required libraries
import numpy as gfg
import matplotlib.image as img

# read an image
imageMat = img.imread('gfg.jpg')
print("Image shape:", imageMat.shape)

# if image is colored (RGB)
if(imageMat.shape[2] == 3):

  # reshape it from 3D matrice to 2D matrice
  imageMat_reshape = imageMat.reshape(imageMat.shape[0],
                                      -1)
  print("Reshaping to 2D array:",
        imageMat_reshape.shape)

# if image is grayscale
else:
  # remain as it is
  imageMat_reshape = imageMat

# saving matrice to .csv file
gfg.savetxt('geek.csv',
            imageMat_reshape)

# retrieving matrice from the .csv file
loaded_2D_mat = gfg.loadtxt('geek.csv')

# reshaping it to 3D matrice
loaded_mat = loaded_2D_mat.reshape(loaded_2D_mat.shape[0],
                                   loaded_2D_mat.shape[1] // imageMat.shape[2],
                                   imageMat.shape[2])

print("Image shape of loaded Image:",
      loaded_mat.shape)

# check if both matrice have same shape or not
if((imageMat == loaded_mat).all()):

  print("\n\nYes",
        "The loaded matrice from CSV file is same as original image matrice")
```

**输出:**

> 图像形状:(251，335，3)
> 整形为 2D 阵列:(251，1005)
> 加载图像的图像形状:(251，335，3)
> 是 CSV 文件中加载的矩阵与原始图像矩阵相同

**方法二:**使用**熊猫**文库。

我们将使用[熊猫。数据框(](https://www.geeksforgeeks.org/python-pandas-dataframe/))和[熊猫。Dataframe()。to_csv()](https://www.geeksforgeeks.org/saving-a-pandas-dataframe-as-a-csv/) 法。

## 蟒蛇 3

```
# import required libraries
import numpy as gfg
import matplotlib.image as img
import pandas as pd

# read an image
imageMat = img.imread('gfg.jpg')
print("Image shape:",
      imageMat.shape)

# if image is colored (RGB)
if(imageMat.shape[2] == 3):

  # reshape it from 3D matrice to 2D matrice
  imageMat_reshape = imageMat.reshape(imageMat.shape[0],
                                      -1)
  print("Reshaping to 2D array:",
        imageMat_reshape.shape)

# if image is grayscale
else:
  # remain as it is
  imageMat_reshape = imageMat

# converting it to dataframe.
mat_df = pd.DataFrame(imageMat_reshape)

# exporting dataframe to CSV file.
mat_df.to_csv('gfgfile.csv',
              header = None,
              index = None)

# retrieving dataframe from CSV file
loaded_df = pd.read_csv('gfgfile.csv',
                        sep = ',',
                        header = None)
# getting matrice values.
loaded_2D_mat = loaded_df.values

# reshaping it to 3D matrice
loaded_mat = loaded_2D_mat.reshape(loaded_2D_mat.shape[0],
                                   loaded_2D_mat.shape[1] // imageMat.shape[2],
                                   imageMat.shape[2])

print("Image shape of loaded Image :",
      loaded_mat.shape)

# check if both matrice have same shape or not
if((imageMat == loaded_mat).all()):
  print("\n\nYes",
        "The loaded matrice from CSV file is same as original image matrice")
```

**输出:**

> 图像形状:(251，335，3)
> 整形为 2D 阵列:(251，1005)
> 加载图像的图像形状:(251，335，3)
> 是 CSV 文件中加载的矩阵与原始图像矩阵相同