# NLP |展平深树

> 原文:[https://www.geeksforgeeks.org/nlp-flattening-deep-tree/](https://www.geeksforgeeks.org/nlp-flattening-deep-tree/)

我们使用的一些语料库通常是嵌套短语的深树。但是在这么深的树上工作对于训练矮子来说是一项乏味的工作。因为 IOB 标签解析不是为嵌套块设计的。所以，为了利用这些树进行矮化训练，我们必须将它们展平。
嗯，POS(词性)实际上是树结构的一部分，而不是在单词中。这些与`Tree.pos()`方法一起使用，该方法专门设计用于将单词与终端前树标签(如词性标签)相结合。

**代码#1:展平深树类**

```py
from nltk.tree import Tree

def flatten_childtrees(trees):
    children = []

    for t in trees:
        if t.height() < 3:
            children.extend(t.pos())

        elif t.height() == 3:
            children.append(Tree(t.label(), t.pos()))

        else:
            children.extend(
                    flatten_childtrees())

    return children

def flatten_deeptree(tree):
    return Tree(tree.label(), 
                flatten_childtrees())

```

**代码#2:评估`flatten_deeptree()`**

```py
from nltk.corpus import treebank
from transforms import flatten_deeptree

print ("Deep Tree : \n", treebank.parsed_sents()[0])

print ("\nFlattened Tree : \n", 
       flatten_deeptree(treebank.parsed_sents()[0]))    
```

**输出:**

```py
Deep Tree : 
 (S
  (NP-SBJ
    (NP (NNP Pierre) (NNP Vinken))
    (,, )
    (ADJP (NP (CD 61) (NNS years)) (JJ old))
    (,, ))
  (VP
    (MD will)
    (VP
      (VB join)
      (NP (DT the) (NN board))
      (PP-CLR (IN as) (NP (DT a) (JJ nonexecutive) (NN director)))
      (NP-TMP (NNP Nov.) (CD 29))))
  (. .))

Flattened Tree : 
Tree('S', [Tree('NP', [('Pierre', 'NNP'), ('Vinken', 'NNP')]), (', ',
', '), Tree('NP', [('61', 'CD'), ('years', 'NNS')]), ('old', 'JJ'),
(', ', ', '), ('will', 'MD'), ('join', 'VB'), Tree('NP', [('the',
'DT'), ('board', 'NN')]), ('as', 'IN'), Tree('NP', [('a', 'DT'),
('nonexecutive', 'JJ'), ('director', 'NN')]), Tree('NP-TMP', [('Nov.',
'NNP'), ('29', 'CD')]), ('.', '.')])

```

结果是一个更扁平的树，只包含名词短语。不属于名词短语的单词是分开的

**它是如何工作的？**

*   **flat _ deep Tree():**通过在给定树的每个子树上调用 flatten _ childtrees()从给定树返回一个新树。
*   **flat _ child trees():**递归向下钻取树，直到找到高度()等于或小于 3 的子树。

**代码#3:高度()**

```py
from nltk.corpus import treebank
from transforms import flatten_deeptree

from nltk.tree import Tree

print ("Height : ", 
       Tree('NNP', ['Pierre']).height())

print ("\nHeight : ", Tree(
        'NP', [Tree('NNP', ['Pierre']), 
                    Tree('NNP', ['Vinken'])]). height())
```

**输出:**

```py
Height : 2

Height : 3

```