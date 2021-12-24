# NLP |在 Redis 中存储有序字典

> 原文:[https://www . geesforgeks . org/NLP-storing-a-ordered-in-dictionary-redis/](https://www.geeksforgeeks.org/nlp-storing-an-ordered-dictionary-in-redis/)

有序字典就像普通字典，但是关键字是由一个排序函数排序的。就 Redis 而言，它支持关键字为字符串、值为浮点分数的有序字典。在必须计算信息增益并且必须存储所有单词和分数以备后用的情况下，这种结构可以派上用场。
redis collections . py 中的 RedisOrderedDict 类扩展了集合。MutableMapping 来免费获得一些 dict 兼容的方法。然后，它实现了所有需要 Redis 有序集的关键方法(也称为 **Zset** )命令:
**代码:在 Redis 中存储一个频率分布。**

```
class RedisOrderedDict(collections.MutableMapping):

    def __init__(self, r, name):
        self._r = r
        self._name = encode_key(name)

    def __iter__(self):
        return iter(self.items())

    def __len__(self):
        return self._r.zcard(self._name)

    def __getitem__(self, key):
        return self._r.zscore(self._name, encode_key(key))

    def __setitem__(self, key, score):
        self._r.zadd(self._name, encode_key(key), score)

    def __delitem__(self, key):
        self._r.zrem(self._name, encode_key(key))

    def keys(self, start = 0, end =-1):
        # we use zrevrange to get keys sorted
        # by high value instead of by
        lowest
        return self._r.zrevrange(self._name, start, end)

    def values(self, start = 0, end =-1):
        return [v for (k, v) in self.items(start = start, end = end)]

    def items(self, start = 0, end =-1):
        return self._r.zrevrange(self._name, start, end, withscores = True)

    def get(self, key, default = 0):
        return self[key] or default

    def iteritems(self):
        return iter(self)

    def clear(self):
        self._r.delete(self._name)
```

**代码:通过传入 Redis 连接和唯一名称**来创建 RedisOrderedDict 的实例

```
from redis import Redis
from rediscollections import RedisOrderedDict

r = Redis()
rod = RedisOrderedDict(r, 'test')
rod.get('bar')

rod['bar'] = 5.2
print (rod['bar'])

print (len(rod))

print (rod.items()) 

rod.clear()
```

**输出:**

```
0
5.2000000000000002
1
[(b'bar', 5.2)]
```

大部分代码可能看起来类似于 RedisHashMap，这是意料之中的，因为它们都扩展了**集合。可变映射**。这里的主要区别在于**redorderedset**通过浮点值对键进行排序，因此它不适合像**redisahmap**那样的任意键值存储。
**概述解释每个关键方法以及它们如何与 Redis 一起工作:**

*   **__len__():** 这使用 zcard 命令获取有序集中的元素数量。
*   **__getitem__():** 这使用 zscore 命令获取某个键的得分，如果该键不存在，则返回 0。
*   **__setitem__():** 这使用 zadd 命令向具有给定分数的有序集中添加一个键，或者如果该键已经存在，则更新分数。
*   **__delitem__():** 这使用 zrem 命令从有序集中移除密钥。
*   **keys():** 这使用 zrevrange 命令获取有序集中的所有键，按最高分排序。它需要两个可选的关键字参数，开始和结束，以更有效地获得有序键的一部分。