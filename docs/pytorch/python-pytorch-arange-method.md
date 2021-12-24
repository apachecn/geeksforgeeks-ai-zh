# Python Pytorch 排列()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-arange-method/](https://www.geeksforgeeks.org/python-pytorch-arange-method/)

PyTorch 是脸书开发的开源机器学习库。它用于深度神经网络和自然语言处理。
函数 torch.arrange()返回大小为![\left\lceil \frac{\text{end} - \text{start}}{\text{step}} \right\rceil  ](img/aa6e3b8021416d9de8a388d5ee89ac92.png "Rendered by QuickLaTeX.com")
的一维张量，其值来自从开始以公共差步长获取的区间![[start, end)  ](img/b52b591cf68279b19b25b5e4062bc5eb.png "Rendered by QuickLaTeX.com")。
![out_{i+1} = out_i + step  ](img/fb2d86c30c660e982da0f91cda2357b0.png "Rendered by QuickLaTeX.com")

> **语法**:torch . array(start = 0，end，step=1，out=None)
> **参数** :
> **start** :该组点的起始值。默认值:0。
> **结束**:该组点的结束值
> **步**:每对相邻点之间的间隙。默认值:1。
> **出(张量，可选)**:输出张量
> **返回类型**:一张张量

**代码#1:**

## 蟒蛇 3

```
# Importing the PyTorch library
import torch

# Applying the arrange function and
# storing the resulting tensor in 't'
a = torch.arrange(3)
print("a = ", a)

b = torch.arrange(1, 6)
print("b = ", b)

c = torch.arrange(1, 5, 0.5)
print("c = ", c)
```

**输出:**

```
a =  tensor([0, 1, 2])
b =  tensor([1, 2, 3, 4, 5])
c =  tensor([1.0000, 1.5000, 2.0000, 2.5000, 3.0000, 3.5000, 4.0000, 4.5000])
```

请注意，在与 end 进行比较时，非整数步长会受到浮点舍入误差的影响；为了避免不一致，我们建议在这种情况下在末尾添加一个小ε。