# NLP |在 Redis 中存储频率分布

> 原文:[https://www . geesforgeks . org/NLP-storing-frequency-distribution-in-redis/](https://www.geeksforgeeks.org/nlp-storing-frequency-distribution-in-redis/)

nltk 中的许多类都使用了**类来存储和管理频率分布。它非常有用，但是都在内存中，没有提供持久化数据的方法。多个进程也无法访问单个 FreqDist。所有这些都可以通过在 Redis 上建立一个 FreqDist 来改变。
T3】什么是 Redis？**

*   Redis 是一个数据结构服务器，是比较流行的 **NoSQL 数据库**之一。
*   其中，它提供了一个网络可访问的数据库来存储字典(也称为哈希映射)。
*   为 Redis 哈希映射构建一个 FreqDist 接口将允许我们创建一个持久的 FreqDist，多个本地和远程进程可以同时访问它。

**安装:**

*   安装 Redis 和 redis-py。Redis 网站位于[http://redis.io/](http://redis.io/)，包含许多文档资源。
*   要使用哈希映射，请安装最新版本，在撰写本文时是 2.8.9。
*   可以使用 **pip install redis** 或 **easy_install redis** 安装 Redis Python 驱动程序 redis-py。此时最新的版本是 **2.9.1** 。
*   重定向视频主页位于 http://github . com/andymccurdy/redis-py/。
*   一旦两者都安装完毕，并且 redis-server 进程正在运行，您就可以开始了。让我们假设 redis-server 运行在端口 6379(默认主机和端口)上的 localhost 上。

**它是如何工作的？**

*   **FreqDist 类**扩展了标准库**集合。Counter** 类，它使一个 FreqDist 成为一个带有一些额外方法的小包装器，比如 N()。
*   **N()方法**返回样本结果的数量，这是频率分布
    中所有值的总和。
*   通过扩展一个**redhashmap**然后实现 N()方法，在 Redis 之上创建了一个与 API 兼容的类。
*   RedisHashFreqDist(在 redisprob.py 中定义)对 N()方法的哈希映射中的所有值求和

**代码:解释工作**

```py
from rediscollections import RedisHashMap

class RedisHashFreqDist(RedisHashMap):
    def N(self):
        return int(sum(self.values()))

    def __missing__(self, key):
        return 0

    def __getitem__(self, key):
        return int(RedisHashMap.__getitem__(self, key) or 0)

    def values(self):
        return [int(v) for v in RedisHashMap.values(self)]

    def items(self):
        return [(k, int(v)) for (k, v) in RedisHashMap.items(self)]
```

这个类可以像 FreqDist 一样使用。要实例化它，传递一个 Redis 连接和我们的哈希映射的名称。该名称应该是对这个特定 FreqDist 的唯一引用，这样它就不会与 Redis 中的任何其他键冲突。

**代码:**

```py
from redis import Redis
from redisprob import RedisHashFreqDist

r = Redis()
rhfd = RedisHashFreqDist(r, 'test')
print (len(rhfd))

rhfd['foo'] += 1
print (rhfd['foo'])

rhfd.items()
print (len(rhfd))
```

**输出:**

```py
0
1
1
```

大部分工作是在**redisashmap**类中完成的，该类扩展了**集合。可变映射**然后覆盖所有需要 Redis 特定命令的方法。**概述每个使用特定 Redis 命令的方法:**

*   **__len__() :** 这使用 hlen 命令来获取硬件映射中的元素数量
*   **_ _ 包含 __():** 这使用 hexists 命令来检查哈希映射中是否存在元素
*   **__getitem__():** 这使用 hget 命令从哈希映射中获取一个值
*   **__setitem__():** 这使用 hset 命令在哈希映射中设置一个值
*   **__delitem__():** 这使用 hdel 命令从硬件映射中移除一个值
*   **key():**这使用 hkeys 命令获取哈希映射中的所有密钥
*   **values():** 这使用 hvals 命令获取哈希映射中的所有值
*   **items():** 这使用 hgetall 命令来获取包含哈希映射中所有键和值的字典
*   **clear():** 这使用 delete 命令从 Redis 中移除整个哈希映射