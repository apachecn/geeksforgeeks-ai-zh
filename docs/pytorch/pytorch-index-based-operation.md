# py torch–基于索引的操作

> 原文:[https://www . geesforgeks . org/py torch-基于索引的操作/](https://www.geeksforgeeks.org/pytorch-index-based-operation/)

**PyTorch** 是脸书开发的 python 库，用于运行和训练深度学习和机器学习算法。张量是机器或深度学习算法的基本数据结构，为了处理它们，我们执行几个操作，PyTorch 库为此提供了许多功能。

为复制、添加、填充值/张量而在某一特定行或列上处理索引的张量操作被称为基于索引开发的**操作**。PyTorch 中有两种基于索引的操作，一种是原地操作，另一种是异地操作。两者之间的基本区别在于，原位操作直接改变张量的值，而不复制张量的值，而非原位操作则不会。以下是操作:-

1.  索引 _ 添加 _
2.  索引 _ 添加
3.  索引 _ 复制 _
4.  索引 _ 复制
5.  索引 _ 填充 _
6.  索引 _ 填充
7.  索引放入
8.  索引 _ put
9.  索引选择

现在我们用适当的例子讨论每一个函数。

**1。index_add_:** 沿着矩阵中给定的顺序，将给定的张量元素加到自张量上。

**语法:**

```
 index_add_(dim,index,ensor)---> Tensor
```

**参数:**

*   Dim: along which indicator the dimension is added. "0" represents a column and "1" represents a row.
*   Index: Alternative tensor index. It can be *longteng sensor* or *inttensor* .
*   Tensor: Tensor containing the values to be added.

**例 1:** 我们取一个零向量‘x’， *te* 大小为(3，5)的张量和指数张量。沿着行累加结果向量，我们得到输出。

## 蟒 3

```
#importing libraries
import torch

x=torch.zeros(5,5)
te=torch.tensor([[1,3,5,7,9],[1,3,5,7,9],[1,3,5,7,9]],dtype=torch.float32)
index0=torch.tensor([0,2,4])
#adding tensor te to x along row of the given order
x.index_add_(0,index0,te)
```

**输出:**

```
tensor([[1., 3., 5., 7., 9.],
        [0., 0., 0., 0., 0.],
        [1., 3., 5., 7., 9.],
        [0., 0., 0., 0., 0.],
        [1., 3., 5., 7., 9.]])
```

**例 2:**

## 蟒 3

```
#importing libraries
import torch

y=torch.ones(5,5)#unitvector
index2=torch.tensor([0,1,1,1,2])
ten=torch.randn(1,5)
#adding values to y along the column with given order
y.index_add_(1,index2,ten)
```

**输出:**

```
tensor([[0.9460, 0.4762, 1.2219, 1.0000, 1.0000],
        [0.9460, 0.4762, 1.2219, 1.0000, 1.0000],
        [0.9460, 0.4762, 1.2219, 1.0000, 1.0000],
        [0.9460, 0.4762, 1.2219, 1.0000, 1.0000],
        [0.9460, 0.4762, 1.2219, 1.0000, 1.0000]])
```

**2.index_add:** 是上述功能的不合适版本。这会给*自身*张量临时添加一个给定的张量。参数和语法与上面相同。

**例 3:**

## 蟒 3

```
import torch

y=torch.ones(5,5)

index2=torch.tensor([0,1,1,1,2])
ten=torch.randn(1,5)
print("Indexed Matrix:\n",y.index_add(1,index2,ten))
print ("Printing Indexed Matrix again:\n",y)
```

**输出:**

```
Indexed Matrix:
 tensor([[-0.2811, -1.0776,  2.2697,  1.0000,  1.0000],
        [-0.2811, -1.0776,  2.2697,  1.0000,  1.0000],
        [-0.2811, -1.0776,  2.2697,  1.0000,  1.0000],
        [-0.2811, -1.0776,  2.2697,  1.0000,  1.0000],
        [-0.2811, -1.0776,  2.2697,  1.0000,  1.0000]])
Printing Indexed Matrix again:
 tensor([[1., 1., 1., 1., 1.],
        [1., 1., 1., 1., 1.],
        [1., 1., 1., 1., 1.],
        [1., 1., 1., 1., 1.],
        [1., 1., 1., 1., 1.]])
```

**3.index_copy_:** 通过按照“索引”中给出的顺序选择索引，将给定张量的元素复制到输入张量。

**语法:**

```
index_copy_(dim,index,tensor)---> Tensor
```

**参数:**

*   Dim: along which dimension the index is copied. It is in' int' format.
*   Index: An optional tensor index. It can be *int tensor* or [T2】 longtersenter.
*   Tensor: Tensor containing the value to be copied.

**例 4:** 这里“a”的元素被“T1”张量替换，替换顺序在“index3”中给出。

## 蟒 3

```
#importing libraries
import torch

a=torch.ones(4,4)#unit vector
t1=torch.randn(2,4)
index3=torch.tensor([1,3])

#copying elements of t1 ensor to 'a' in given order of index
a.index_copy_(0,index3,t1)
```

**输出:**

```
tensor([[ 1.0000,  1.0000,  1.0000,  1.0000],
        [-0.1918, -1.2089,  0.3229, -0.1831],
        [ 1.0000,  1.0000,  1.0000,  1.0000],
        [ 0.7521,  0.8424, -0.8698, -0.3908]])
```

**示例 5:** 在下面的示例中，我们将收到一个错误。这是因为张量的第三个维度不等于指数的长度。所以我们必须记住张量的第<sup>次</sup>维度必须与索引的长度具有相同的大小。

## 蟒 3

```
#importing libraries
import torch

y=torch.ones(5,5)
index1=torch.tensor([0,1,2,3,4])
te=torch.tensor([[1,3,5,7,9],[1,3,5,7,9],[1,3,5,7,9]],dtype=torch.float32)
y.index_copy_(1,index1,te)
```

**输出:**

```
RuntimeError                              Traceback (most recent call last)
<ipython-input-8-25e4150d5bd7> in <module>
      1 y=torch.ones(5,5)
      2 index1=torch.tensor([0,1,2,3,4])
----> 3 y.index_copy_(1,index1,te)

RuntimeError: index_copy_(): Source/destination tensor must have same slice shapes.
Destination slice shape: 5 at dimension 1 and source slice shape: 3 at dimension 0.
```

**示例 6:** 在本例中，我们将把给定的张量复制到自张量，记住张量的 dim <sup>th</sup> 维度必须与索引的长度具有相同的大小。

## 蟒蛇 3

```
import torch

b=torch.ones(4,4)
t2=torch.randn(4,2)

index4=torch.tensor([0,1])
b.index_copy_(1,index4,t2)
```

**输出:**

```
tensor([[-0.3964, -0.3859,  1.0000,  1.0000],
        [ 2.6910, -0.9394,  1.0000,  1.0000],
        [ 0.3591, -0.2262,  1.0000,  1.0000],
        [ 1.2102, -0.8340,  1.0000,  1.0000]])
```

**4.index_copy:** 这是用给定张量替换输入张量元素的基于错位索引的操作。语法、参数同上。

**5 . index _ fill _:**“Val”值用“x”的元素以及向量“index”中给出的索引顺序填充。

**语法:**

```
index_fill_(dim, index, val) → Tensor
```

**参数:**

*   Dim: The dimension along which it is filled. It is in' int' format.
*   Index: Fill in according to the index order given by this index vector. It can be IntTensor or LongTensor.
*   Val(float): the value to be filled in.

**示例 7:** 在这个示例中，我们将声明一个包含随机元素的张量，然后用‘4’以及给定的索引填充它。

## 蟒 3

```
#importing libraries
import torch
c=torch.randn(4,4)

index5=torch.tensor([0,2])

#filling 4 within the elements of the tensor 'c' along the indices 0,2
c.index_fill_(0,index5,4)
print(c)
```

**输出:**

```
 tensor([[ 4.0000,  4.0000,  4.0000,  4.0000],
        [ 0.4762,  0.0056,  0.3258,  1.1345],
        [ 4.0000,  4.0000,  4.0000,  4.0000],
        [-0.1490, -0.6543,  0.9755,  1.8087]])
```

**示例 8:** 类似地，我们对列执行填充操作。

## 蟒 3

```
d=torch.randn(5,5)

d.index_fill(1,index5,2)
print(d)
```

**输出:**

```
 tensor([[ 0.5978, -1.2461, -0.8794, -1.0175,  0.8938],
        [-0.6374,  1.0848,  0.1291,  0.6658,  0.3081],
        [-0.9686, -0.8212, -0.5223, -0.3208, -1.7718],
        [-0.1153, -1.2552, -0.4119, -1.1293,  0.2266],
        [ 1.2610,  0.2618, -1.5528,  0.7805,  1.3730]])
```

**6。index_fill:** 这是基于索引的不合适的操作，用“val”填充张量元素。语法、参数同上。

**7.index_put_:** 该操作使用给定“索引”的索引将“val”的值放入自张量。

**语法:**

```
index_put_(indices, values, accumulate=False) → Tensor
```

**参数:**

*   Index: It is the tuple of Longtengsen, which is used to index yourself.
*   Value: Tensor with the value to be put into the target.
*   Accumulate: whether to accumulate.

**例 9:** 这里我们取目标向量，替换

## 中提到的值张量的值

```
#importing libraries
import torch

target=torch.zeros([4,4])
indices = torch.LongTensor([[0,1],[1,2],[3,1],[1,0]])#indices to which values to be put
value = torch.ones(indices.shape[0])
#tuple of the index tensor is passed along with the value
target.index_put_(tuple(indices.t()), value)
```

**输出:**

```
tensor([[0., 1., 0., 0.],
       [1., 0., 1., 0.],
       [0., 0., 0., 0.],
       [0., 1., 0., 0.]])
```

**注意:**我们必须进行指数张量的转置，否则会出现错误。

**示例 10:** 在本例中，我们将累加函数保持为 true，这意味着值中的元素被添加到目标中。

## 蟒 3

```
e=torch.ones([4,4])
indices2=torch.LongTensor([[0,1],[0,1],[2,1]])
value2=torch.zeros(indices2.shape[0])

e.index_put_(tuple(indices2.t()),value2,accumulate=True)
```

```
Output:
tensor([[1., 1., 1., 1.],
       [1., 1., 1., 1.],
       [1., 1., 1., 1.],
       [1., 1., 1., 1.]])
```

**8。index_fill:** 这是 *index_fill_* 的不合适版本。语法、参数同上。

**9。** **index_select:** 通过从目标张量中进行选择，可以返回一个带有上述索引的张量。

**语法:**

```
torch.index_select(input, dim, index, out=None) 
```

**参数:**

*   Input (Tensor): Tensor from which the index will be selected.
*   Dimension (int): The dimension selected along it.
*   Index: An index containing an index.

**示例 11:** 我们沿着 dim=0(即行)选取张量‘m’的 0，1 个索引，并打印输出。

## 蟒 3

```
#importing libraries
import torch

m=torch.randn(3,4)
print('Original matrix:\n',m)
indices=torch.tensor([0,1])
print("Indexed Matrix:\n",torch.index_select(m, 0, indices))
```

**输出:**

```
Original matrix:
 tensor([[ 0.2008, -0.2637,  2.1216, -0.2892],
        [-0.4059, -1.6054, -2.5022, -0.2912],
        [-0.3246,  0.4751, -0.1018, -0.6707]])
Indexed Matrix:
 tensor([[ 0.2008, -0.2637,  2.1216, -0.2892],
        [-0.4059, -1.6054, -2.5022, -0.2912]])
```

**参考:**T2】https://pytorch.org/docs/stable/tensors.html