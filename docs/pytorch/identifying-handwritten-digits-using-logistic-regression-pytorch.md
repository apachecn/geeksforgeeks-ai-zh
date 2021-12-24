# 在 PyTorch 中使用逻辑回归识别手写数字

> 原文:[https://www . geesforgeks . org/identificati-手写-数字-使用-逻辑回归-pytorch/](https://www.geeksforgeeks.org/identifying-handwritten-digits-using-logistic-regression-pytorch/)

逻辑回归是一种非常常用的统计方法，它允许我们从一组自变量中预测二进制输出。逻辑回归及其 Python 实现的各种属性已经在本文中介绍过了。现在，我们将了解如何在 PyTorch 中实现这一点，这是一个非常受欢迎的深度学习库，由脸书开发。
现在，我们将看到如何使用 PyTorch 中的逻辑回归对来自 MNIST 数据集的手写数字进行分类。首先，您需要将 PyTorch 安装到 Python 环境中。最简单的方法是使用 pip 或 conda 工具。访问[pytorch.org](https://pytorch.org)并安装您想要使用的 Python 解释器和包管理器版本。
安装了 PyTorch，现在让我们来看看代码。写下下面的三行来导入所需的库函数和对象。

## 蟒蛇 3

```
import torch
import torch.nn as nn
import torchvision.datasets as dsets
import torchvision.transforms as transforms
from torch.autograd import Variable
```

这里， *torch.nn* 模块包含模型所需的代码， *torchvision.datasets* 包含 MNIST 数据集。它包含我们将在这里使用的手写数字数据集。 *torchvision.transforms* 模块包含各种将对象转换为其他对象的方法。在这里，我们将使用它来从图像转换为 PyTorch 张量。此外， *torch.autograd* 模块包含变量类，我们在定义张量时会用到它。
接下来，我们将下载数据集并加载到内存中。

## 蟒蛇 3

```
# MNIST Dataset (Images and Labels)
train_dataset = dsets.MNIST(root ='./data', 
                            train = True, 
                            transform = transforms.ToTensor(),
                            download = True)

test_dataset = dsets.MNIST(root ='./data', 
                           train = False, 
                           transform = transforms.ToTensor())

# Dataset Loader (Input Pipeline)
train_loader = torch.utils.data.DataLoader(dataset = train_dataset, 
                                           batch_size = batch_size, 
                                           shuffle = True)

test_loader = torch.utils.data.DataLoader(dataset = test_dataset, 
                                          batch_size = batch_size, 
                                          shuffle = False)
```

现在，我们将定义我们的超参数。

## 蟒蛇 3

```
# Hyper Parameters 
input_size = 784
num_classes = 10
num_epochs = 5
batch_size = 100
learning_rate = 0.001
```

在我们的数据集中，图像大小是 28*28。因此，我们的输入大小是 784。此外，这里有 10 位数字，因此我们可以有 10 个不同的输出。因此，我们将 num _ classes 设置为 10。此外，我们将在整个数据集上训练五次。最后，我们将分批训练，每批 100 张图片，以防止程序因内存溢出而崩溃。
之后，我们将如下定义我们的模型。在这里，我们将把我们的模型初始化为 *torch.nn.Module* 的子类，然后定义正向传递。在我们正在编写的代码中，softmax 是在每次向前传递期间内部计算的，因此我们不需要在 forward()函数中指定它。

## 蟒蛇 3

```
class LogisticRegression(nn.Module):
    def __init__(self, input_size, num_classes):
        super(LogisticRegression, self).__init__()
        self.linear = nn.Linear(input_size, num_classes)

    def forward(self, x):
        out = self.linear(x)
        return out
```

已经定义了我们的类，现在我们为它实例化一个对象。

## 蟒蛇 3

```
model = LogisticRegression(input_size, num_classes)
```

接下来，我们设置损失函数和优化器。这里，我们将使用交叉熵损失，对于优化器，我们将使用随机梯度下降算法，学习率为 0.001，如上面的超参数中所定义的。

## 蟒蛇 3

```
criterion = nn.CrossEntropyLoss()
optimizer = torch.optim.SGD(model.parameters(), lr = learning_rate)
```

现在，我们开始训练。在这里，我们将执行以下任务:

1.  将所有渐变重置为 0。
2.  向前传球。
3.  计算损失。
4.  执行反向传播。
5.  更新所有重量。

## 蟒蛇 3

```
# Training the Model
for epoch in range(num_epochs):
    for i, (images, labels) in enumerate(train_loader):
        images = Variable(images.view(-1, 28 * 28))
        labels = Variable(labels)

        # Forward + Backward + Optimize
        optimizer.zero_grad()
        outputs = model(images)
        loss = criterion(outputs, labels)
        loss.backward()
        optimizer.step()

        if (i + 1) % 100 == 0:
            print('Epoch: [% d/% d], Step: [% d/% d], Loss: %.4f'
                  % (epoch + 1, num_epochs, i + 1,
                     len(train_dataset) // batch_size, loss.data[0]))
```

最后，我们将使用下面的代码测试这个模型。

## 蟒蛇 3

```
# Test the Model
correct = 0
total = 0
for images, labels in test_loader:
    images = Variable(images.view(-1, 28 * 28))
    outputs = model(images)
    _, predicted = torch.max(outputs.data, 1)
    total += labels.size(0)
    correct += (predicted == labels).sum()

print('Accuracy of the model on the 10000 test images: % d %%' % (
            100 * correct / total))
```

假设您正确执行了所有步骤，您将获得 82%的准确率，这与当今使用特殊类型神经网络架构的最先进模型相去甚远。作为参考，您可以在下面找到本文的全部代码:

## 蟒蛇 3

```
import torch
import torch.nn as nn
import torchvision.datasets as dsets
import torchvision.transforms as transforms
from torch.autograd import Variable

# MNIST Dataset (Images and Labels)
train_dataset = dsets.MNIST(root ='./data',
                            train = True,
                            transform = transforms.ToTensor(),
                            download = True)

test_dataset = dsets.MNIST(root ='./data',
                           train = False,
                           transform = transforms.ToTensor())

# Dataset Loader (Input Pipeline)
train_loader = torch.utils.data.DataLoader(dataset = train_dataset,
                                           batch_size = batch_size,
                                           shuffle = True)

test_loader = torch.utils.data.DataLoader(dataset = test_dataset,
                                          batch_size = batch_size,
                                          shuffle = False)

# Hyper Parameters
input_size = 784
num_classes = 10
num_epochs = 5
batch_size = 100
learning_rate = 0.001

# Model
class LogisticRegression(nn.Module):
    def __init__(self, input_size, num_classes):
        super(LogisticRegression, self).__init__()
        self.linear = nn.Linear(input_size, num_classes)

    def forward(self, x):
        out = self.linear(x)
        return out

model = LogisticRegression(input_size, num_classes)

# Loss and Optimizer
# Softmax is internally computed.
# Set parameters to be updated.
criterion = nn.CrossEntropyLoss()
optimizer = torch.optim.SGD(model.parameters(), lr = learning_rate)

# Training the Model
for epoch in range(num_epochs):
    for i, (images, labels) in enumerate(train_loader):
        images = Variable(images.view(-1, 28 * 28))
        labels = Variable(labels)

        # Forward + Backward + Optimize
        optimizer.zero_grad()
        outputs = model(images)
        loss = criterion(outputs, labels)
        loss.backward()
        optimizer.step()

        if (i + 1) % 100 == 0:
            print('Epoch: [% d/% d], Step: [% d/% d], Loss: %.4f'
                  % (epoch + 1, num_epochs, i + 1,
                     len(train_dataset) // batch_size, loss.data[0]))

# Test the Model
correct = 0
total = 0
for images, labels in test_loader:
    images = Variable(images.view(-1, 28 * 28))
    outputs = model(images)
    _, predicted = torch.max(outputs.data, 1)
    total += labels.size(0)
    correct += (predicted == labels).sum()

print('Accuracy of the model on the 10000 test images: % d %%' % (
            100 * correct / total))
```

**参考文献**:

*   [推土机出发](https://drive.google.com/drive/folders/0B41Zbb4c8HVyUndGdGdJSXd5d3M)
*   [运行库上的云杰](https://github.com/yunjey/pytorch-tutorial)