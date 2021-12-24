# NLP |创建浅树

> 原文:[https://www.geeksforgeeks.org/nlp-creating-shallow-tree/](https://www.geeksforgeeks.org/nlp-creating-shallow-tree/)

先决条件:[展平深树](https://www.geeksforgeeks.org/nlp-flattening-deep-tree/)

我们只保留了最低级别的子树，从而展平了深树。但是这里我们可以保留最高级别的子树。

**代码#1:让我们理解`shallow_tree()`T2】**

```
from nltk.tree import Tree

def shallow_tree(tree):
        children = []

    for t in tree:
        if t.height() < 3:
            children.extend(t.pos())
    else:
        children.append(Tree(t.label(), t.pos()))

    return Tree(tree.label(), children)
```

**代码#2:评估**

```
from transforms import shallow_tree
from nltk.corpus import treebank

print ("Deep Tree : \n", treebank.parsed_sents()[0])

print ("\nShallow Tree : \n", shallow_tree(treebank.parsed_sents()[0]) )
```

**输出:**

```
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

Shallow Tree :
Tree('S', [Tree('NP-SBJ', [('Pierre', 'NNP'), ('Vinken', 'NNP'), (', ', ', '), 
('61', 'CD'), ('years', 'NNS'), ('old', 'JJ'), (', ', ', ')]),
Tree('VP', [('will', 'MD'), ('join', 'VB'), ('the', 'DT'), ('board', 'NN'), 
('as', 'IN'), ('a', 'DT'), ('nonexecutive', 'JJ'), ('director', 'NN'), 
('Nov.', 'NNP'), ('29', 'CD')]), ('.', '.')])

```

**它是如何工作的？**

*   函数的作用是:通过迭代每个顶级子树来创建新的子树。
*   如果子树的高度()小于 3，则该子树被其词性标记子树的列表替换。
*   如果树的子树是带词性标记的叶子，则所有其他子树将被新树替换。
*   因此，消除了所有嵌套的子树，同时仍然保留顶级子树。

**代码#3:高度**

```
print ("height of tree : ", 
       treebank.parsed_sents()[0].height())

print ("\nheight of shallow tree : ", 
       shallow_tree(treebank.parsed_sents()[0]).height())
```

**输出:**

```
height of tree : 7

height of shallow tree :3

```