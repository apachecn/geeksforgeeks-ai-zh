# NLP |使用 Execnet 进行分布式标记–第 2 部分

> 原文:[https://www . geesforgeks . org/NLP-distributed-taging-with-exec net-part-2/](https://www.geeksforgeeks.org/nlp-distributed-tagging-with-execnet-part-2/)

网关的 **remote_exec()** 方法接受一个参数，该参数可以是以下三种类型之一:

*   要远程执行的代码字符串
*   将被序列化并远程执行的纯函数的名称
*   将远程执行其源代码的纯模块的名称

**代码:使用带三个选项的 remote_tag.py 模块**

```
import pickle

if __name__ == '__channelexec__':
    tagger = pickle.loads(channel.receive())
for sentence in channel:
    channel.send(tagger.tag(sentence))
```

**什么是纯模块？**

*   纯模块是一个独立的模块:它只能访问在它执行的地方可用的 Python 模块，并且不能访问任何存在于最初创建网关的地方的变量或状态。
*   类似地，纯函数是一个独立的函数，没有外部依赖。
*   要检测 execnet 正在执行模块，请检查 **__name__** 变量。如果它等于 **'__channelexec__'** ，那么它被用来创建一个远程通道。
*   这类似于如果 **__name__ == '__main__'** 检查模块是否正在
    命令行上执行。
*   首先要做的是调用 channel.receive()来获取序列化的标记符，该标记符是使用 **pickle.loads()** 加载的
*   注意到通道没有在任何地方被导入——这是因为它包含在模块的全局命名空间中。execnet 远程执行的任何模块都可以访问通道变量，以便与通道创建者进行通信。
*   在标记器之后，迭代地标记()从通道接收的每个标记化的句子。
*   这允许用户标记发送者想要发送的句子，因为迭代不会停止，直到通道关闭。
*   因此，创建了一个用于词性标注的计算节点，它将 100%的资源用于标注它收到的任何句子。只要通道保持打开，节点就可以进行处理。

Execnet 可以做的更多，比如开放多通道增加并行处理，以及通过 SSH 向远程主机开放网关做分布式处理。

**创建多个通道**
创建多个通道，每个网关一个通道，使处理更加并行。每个网关创建一个新的子进程(如果使用 SSH 网关，则创建一个远程解释器)，每个网关使用一个通道进行通信。一旦创建了两个通道，就可以使用 MultiChannel 类将它们组合起来，这样用户就可以遍历这些通道，并形成一个接收队列来接收来自每个通道的消息。
创建每个通道并发送标记器后，通道循环通过，向每个通道发送偶数个句子进行标记。然后，从队列中收集所有响应。对 **queue.get()** 的调用将返回一个二元组(通道，消息)，以防需要知道消息来自哪个通道。一旦收集了所有标记的句子，网关就可以轻松退出。

**代码:**

```
import itertools

gw1 = execnet.makegateway()
gw2 = execnet.makegateway()

ch1 = gw1.remote_exec(remote_tag)
ch1.send(pickled_tagger)
ch2 = gw2.remote_exec(remote_tag)
ch2.send(pickled_tagger)

mch = execnet.MultiChannel([ch1, ch2])
queue = mch.make_receive_queue()
channels = itertools.cycle(mch)

for sentence in treebank.sents()[:4]:
    channel = next(channels)
    channel.send(sentence)
tagged_sentences = []

for i in range(4):
    channel, tagged_sentence = queue.get()
    tagged_sentences.append(tagged_sentence)

print ("Length : ", len(tagged_sentences))

gw1.exit()
gw2.exit()
```

**输出:**

```
Length : 4
```

在示例代码中，只发送了四个句子，但在现实生活中，一个人需要发送数千个句子。一台计算机可以非常快速地标记四个句子，但是当需要标记成千上万个句子时，将句子发送到多台计算机比等待一台计算机完成所有工作要快得多。