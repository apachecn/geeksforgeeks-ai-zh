# NLP |在 Redis 中存储条件频率分布

> 原文:[https://www . geesforgeks . org/NLP-storing-conditional-frequency-distribution-in-redis/](https://www.geeksforgeeks.org/nlp-storing-conditional-frequency-distribution-in-redis/)

类是 FreqDist 实例的容器，每个条件有一个 FreqDist。它用于计算依赖于另一个条件的频率，例如另一个单词或类别标签。它在这里被用来使用**redisashreqdist**在 Redis 之上创建一个 API 兼容的类。
在下面给出的代码中，一个**redisconditionalshfreqdist**类扩展了**nltk . probability . conditionalreqdist**并覆盖了**getitem _ _()**方法。覆盖 **__getitem__()** ，以便创建 RedisHashFreqDist 的实例，而不是 FreqDist。

**代码:**

```
from nltk.probability import ConditionalFreqDist
from rediscollections import encode_key

class RedisConditionalHashFreqDist(ConditionalFreqDist):
    def __init__(self, r, name, cond_samples = None):
        self._r = r
        self._name = name
        ConditionalFreqDist.__init__(self, cond_samples)

        for key in self._r.keys(encode_key('% s:*' % name)):
            condition = key.split(':')[1]
            # calls self.__getitem__(condition)
            self[condition] 

    def __getitem__(self, condition):
        if condition not in self._fdists:
            key = '% s:% s' % (self._name, condition)
            val = RedisHashFreqDist(self._r, key)
            super(RedisConditionalHashFreqDist, self).__setitem__(
                    condition, val)
        return super(
                RedisConditionalHashFreqDist, self).__getitem__(condition)
    def clear(self):
        for fdist in self.values():
            fdist.clear()
```

这个类的一个实例可以通过传入一个 Redis 连接和一个基名称来创建。之后，它就像 ConditionalFreqDist 一样工作，如下面的代码所示:
**代码:**

```
from redis import Redis
from redisprob import RedisConditionalHashFreqDist

r = Redis()
rchfd = RedisConditionalHashFreqDist(r, 'condhash')

print (rchfd.N())

print (rchfd.conditions())

rchfd['cond1']['foo'] += 1

print (rchfd.N())

print (rchfd['cond1']['foo'])

print (rchfd.conditions())

rchfd.clear()
```

 **输出:**

```
0
[]
1
1
['cond1']
```

**它是如何工作的？**

*   **RedisConditionalHashFreqDist**使用名称前缀来引用 RedisHashFreqDist 实例。
*   传递到 RedisConditionalHashFreqDist 的名称是一个基本名称，它与每个条件相结合，为每个 **RedisHashFreqDist** 创建一个唯一的名称。
*   例如，如果 RedisConditionalHashFreqDist 的基本名称是**“cond hash”**，条件是“cond1”，那么 RedisHashFreqDist 的最终名称是**“cond hash:cond 1”**。
*   这种命名模式在初始化时使用 keys 命令来查找所有现有的哈希映射。
*   通过搜索所有匹配“condhash:*”的关键字，用户可以识别所有现有条件，并为每个条件创建一个 RedisHashFreqDist 实例。
*   将字符串与冒号组合是 Redis 键的一种常见命名约定，作为定义名称空间的一种方式。
*   每个 RedisConditionalHashFreqDist 实例定义一个哈希映射的命名空间。

RedisConditionalHashFreqDist 还定义了一个 **clear()** 方法。这是一个助手方法，它在所有内部 RedisHashFreqDist 实例上调用 clear()。**条件要求**中没有定义 clear()方法。