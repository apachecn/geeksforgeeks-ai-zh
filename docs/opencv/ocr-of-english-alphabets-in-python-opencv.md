# Python OpenCV 中英文字母的 OCR

> 原文:[https://www . geesforgeks . org/ocr-of-English-alphabets-in-python-opencv/](https://www.geeksforgeeks.org/ocr-of-english-alphabets-in-python-opencv/)

**OCR** 代表**光学字符识别**是一种用于识别数字、字母、符号等字符的计算机视觉技术。这些字符在日常生活中很常见，我们可以根据自己的需求进行字符识别。我们将使用 OpenCV 实现英文字母的光学字符识别。这里我们将使用用于分类的 KNN 算法。

**注意:**你可以在这里找到数据[数据](https://github.com/opencv/opencv/blob/master/samples/data/letter-recognition.data)我们会对其进行 OCR。

有 20000 行数据包含 17 列，其中第一列代表字母表，其余 16 列将代表其不同的特征。我们必须通过将字母转换成 ASCII 字符来处理数据。为了执行分类，我们将使用 10000 行作为训练数据，10000 行作为测试数据。

下面是实现。

## 蟒 3

```
#Import the libraries
import cv2 as cv
import numpy as np

# Read data and use converters
# to convert the alphabets to
# Numeric value.
data= np.loadtxt('letter-recognition',
                 dtype= 'float32',
                 delimiter = ',',
                 converters= {0: lambda ch: ord(ch)-ord('A')})

# split the data into train_data
# and test_data
train_data, test_data = np.vsplit(data,2)

# split train_data and test_data
# to features and responses.
responses, training = np.hsplit(train_data,[1])
classes, testing = np.hsplit(test_data,[1])

# Create the knn classifier
knn = cv.ml.KNearest_create()
knn.train(training, cv.ml.ROW_SAMPLE, responses)

# Obtain the results of the classifier
# determine the number of neighbors.
ret, Output, neighbours,
distance = knn.findNearest(testing, k=7)

# Match the Output to find the
# number of wrong predictions.
correct_OP = np.count_nonzero(Output == classes)

#calculate accuracy and display it.
accuracy = (correct_OP*100.0)/(10000)
print( accuracy )
```

**输出**

```
92.82
```