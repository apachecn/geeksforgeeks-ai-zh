# NLP |提取命名实体

> 原文:[https://www . geesforgeks . org/NLP-extracting-named-entities/](https://www.geeksforgeeks.org/nlp-extracting-named-entities/)

识别命名实体是一种特定类型的块提取，它使用实体标签和块标签。
常见的实体标签包括 PERSON、LOCATION 和 ORGANIZATION。POS 标记的句子被解析成具有正常组块的组块树，但是树标签可以是代替组块短语标签的实体标签。NLTK 已经有一个预先训练好的命名实体组块器，可以在 nltk.chunk 模块中使用`ne_chunk()`方法。这个方法把一个句子分成一棵树。

**代码#1:在树库 _ 组块语料库的标记句子上使用 ne-chunk()**

```py
from nltk.corpus import treebank_chunk
from nltk.chunk import ne_chunk

ne_chunk(treebank_chunk.tagged_sents()[0])
```

**输出:**

```py
Tree('S', [Tree('PERSON', [('Pierre', 'NNP')]), Tree('ORGANIZATION', 
[('Vinken', 'NNP')]), (', ', ', '), ('61', 'CD'), ('years', 'NNS'), 
('old', 'JJ'), (', ', ', '), ('will', 'MD'), ('join', 'VB'), ('the', 'DT'),
('board', 'NN'), ('as', 'IN'), ('a', 'DT'), ('nonexecutive', 'JJ'), 
('director', 'NN'), ('Nov.', 'NNP'), ('29', 'CD'), ('.', '.')])

```

找到了两个实体标签:PERSON 和 ORGANIZATION。这些子树中的每一个都包含被识别为“个人”或“组织”的单词列表。

**代码#2:使用所有子树的叶子提取命名实体的方法**

```py
def sub_leaves(tree, label):
    return [t.leaves() 
            for t in tree.subtrees(
                    lambda s: label() == label)]
```

**代码#3:使用方法从树上获取所有的人或组织的叶子**

```py
tree = ne_chunk(treebank_chunk.tagged_sents()[0])

from chunkers import sub_leaves
print ("Named entities of PERSON : ", 
       sub_leaves(tree, 'PERSON'))

print ("\nNamed entites of ORGANIZATION : ", 
       sub_leaves(tree, 'ORGANIZATION'))
```

**输出:**

```py
Named entities of PERSON : [[('Pierre', 'NNP')]]

Named entites of ORGANIZATION : [[('Vinken', 'NNP')]]

```

一次处理多个句子，使用`chunk_ne_sents()`。在下面的代码中，来自`treebank_chunk.tagged_sents()`的前 10 个句子被处理以获得组织`sub_leaves()`。

**代码#4:我们来了解一下`chunk_ne_sents()`**

```py
from nltk.chunk import chunk_ne_sents
from nltk.corpus import treebank_chunk

trees = chunk_ne_sents(treebank_chunk.tagged_sents()[:10])
[sub_leaves(t, 'ORGANIZATION') for t in trees]
```

**输出:**

```py
[[[('Vinken', 'NNP')]], [[('Elsevier', 'NNP')]], [[('Consolidated', 'NNP'), 
('Gold', 'NNP'), ('Fields', 'NNP')]], [], [], [[('Inc.', 'NNP')], 
[('Micronite', 'NN')]], [[('New', 'NNP'), ('England', 'NNP'),
('Journal', 'NNP')]], [[('Lorillard', 'NNP')]], [], []]

```