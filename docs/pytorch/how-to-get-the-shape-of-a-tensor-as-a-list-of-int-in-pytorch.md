# 如何在 Pytorch 中获得作为 int 列表的张量的形状？

> 原文:[https://www . geeksforgeeks . org/如何将张量形状作为 pytorch 中的 int 列表/](https://www.geeksforgeeks.org/how-to-get-the-shape-of-a-tensor-as-a-list-of-int-in-pytorch/)

要在 PyTorch 中获得张量形状列表，我们可以使用两种方法。一个使用 size()方法，另一个使用 PyTorch 中张量的形状属性。在这篇短文中，我们将看到如何使用这两种方法。

### **使用大小()方法:**

size()方法返回自张量的大小。返回值是元组的子类。

## 蟒 3

```
import torch
torch.empty(3, 4, 5).size()
```