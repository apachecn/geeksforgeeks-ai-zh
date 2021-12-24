# NLP |交换动词短语和名词基数

> 原文:[https://www . geesforgeks . org/NLP-交换-动词-短语-名词-红雀/](https://www.geeksforgeeks.org/nlp-swapping-verb-phrases-and-noun-cardinals/)

**需要交换动词短语吗？**
消除特定短语中的被动语态。通过将两个明显不同的短语算作同一个短语，这种规范化有助于频率分析。

下面的代码是`swap_verb_phrase class`，它使用动词作为轴心点，将块的左侧与右侧交换。它使用定义的`first_chunk_index()`函数来查找要绕其旋转的动词。

**代码#1:交换 _ 动词 _ 短语类交换动词**

```
def swap_verb_phrase(chunk):
    def vbpred(wt):
        word, tag = wt
        return tag != 'VBG' and tag.startswith('VB') and len(tag) > 2

    vbidx = first_chunk_index(chunk, vbpred)

    if vbidx is None:
        return chunk

    return chunk[vbidx + 1:] + chunk[:vbidx]
```

**代码#2:评估 swap _ 动词 _ 短语**

```
swap_verb_phrase([('the', 'DT'), ('book', 'NN'),
               ('was', 'VBD'), ('great', 'JJ')])
```

**输出:**

```
[('great', 'JJ'), ('the', 'DT'), ('book', 'NN')]

```

代码没有绕动名词旋转，因为它们通常用于描述名词。

**代码#3 :**

```
swap_verb_phrase([('this', 'DT'), 
                  ('gripping', 'VBG'), ('book', 'NN'), 
                  ('is', 'VBZ'), ('fantastic', 'JJ')])
```

**输出:**

```
[('fantastic', 'JJ'), ('this', 'DT'), ('gripping', 'VBG'), ('book', 'NN')]

```

**交换名词红雀:**
一个组块中的红雀指的是一个数字，被标记为 CD。这些基数出现在名词前。把基数放在名词前面是有用的。

**代码#4:交换名词红雀**

```
swap_noun_cardinal([('Dec.', 'NNP'), ('10', 'CD')])

swap_noun_cardinal([('the', 'DT'), ('top', 'NN'), ('10', 'CD')])
```

**输出:**

```
[('10', 'CD'), ('Dec.', 'NNP')]

[('the', 'DT'), ('10', 'CD'), ('top', 'NN')]

```