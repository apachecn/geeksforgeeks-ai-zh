# py torch 中的二维张量

> 原文:[https://www . geesforgeks . org/二维-tensors-in-pytorch/](https://www.geeksforgeeks.org/two-dimensional-tensors-in-pytorch/)

**PyTorch** 是脸书开发的一个 python 库，用来运行和训练机器学习和深度学习模型。在 PyTorch 中，一切都基于张量运算。

**二维张量**只不过是具有特定数据类型的二维矩阵或向量，由 n 行 n 列组成。

**表示:**二维张量具有以下表示。

```py
torch.tensor([[3,2,1]
               [6,5,4]
               [9,8,7]]) 
```

### **二维张量的产生:**

我们可以通过传递数据列表来创建张量，或者用 *randn* 随机生成值，也可以用*array*函数在一定间隔内取值。

**示例:**

## 蟒蛇 3

```py
# importing library
import torch

 # list of data in 1d form
y=torch.tensor([2.5,5.6,8.1,4.6,3.2,6.7])

# reshaping it to 2d
x=y.view(2,3)
print('First tensor is: {}'.format(x),'\nSize of it:{}'.format(x.size()),
      '\ntype of tensor:{}\n'.format(x.dtype))

# random values of size 2X2
x2=torch.randn(2,2)
print('Second tensor is: {}'.format(x2),'\nSize of it:{}'.format(x2.size()),
      '\ntype of tensor:{}\n'.format(x2.dtype))

# integers within this range
y1=torch.arrange(0,8)
x1=y1.view(4,2)
print('Third tensor is: {}'.format(x1),'\nSize of it:{}'.format(x1.size()),
      '\ntype of tensor:{}'.format(x1.dtype))
```

**输出:**

```py
First tensor is: tensor([[2.5000, 5.6000, 8.1000],
        [4.6000, 3.2000, 6.7000]]) 
Size of it:torch.Size([2, 3]) 
type of tensor:torch.float32

Second tensor is: tensor([[1.2532, 1.3558],
        [0.5496, 1.7828]]) 
Size of it:torch.Size([2, 2]) 
type of tensor:torch.float32

Third tensor is: tensor([[0, 1],
        [2, 3],
        [4, 5],
        [6, 7]]) 
Size of it:torch.Size([4, 2]) 
type of tensor:torch.int64
```

### **张量相乘**T2】

张量的乘法可以是逐元素乘法(将每个元素乘以元素)或度量乘法(将相应的列乘以相应的行)。在深度学习中，我们使用度量与所需大小相乘的概念。

**示例:**

## 蟒蛇 3

```py
import torch

a=torch.arrange(0,9)

# reshaping data
a=mat_a.view(3,3)

b=torch.arrange(0,9)

# reshaping data
b=mat_b.view(3,3)

mat_mul=torch.matmul(mat_a,mat_b)
elem_mul=torch.mul(mat_a,mat_b)
print('Tensor after elementwise multiplication:{}'.format(elem_mul),
      '\n Tensor after matrix multiplication: {}'.format(mat_mul))
```

**输出:**

```py
Tensor after elementwise multiplication:tensor([[ 0,  1,  4],
        [ 9, 16, 25],
        [36, 49, 64]]) 
 Tensor after matrix multiplication: tensor([[ 15,  18,  21],
        [ 42,  54,  66],
        [ 69,  90, 111]])
```

### **访问元素:**

在张量中，我们可以通过切片访问任何列或行的值，对于特定的元素，我们使用索引。为了仅获得张量中的值，我们使用**。项目()。**

**示例:**

## 蟒蛇 3

```py
import torch

# defining the tensor
x4=torch.arrange(4,13)
y4=x4.view(3,3)

# slicing is performed
print('First column has the values:{}'.format(y4[:,0]))
print('Second row has the values:{}'.format(y4[1,:]))

# indexing a  particular element
print('Data at the index 1,2 :{}'.format(y4[1][2]))
```

**输出:**

```py
First column has the values:tensor([ 4,  7, 10])
Second row has the values:tensor([7, 8, 9])
Data at the index 1,2 :9
```

### 三维**张量:**

三维张量只不过是秩为 3 的矩阵或向量。三维张量是通过在二维向量的层次上添加另一个带括号的层次来创建的。在图像处理中，我们使用具有 3 维彩色像素的 RGB 图像。

## 蟒蛇 3

```py
import torch

# tensor with 3 dimension
x=torch.tensor([[[11,12,13],[14,15,16],[17,18,19]]])

# 1d tensor
x1=torch.arrange(10,19)

# reshaping it to 3d tensor
x1=x1.view(1,3,3)
print(x,'\n',x1)
```

**输出:**

```py
tensor([[[11, 12, 13],
         [14, 15, 16],
         [17, 18, 19]]]) 
 tensor([[[10, 11, 12],
         [13, 14, 15],
         [16, 17, 18]]])

```