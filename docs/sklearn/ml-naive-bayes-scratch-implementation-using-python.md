# ML |使用 Python 的朴素贝叶斯 Scratch 实现

> 原文:[https://www . geesforgeks . org/ml-朴素贝叶斯-scratch-实现-使用-python/](https://www.geeksforgeeks.org/ml-naive-bayes-scratch-implementation-using-python/)

**朴素贝叶斯简介**
朴素贝叶斯是基于**贝叶斯定理**的非常简单和强大的分类算法之一，假设预测器之间是独立的。朴素贝叶斯分类器假设类中某个特征的存在与任何其他特征无关。朴素贝叶斯是一种用于二类和多类分类问题的分类算法。
**贝叶斯定理**

*   基于可能与事件相关的条件的先验知识，贝叶斯定理描述了事件的概率
*   条件概率可以这样找到
*   假设我们有一个假设( *H* )和证据( *E* )，
    根据贝叶斯定理，在得到表示为 *P(H)* 的证据之前假设的概率和得到表示为 *P(H|E)* 的证据之后假设的概率之间的关系是:

```py
*P(H|E) = P(E|H)*P(H)/P(E)*
```

*   **先验概率** = *P(H)* 为获得证据前的概率
    T5】后验概率 = *P(H|E)* 为获得证据后的概率
*   一般情况下，

```py
*P(class|data) = (P(data|class) * P(class)) / P(data)*
```

**贝叶斯定理示例**
假设我们必须找到随机选择的牌成为王的概率，假设它是一张脸牌。
一副牌中有 *4* 个王，暗示着 *P(王)= 4/52*
由于所有的王都是面牌所以 *P(面|王)= 1*
一套 *13 张牌中有 *3* 张面牌*总共有 *4 套*所以 *P(面)= 12/52【T15*

```py
*P(King|face) = P(face|king)*P(king)/P(face) = 1/3*
```

[在此下载数据集](https://gist.github.com/ktisha/c21e73a1bd1700294ef790c56c8aec1f)

**代码:使用 Python 从头开始实现朴素贝叶斯算法**

## 蟒蛇 3

```py
# Importing library
import math
import random
import csv

# the categorical class names are changed to numberic data
# eg: yes and no encoded to 1 and 0
def encode_class(mydata):
    classes = []
    for i in range(len(mydata)):
        if mydata[i][-1] not in classes:
            classes.append(mydata[i][-1])
    for i in range(len(classes)):
        for j in range(len(mydata)):
            if mydata[j][-1] == classes[i]:
                mydata[j][-1] = i
    return mydata           

# Splitting the data
def splitting(mydata, ratio):
    train_num = int(len(mydata) * ratio)
    train = []
    # initially testset will have all the dataset
    test = list(mydata)
    while len(train) < train_num:
        # index generated randomly from range 0
        # to length of testset
        index = random.randrange(len(test))
        # from testset, pop data rows and put it in train
        train.append(test.pop(index))
    return train, test

# Group the data rows under each class yes or
# no in dictionary eg: dict[yes] and dict[no]
def groupUnderClass(mydata):
      dict = {}
      for i in range(len(mydata)):
          if (mydata[i][-1] not in dict):
              dict[mydata[i][-1]] = []
          dict[mydata[i][-1]].append(mydata[i])
      return dict

# Calculating Mean
def mean(numbers):
    return sum(numbers) / float(len(numbers))

# Calculating Standard Deviation
def std_dev(numbers):
    avg = mean(numbers)
    variance = sum([pow(x - avg, 2) for x in numbers]) / float(len(numbers) - 1)
    return math.sqrt(variance)

def MeanAndStdDev(mydata):
    info = [(mean(attribute), std_dev(attribute)) for attribute in zip(*mydata)]
    # eg: list = [ [a, b, c], [m, n, o], [x, y, z]]
    # here mean of 1st attribute =(a + m+x), mean of 2nd attribute = (b + n+y)/3
    # delete summaries of last class
    del info[-1]
    return info

# find Mean and Standard Deviation under each class
def MeanAndStdDevForClass(mydata):
    info = {}
    dict = groupUnderClass(mydata)
    for classValue, instances in dict.items():
        info[classValue] = MeanAndStdDev(instances)
    return info

# Calculate Gaussian Probability Density Function
def calculateGaussianProbability(x, mean, stdev):
    expo = math.exp(-(math.pow(x - mean, 2) / (2 * math.pow(stdev, 2))))
    return (1 / (math.sqrt(2 * math.pi) * stdev)) * expo

# Calculate Class Probabilities
def calculateClassProbabilities(info, test):
    probabilities = {}
    for classValue, classSummaries in info.items():
        probabilities[classValue] = 1
        for i in range(len(classSummaries)):
            mean, std_dev = classSummaries[i]
            x = test[i]
            probabilities[classValue] *= calculateGaussianProbability(x, mean, std_dev)
    return probabilities

# Make prediction - highest probability is the prediction
def predict(info, test):
    probabilities = calculateClassProbabilities(info, test)
    bestLabel, bestProb = None, -1
    for classValue, probability in probabilities.items():
        if bestLabel is None or probability > bestProb:
            bestProb = probability
            bestLabel = classValue
    return bestLabel

# returns predictions for a set of examples
def getPredictions(info, test):
    predictions = []
    for i in range(len(test)):
        result = predict(info, test[i])
        predictions.append(result)
    return predictions

# Accuracy score
def accuracy_rate(test, predictions):
    correct = 0
    for i in range(len(test)):
        if test[i][-1] == predictions[i]:
            correct += 1
    return (correct / float(len(test))) * 100.0

# driver code

# add the data path in your system
filename = r'E:\user\MACHINE LEARNING\machine learning algos\Naive bayes\filedata.csv'

# load the file and store it in mydata list
mydata = csv.reader(open(filename, "rt"))
mydata = list(mydata)
mydata = encode_class(mydata)
for i in range(len(mydata)):
    mydata[i] = [float(x) for x in mydata[i]]

# split ratio = 0.7
# 70% of data is training data and 30% is test data used for testing
ratio = 0.7
train_data, test_data = splitting(mydata, ratio)
print('Total number of examples are: ', len(mydata))
print('Out of these, training examples are: ', len(train_data))
print("Test examples are: ", len(test_data))

# prepare model
info = MeanAndStdDevForClass(train_data)

# test model
predictions = getPredictions(info, test_data)
accuracy = accuracy_rate(test_data, predictions)
print("Accuracy of your model is: ", accuracy)
```

**输出:**

```py
Total number of examples are: 200
Out of these, training examples are: 140
Test examples are: 60
Accuracy of your model is: 71.2376788
```