# NLP |用 execnet 进行并行列表处理

> 原文:[https://www . geesforgeks . org/NLP-parallel-list-processing-with-exec net/](https://www.geeksforgeeks.org/nlp-parallel-list-processing-with-execnet/)

本文介绍了一种使用 execnet 并行处理列表的模式。这是一种函数模式，用于将列表中的每个元素映射到一个新值，使用 execnet 并行进行映射。

在下面给出的代码中，整数被简单地加倍，任何纯计算都可以被执行。给定的是模块，它将由 execnet 执行。它接收(I，arg)的二元组，假设 arg 是一个数字，然后发送回来(I，arg*2)。

**代码:**

```
if __name__ == '__channelexec__':
    for (i, arg) in channel:
        channel.send((i, arg * 2))
```

要使用此模块将列表中的每个元素加倍，请导入 **plists** 模块，并使用 remote_double 模块调用 **plists.map()** ，并将整数列表加倍。

**代码:使用 plist**

```
import plists, remote_double
plists.map(remote_double, range(10))
```

**输出:**

```
[0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```

map()函数是在 plists.py 中定义的。它包含一个纯模块、一个参数列表和一个可选的二元组列表，二元组由(spec，count)组成。默认规格为[('popen '，2)]，这意味着用户将打开两个本地网关和通道。一旦这些通道被打开，用户就可以将它们放入 itertools 循环中，这将创建一个无限迭代器，一旦到达终点，它就会循环回到起点。

现在，每个参数都可以以参数的形式发送到一个通道进行处理，并且由于通道是循环的，所以每个通道都获得了几乎均匀的参数分布。这就是 **i** 进来的地方——结果返回的顺序未知，所以 **i** 作为列表中每个参数的索引，被传递给通道，然后返回，这样用户就可以按照原来的顺序组合结果。然后用一个多通道接收队列等待结果，并将它们插入一个与原始参数长度相同的预填充列表中。获得所有预期结果后，退出网关并返回结果，如下面给出的代码所示–

**代码:**

```
import itertools, execnet
def map(mod, args, specs =[('popen', 2)]):
    gateways = []
    channels = []

    for spec, count in specs:
        for i in range(count):
            gw = execnet.makegateway(spec)
            gateways.append(gw)
            channels.append(gw.remote_exec(mod))

    cyc = itertools.cycle(channels)

    for i, arg in enumerate(args):
        channel = next(cyc)
        channel.send((i, arg))
    mch = execnet.MultiChannel(channels)
    queue = mch.make_receive_queue()
    l = len(args)
    # creates a list of length l, 
    # where every element is None
    results = [None] * l 

    for i in range(l):
        channel, (i, result) = queue.get()
        results[i] = result

    for gw in gateways:
        gw.exit()
    return results
```

**代码:通过修改规格增加并行化**

```
plists.map(remote_double, range(10), [('popen', 4)])
```

**输出:**

```
[0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```

然而，更多的并行化不一定意味着更快的处理。这取决于可用的资源，打开的网关和通道越多，需要的开销就越大。理想情况下，每个中央处理器内核应该有一个网关和通道，以获得最大的资源利用率。对任何纯模块使用 **plists.map()** ，只要它接收并发回 2 元组，其中 I 是第一个元素。当有一堆要处理的数字需要尽快处理时，这种模式是最有用的。