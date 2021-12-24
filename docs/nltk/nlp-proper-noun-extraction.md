# NLP |专有名词抽取

> 原文:[https://www.geeksforgeeks.org/nlp-proper-noun-extraction/](https://www.geeksforgeeks.org/nlp-proper-noun-extraction/)

分块所有专有名词(用 NNP 标记)是执行命名实体提取的一种非常简单的方法。使用正则表达式类可以创建一个简单的语法，将所有专有名词组合成一个名称块。

然后，我们可以在 *treebank_chunk* 的第一个标记句子上进行测试，将结果与之前的食谱进行比较:

**代码#1:在 treebank_chunk 的第一个标记句子**上测试

```py
from nltk.corpus import treebank_chunk
from nltk.chunk import RegexpParser
from chunkers import sub_leaves

chunker = RegexpParser(r'''  
                       NAME:
                       {<NNP>+}
                       ''')

print ("Named Entities : \n", 
       sub_leaves(chunker.parse(
               treebank_chunk.tagged_sents()[0]), 'NAME'))
```

**输出:**

```py
Named Entities : 
[[('Pierre', 'NNP'), ('Vinken', 'NNP')], [('Nov.', 'NNP')]]

```

**注意:**上面的代码返回了所有专有名词—‘Pierre’、‘Vinken’、‘nov .’
NAME chunker 是 RegexpParser 类的简单用法。所有 NNP 标记单词的序列被组合成名称组块。
`PersonChunker class`如果你只想把人的名字拼起来，就可以用。

**代码#2 : PersonChunker 类**

```py
from nltk.chunk import ChunkParserI
from nltk.chunk.util import conlltags2tree
from nltk.corpus import names

class PersonChunker(ChunkParserI):
    def __init__(self):
        self.name_set = set(names.words())

    def parse(self, tagged_sent):

        iobs = []
        in_person = False
        for word, tag in tagged_sent:
            if word in self.name_set and in_person:
                iobs.append((word, tag, 'I-PERSON'))
            elif word in self.name_set:
                iobs.append((word, tag, 'B-PERSON'))
                in_person = True
            else:
                iobs.append((word, tag, 'O'))
                in_person = False

        return conlltags2tree(iobs)
```

`PersonChunker class`通过迭代标记的句子来检查每个单词是否在它的 names_set(由 names 语料库构建)中。如果当前单词在 name _ set 中，它将使用 B-PERSON 或 I-PERSON IOB 标记，具体取决于前一个单词是否也在 name _ set 中。O IOB 标记被分配给名称集参数中没有的单词。完成后，使用`conlltags2tree()`将 IOB 标签列表转换为树。

**代码#3:在同一个标记句子上使用 PersonChunker 类**

```py
from nltk.corpus import treebank_chunk
from nltk.chunk import RegexpParser
from chunkers import sub_leaves

from chunkers import PersonChunker
chunker = PersonChunker()
print ("Person name  : ", 
       sub_leaves(chunker.parse(
               treebank_chunk.tagged_sents()[0]), 'PERSON'))
```

**输出:**

```py
Person name  : [[('Pierre', 'NNP')]]

```