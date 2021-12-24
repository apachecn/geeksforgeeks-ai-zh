# 【PyTorch 和 TensorFlow 的区别

> 原文:[https://www . geeksforgeeks . org/py torch-and-tensorflow 之差/](https://www.geeksforgeeks.org/difference-between-pytorch-and-tensorflow/)

有各种各样的深度学习图书馆，但最著名的两个图书馆是 PyTorch 和 Tensorflow。虽然两者都是开源库，但有时很难弄清楚两者之间的区别。它们被广泛用于商业代码和学术研究。

### PyTorch：

这是一个用于机器学习的开源库。它由脸书开发，并于 2016 年首次向公众发布。这是必须的，这意味着它会立即运行，用户可以在编写完整代码之前检查它是否工作。我们可以编写一部分代码并实时检查，它是内置的基于 python 的实现，作为深度学习平台提供兼容性。它因其用户友好的界面而迅速获得用户，这使得 Tensorflow 团队在 Tensorflow 2.0 中获得了其受欢迎的功能。

### [张量流：](https://www.geeksforgeeks.org/introduction-to-tensorflow/)

就像 PyTorch 一样，它也是一个用于机器学习的开源库。它由谷歌开发，于 2015 年发布。它的名字本身就表达了如何对数据执行和组织任务。生产和研究是张量流的主要用途。神经网络大多使用 Tensorflow 来开发机器学习应用。

### PyTorch V/S TensorFlow

<figure class="table">

| S.No | 皮托奇 | TensorFlow |
| --- | --- | --- |
| one | 它是由脸书开发的 | 它是由谷歌开发的 |
| Two | 它是用 Torch 库制作的。 | 它被部署在一个 python 库——antio 上 |
| three | 它基于动态图的概念 | 它相信静态图形概念 |
| four | 与 Tensorflow 相比，Pytorch 的功能更少。 | 它具有更高级别的功能，并提供了广泛的工作选择。 |
| five | Pytorch 使用简单的 API，节省了整个模型的重量。 | 它的一个主要好处是整个图形可以保存为协议缓冲区。 |
| six | 相对而言，它对部署的支持较少。 | 与 Pytorch 相比，它更支持嵌入式和移动部署 |
| seven | 它有一个较小的社区。 | 它有一个更大的社区。 |
| eight | 很容易学习和理解。 | 这是比较难学的 |
| nine | 它要求用户将所有内容存储到设备中。 | 默认设置在张量流中定义明确。 |
| Ten | 它有一个动态的计算过程。 | 它需要使用调试器工具。 |
| Eleven | 它的一些特性或库有: *PYRO* 、 *Horizon* 、 *CheXNet* 等。 | 它的一些功能或库有:*十四行诗*、*路德维希*、*洋红色*等。 |

</figure>

## 结论

不能说一个库好一个库坏，两者都是非常有用的框架，都是大规模使用的。两者都是机器学习库，用于完成各种任务。Tensorflow 是一个有用的工具，具有调试功能和可视化，它还将图形保存为协议缓冲区。另一方面，由于 python 的友好使用，Pytorch 仍在获得势头并吸引 python 开发人员。简而言之，Tensorflow 用于更快地实现自动化，并制造人工智能相关产品，而更注重研究的开发人员更喜欢使用 Pytorch。