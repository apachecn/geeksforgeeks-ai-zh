# NLP |单数复数名词和交换无限短语

> 原文:[https://www . geesforgeks . org/NLP-单数-复数-名词-和-交换-无限-短语/](https://www.geeksforgeeks.org/nlp-singularizing-plural-nouns-and-swapping-infinite-phrases/)

让我们用一个例子来理解这一点:

1.  我们的孩子训练够了吗？
2.  我们的孩子训练够了吗？

动词“is”只能与单数名词连用。对于复数名词，我们用“是”。这个问题在现实世界中非常常见，我们可以通过创建动词纠正映射来纠正这个错误，该映射的使用取决于词块中的名词是复数还是单数。

**代码#1:奇点 _ 复数 _ 名词()类**

```
def singularize_plural_noun(chunk):

    nnsidx = first_chunk_index(chunk, tag_equals('NNS'))

    if nnsidx is not None and 
    nnsidx + 1 < len(chunk) and 
    chunk[nnsidx + 1][1][:2] == 'NN':

        noun, nnstag = chunk[nnsidx]
        chunk[nnsidx] = (noun.rstrip('s'), nnstag.rstrip('S'))

    return chunk
```

**代码#2:奇点复数**

```
singularize_plural_noun([('recipes', 'NNS'), ('book', 'NN')])
```

**输出:**

```
[('recipe', 'NN'), ('book', 'NN')]

```

上面的代码寻找标签 NNS 寻找复数名词。创建后，如果下一个单词是名词(通过确保标签以 NN 开头来确定)，那么我们通过从标签和单词的右侧移除“s”来去除复数名词。

**交换无限短语**
不定式短语的形式是的 **A，如“电影世界”。On 可以将它转换为“电影世界”，它仍然具有相同的含义。**

**代码#3:我们来了解一下 swap _ infinitive _ 短语()类**

```
def swap_infinitive_phrase(chunk):
    def inpred(wt):
        word, tag = wt
        return tag == 'IN' and word != 'like'

    inidx = first_chunk_index(chunk, inpred)

    if inidx is None:
        return chunk

    nnidx = first_chunk_index(chunk, 
                              tag_startswith('NN'), 
                              start = inidx, step =-1) or 0

    return chunk[:nnidx] + chunk[inidx + 1:] + chunk[nnidx:inidx]
```

**代码#4:我们来评估一下 swap _ infinitive _ 短语**

```
from transforms import swap_infinitive_phrase

swap_infinitive_phrase([('book', 'NN'), 
                        ('of', 'IN'), ('recipes', 'NNS')])
```

**输出:**

```
[('recipes', 'NNS'), ('book', 'NN')]

```