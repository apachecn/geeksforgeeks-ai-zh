# 使用 PyTorch 的线性回归

> 原文:[https://www . geesforgeks . org/线性回归-使用-pytorch/](https://www.geeksforgeeks.org/linear-regression-using-pytorch/)

线性回归是一种非常常用的统计方法，它允许我们确定和研究两个连续变量之间的关系。线性回归的各种属性及其 Python 实现已经在本文中介绍过了。现在，我们将了解如何在 PyTorch 中实现这一点，这是一个非常受欢迎的深度学习库，由脸书开发。
首先，您需要将 PyTorch 安装到 Python 环境中。最简单的方法是使用 pip 或 conda 工具。访问[pytorch.org](https://pytorch.org)并安装您想要使用的 Python 解释器和包管理器版本。

## 蟒蛇 3

```py
# We can run this Python code on a Jupyter notebook
# to automatically install the correct version of
# PyTorch.

# http://pytorch.org / from os import path
from wheel.pep425tags import get_abbr_impl, get_impl_ver, get_abi_tag
platform = '{}{}-{}'.format(get_abbr_impl(), get_impl_ver(), get_abi_tag())

accelerator = 'cu80' if path.exists('/opt / bin / nvidia-smi') else 'cpu'

! pip install -q http://download.pytorch.org / whl/{accelerator}/torch-1.3.1.post4-{platform}-linux_x86_64.whl torchvision
```

安装了 PyTorch 之后，现在让我们看一下代码。
写出下面给出的两行，导入必要的库函数和对象。

## 蟒蛇 3

```py
import torch
from torch.autograd import Variable
```

我们还定义了一些数据，并将其分配给变量 *x_data* 和 *y_data* ，如下所示:

## 蟒蛇 3

```py
x_data = Variable(torch.Tensor([[1.0], [2.0], [3.0]]))
y_data = Variable(torch.Tensor([[2.0], [4.0], [6.0]]))
```

这里， *x_data* 是我们的自变量， *y_data* 是我们的因变量。这将是我们目前的数据集。接下来，我们需要定义我们的模型。定义我们的模型有两个主要步骤。他们是:

1.  初始化我们的模型。
2.  声明向前传递。

我们使用下面给出的类:

## 蟒蛇 3

```py
class LinearRegressionModel(torch.nn.Module):

    def __init__(self):
        super(LinearRegressionModel, self).__init__()
        self.linear = torch.nn.Linear(1, 1)  # One in and one out

    def forward(self, x):
        y_pred = self.linear(x)
        return y_pred
```

可以看到，我们的*模型*类是 *torch.nn.module* 的子类。此外，由于这里只有一个输入和一个输出，我们使用输入和输出维度都为 1 的线性模型。
接下来，我们创建这个模型的一个对象。

## 蟒蛇 3

```py
# our model
our_model = LinearRegressionModel()
```