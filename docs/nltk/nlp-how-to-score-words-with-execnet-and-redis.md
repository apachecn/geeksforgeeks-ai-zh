# NLP |如何用 Execnet 和 Redis 进行单词评分

> 原文:[https://www . geesforgeks . org/NLP-如何用-execnet-and-redis 给单词打分/](https://www.geeksforgeeks.org/nlp-how-to-score-words-with-execnet-and-redis/)

分布式单词评分可以使用 Redis 和 Execnet 一起执行。对于 movie_reviews 语料库中的每个单词，FreqDist 和 ConditionalFreqDist 用于计算信息增益。
使用>redishashreqdist 和一个**redisconditional hashreqdist**，可以用 Redis 进行同样的操作。分数然后被存储在**重新排序的**中。为了更好地利用 Redis，使用 Execnet 来分配计数。
Redis 和 execnet 用来一起做分布式单词评分。中每个单词的信息增益是使用 FreqDist 和 ConditionalFreqDist 计算的。现在有了 Redis，同样的事情可以用一个**redishashreqdist**和一个**redisconditionalhashreqdist**来执行，然后把分数存储在一个 **RedisOrderedDict** 中。Execnet 可以用来分配计数，以便从 Redis 中获得更好的性能。安装 redis 和 execnet 后， **redis 服务器的实例**必须在本地主机上运行。
**步骤:**

*   对于 movie_reviews 语料库中的每个标签(只有 pos 和 neg 标签)，首先获取一个元组列表——标签和单词。
*   然后从 dist_featx 模块，使用 score_words()获取单词分数。
*   总字数为 39，764，word_scores 函数是**redordereddict**的一个实例。
*   然后获取前 1000 个单词，并使用 key()方法检查前五个单词，看看它们是什么。
*   从 word_scores 获得所有需要的数据后，删除 Redis 中的键，因为不再需要这些数据。

**代码:**

## 蟒蛇 3

```py
# importing libraries
from dist_featx import score_words
from nltk.corpus import movie_reviews

# finding category via categoreies
category = movie_reviews.categories()

print ("Categories : ", category)
category_words = [
        (l, movie_reviews.words(categories = [l]))
        for l in category]

# Scores
word_scores = score_words(category_words)
print ("Length : ", len(word_scores))

# top words
topn_words = word_scores.keys(end = 1000)
print ("Top Words : ", topn_words[0:5])

# Delete the keys in Redis after getting
# all the required from word_scores
from redis import Redis
r = Redis()
print ([r.delete(key) for
     key in ['word_fd', 'label_word_fd:neg',
             'label_word_fd:pos', 'word_scores']] )
```

**输出:**

```py
Categories :  ['neg', 'pos']
Length : 39767
Top Words : [b'bad', b', ', b'and', b'?', b'movie']
[1, 1, 1, 1]
```

**score_words()** 是 dist_featx 的函数。但是它需要等待一段时间，因为它需要一些时间来完成。使用 execnet 和 Redis 的开销意味着它将比非分布式内存版本的函数花费更长的时间。
**它是如何工作的？**
**dist _ featx . py**模块包含 score_words()函数，该函数执行以下操作:

*   打开网关和通道。
*   向每个通道发送初始化数据。
*   为了计数，它通过通道发送每个(标签，单词)元组。
*   向每个通道发送完成消息。
*   等待回复。
*   关闭通道和网关。
*   根据计数计算每个单词的分数。
*   将分数存储在 RedisOrderedDict 中。

一旦计数完成，对所有单词评分并存储结果。代码如下:
**代码:**

## 蟒蛇 3

```py
# Importing library
import itertools, execnet, remote_word_count
from nltk.metrics import BigramAssocMeasures
from redis import Redis
from redisprob import RedisHashFreqDist, RedisConditionalHashFreqDist
from rediscollections import RedisOrderedDict

# Scoring the words
def score_words(category_words,
                score_fn = BigramAssocMeasures.chi_sq,
                host ='localhost', specs =[('popen', 2)]):
    gateways = []
    channels = []

    # counting
    for spec, count in specs:
        for i in range(count):
            gw = execnet.makegateway(spec)
            gateways.append(gw)
            channel = gw.remote_exec(remote_word_count)
            channel.send((host, 'word_fd', 'category_word_fd'))
            channels.append(channel)

    cyc = itertools.cycle(channels)

    # syncing the channel
    for category, words in category_words:
        channel = next(cyc)
        channel.send((category, list(words)))

    for channel in channels:
        channel.send('done')
        assert 'done' == channel.receive()
        channel.waitclose(5)

    for gateway in gateways:
        gateway.exit()

    r = Redis(host)
    # frequency distribution
    fd = RedisHashFreqDist(r, 'word_fd')
    cfd = RedisConditionalHashFreqDist(r, 'category_word_fd')
    word_scores = RedisOrderedDict(r, 'word_scores')
    n_xx = cfd.N()

    for category in cfd.conditions():
        n_xi = cfd[category].N()

    for word, n_ii in cfd[category].iteritems():
        word = word.decode()
        n_ix = fd[word]

        if n_ii and n_ix and n_xi and n_xx:
            score = score_fn(n_ii, (n_ix, n_xi), n_xx)
            word_scores[word] = score
    # final word scores       
    return word_scores
```

如果有两个以上的标签，应使用不同的评分方法。比较两个标签，评分方法只会准确。这些要求将决定你如何存储单词分数。
有两种数据可以在拥有实例后通过通道接收–

1.  已完成的消息:它表示没有更多的数据通过通道进入。
    用另一条 done 消息回复，最后退出循环关闭通道。
2.  (标签，单词)的二元组:用于迭代以增加**redishashreqdist**和**redisconditionalhashreqdist**中的计数