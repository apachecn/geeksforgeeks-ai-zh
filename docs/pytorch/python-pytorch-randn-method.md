# Python–Pytorch randn()方法

> 原文:[https://www.geeksforgeeks.org/python-pytorch-randn-method/](https://www.geeksforgeeks.org/python-pytorch-randn-method/)

PyTorch **torch.randn()** 返回由变量自变量大小(定义输出张量形状的整数序列)定义的张量，包含来自标准正态分布的随机数。

> **语法:** torch.randn(*size，out=None，dtype=None，*布局=torch.strided* ， *device=None* ，requires_grad=False)
> 
> **参数:**
> 
> *   **大小:**定义输出张量大小的整数序列。可以是可变数量的参数或集合，如列表或元组。
> *   **out:** (可选)输出张量。
> *   **数据类型:**(可选)输出张量的数据类型。
> *   **布局:**(可选)返回张量的所需布局。默认值为 torch.strided。
> *   **设备:**(可选)返回张量的所需设备。默认值:如果无，则使用默认张量类型的当前设备(参见[torch . set _ default _ tensor _ type()](https://pytorch.org/docs/master/generated/torch.set_default_tensor_type.html#torch.set_default_tensor_type))。设备将是用于 CPU 张量类型的 CPU 和用于 CUDA 张量类型的当前 CUDA 设备。
> *   **requires_grad:** (可选)如果设置为 true，则在输出张量上自动记录操作。
> 
> **返回:**由标准正态分布的值填充的张量。

让我们借助几个例子来看看这个概念:

**例 1:**

## 计算机编程语言

```py
# import pytorch library
import torch

# create a tensor of size 2 x 4
input_var = torch.randn(2,4)

print (input_var)
```

**输出:**

```py
tensor([[-1.4313, -0.3831, -0.8356, -1.5555],
        [-1.2749, -1.1872, -0.4983,  0.1029]])
```

这将返回一个大小为 2 × 4 的张量，其中填充了标准正态分布的值，即平均值为 0，方差为 1。

**例 2:**

## 蟒蛇 3

```py
# import Pytorch library
import torch

# create a 3-dimensional tensor
# of 4 x 5
input_var =  torch.randn(3, 4, 5,
                     requires_grad = True)
print(input_var)
```

**输出:**

> 张量([[-0.1097，1.6845，0.9375，-1.0515，0.5767]，
> [ 0.1924，-0.7736，-0.7102，-0.2654，0.3118]，
> [-0.5314，0.1924，-1.1629，0.2360，0.8605]，

这将返回一个大小为 3 × 4 × 5 的张量，用随机数填充，并在执行时记录梯度值。
**例 3:**

## 蟒蛇 3

```py
# import Pytorch library
import torch

# error occur
input_var =  torch.randn(3.0, 4.0, 5.0,
                     requires_grad = True)
print(input_var)
```

**输出:**

> 在
> 1 #导入 Pytorch 库
> 2 导入 torch
> —>3 输入= torch.randn(3.0，4.0，5.0，requires_grad=True)
> 4 打印(输入)
> TypeError: randn()收到无效的参数组合–got(float，float，float，requires_grad=bool)，但应为:
> *(ints 大小的元组，*，名称的元组，torch 生成器生成器，名称元组，torch.dtype dtype，torch.layout 布局，torch.device device，bool pin_memory，bool requires _ grad)
> *(ints 大小元组，*，torch。生成器生成器，Tensor out，torch.dtype dtype，torch.layout 布局，torch.device device，bool pin_memory，bool requires _ grad)
> *(ints 大小的元组，* Tensor out，torch.dtype dtype，torch.layout 布局，torch.device device，bool pin_memory，bool requires_grad)

size 参数不能采用浮点数，因此会产生错误。