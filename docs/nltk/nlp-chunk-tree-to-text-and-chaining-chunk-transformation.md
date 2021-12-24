# NLP |块树到文本和链接块转换

> 原文:[https://www . geesforgeks . org/NLP-chunk-tree-to-text-and-chain-chunk-transformation/](https://www.geeksforgeeks.org/nlp-chunk-tree-to-text-and-chaining-chunk-transformation/)

我们可以将树或子树转换回句子或组块字符串。为了理解如何做到这一点，下面的代码使用了 treebank_chunk 语料库的第一棵树。

**代码#1:用空格连接树中的单词。**

```py
# Loading library    
from nltk.corpus import treebank_chunk

# tree
tree = treebank_chunk.chunked_sents()[0]

print ("Tree : \n", tree)

print ("\nTree leaves : \n", tree.leaves())

print ("\nSentence from tree : \n", ' '.join(
        [w for w, t in tree.leaves()]))
```

**输出:**

```py
Tree : 
 (S
  (NP Pierre/NNP Vinken/NNP), /,
  (NP 61/CD years/NNS)
  old/JJ, /,
  will/MD
  join/VB
  (NP the/DT board/NN)
  as/IN
  (NP a/DT nonexecutive/JJ director/NN Nov./NNP 29/CD)
  ./.)

Tree leaves : 
 [('Pierre', 'NNP'), ('Vinken', 'NNP'), (', ', ', '), ('61', 'CD'), 
 ('years', 'NNS'), ('old', 'JJ'), (', ', ', '), ('will', 'MD'), ('join', 'VB'),
 ('the', 'DT'), ('board', 'NN'), ('as', 'IN'), ('a', 'DT'), ('nonexecutive', 'JJ'),
 ('director', 'NN'), ('Nov.', 'NNP'), ('29', 'CD'), ('.', '.')]

Sentence from tree : 
 Pierre Vinken, 61 years old, will join the board as a nonexecutive director Nov. 29 .

```

在上面的代码中，标点符号是不正确的，因为句点和逗号被视为特殊的单词。所以，他们也获得了周围的空间。但是在下面的代码中，我们可以使用正则表达式替换来修复这个问题。

**代码#2 : `chunk_tree_to_sent()`功能改进代码 1**

```py
import re

# defining regex expression
punct_re = re.compile(r'\s([, \.;\?])')

def chunk_tree_to_sent(tree, concat =' '):

    s = concat.join([w for w, t in tree.leaves()])
    return re.sub(punct_re, r'\g<1>', s)
```

**代码#3:评估组块 _ 树 _ to _ send()**

```py
# Loading library    
from nltk.corpus import treebank_chunk
from transforms import chunk_tree_to_sent

# tree
tree = treebank_chunk.chunked_sents()[0]

print ("Tree : \n", tree)

print ("\nTree leaves : \n", tree.leaves())

print ("Tree to sentence : ", chunk_tree_to_sent(tree))
```

**输出:**

```py
Tree : 
 (S
  (NP Pierre/NNP Vinken/NNP), /,
  (NP 61/CD years/NNS)
  old/JJ, /,
  will/MD
  join/VB
  (NP the/DT board/NN)
  as/IN
  (NP a/DT nonexecutive/JJ director/NN Nov./NNP 29/CD)
  ./.)

Tree leaves : 
 [('Pierre', 'NNP'), ('Vinken', 'NNP'), (', ', ', '), ('61', 'CD'), 
 ('years', 'NNS'), ('old', 'JJ'), (', ', ', '), ('will', 'MD'), ('join', 'VB'),
 ('the', 'DT'), ('board', 'NN'), ('as', 'IN'), ('a', 'DT'), ('nonexecutive', 'JJ'),
 ('director', 'NN'), ('Nov.', 'NNP'), ('29', 'CD'), ('.', '.')]

Tree to sentence : 
Pierre Vinken, 61 years old, will join the board as a nonexecutive director Nov. 29.

```

**链接组块转换**
转换函数可以被链接在一起以规范化组块，并且得到的组块通常更短，并且它仍然保持相同的含义。

在下面的代码中，一个单独的块和可选的转换函数列表被传递给该函数。该函数将调用块上的每个转换函数，并将返回最终的块。

**代码#4 :**

```py
def transform_chunk(
        chunk, chain = [filter_insignificant, 
                        swap_verb_phrase, swap_infinitive_phrase, 
                        singularize_plural_noun], trace = 0):
    for f in chain:
        chunk = f(chunk)

        if trace:
            print (f.__name__, ':', chunk)

    return chunk
```

**代码#5:评估转换 _ 区块**

```py
from transforms import transform_chunk

chunk = [('the', 'DT'), ('book', 'NN'), ('of', 'IN'), 
         ('recipes', 'NNS'), ('is', 'VBZ'), ('delicious', 'JJ')]

print ("Chunk : \n", chunk)

print ("\nTransformed Chunk : \n", transform_chunk(chunk))
```

**输出:**

```py
Chunk :  
[('the', 'DT'), ('book', 'NN'), ('of', 'IN'), ('recipes', 'NNS'), 
('is', 'VBZ'), ('delicious', 'JJ')]

Transformed Chunk : 
[('delicious', 'JJ'), ('recipe', 'NN'), ('book', 'NN')]

```