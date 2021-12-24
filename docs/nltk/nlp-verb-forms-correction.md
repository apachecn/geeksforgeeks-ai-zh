# NLP |动词形式修正

> 原文:[https://www.geeksforgeeks.org/nlp-verb-forms-correction/](https://www.geeksforgeeks.org/nlp-verb-forms-correction/)

让我们用一个例子来理解这一点:

1.  我们的孩子训练够了吗？
2.  我们的孩子训练够了吗？

动词“is”只能与单数名词连用。对于复数名词，我们用“是”。这个问题在现实世界中非常常见，我们可以通过创建动词纠正映射来纠正这个错误，该映射的使用取决于词块中的名词是复数还是单数。

**代码#1:定义动词修正映射**

```
# singular to plural mapping

plural_verb_forms = {
        ('is', 'VBZ'): ('are', 'VBP'),
        ('was', 'VBD'): ('were', 'VBD')
        }

# plural to singular mapping
singular_verb_forms = {
        ('are', 'VBP'): ('is', 'VBZ'),
        ('were', 'VBD'): ('was', 'VBD')
        }
```

我们使用 first_chunk_index()方法在块中搜索第一个标记单词的位置。这个方法有一个参数“pred”，它接受一个(单词，标签)元组并返回真或假。

**代码#2 : first_chunk_index()**

```
def first_chunk_index(chunk, pred, start = 0, step = 1):

    l = len(chunk)
    end = l if step > 0 else -1

    for i in range(start, end, step):
        if pred(chunk[i]):
            return i

    return None
```

如果(单词，标签)参数中的标签以给定的标签前缀开头，下面代码中的谓词函数将返回 True。否则，假的。

**代码#3 :**

```
def tag_startswith(prefix):
    def f(wt):
        return wt[1].startswith(prefix)
    return f
```

**代码#4:让我们纠正动词形式**

```
from transforms import correct_verbs

print ("Corrected verb forms : \n", 
       correct_verbs([('is', 'VBZ'), ('our', 'PRP{content}apos;), 
                      ('children', 'NNS'), ('learning', 'VBG')]))
```

**输出:**

```
Corrected verb forms : 
[('are', 'VBP'), ('our', 'PRP{content}apos;), ('children', 'NNS'), ('learning',
'VBG')]

```