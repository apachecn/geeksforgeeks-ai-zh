# NLP |使用 RegEx 进行分块和缝隙

> 原文:[https://www . geesforgeks . org/NLP-chunking-and-chink-with-regex/](https://www.geeksforgeeks.org/nlp-chunking-and-chinking-with-regex/)

**组块提取或部分解析**是从句子(用词性标注)中提取有意义的短短语的过程。
词块是由单词组成的，单词的种类是用词性标签来定义的。人们甚至可以定义一个不能成为查克一部分的模式或单词，这样的单词被称为 **chinks** 。ChunkRule 类指定在一个块中包含和排除哪些单词或模式。

**定义 Chunk 模式:**
Chuck 模式是正常的正则表达式，它们被修改和设计为匹配词性标签，词性标签被设计为匹配词性标签序列。尖括号用于指定单个标签，例如–*匹配名词标签*。可以用同样的方式定义多个标签。

**代码#1:将组块转换为正则表达式模式。**

## 蟒蛇 3

```
# Laading Library
from nltk.chunk.regexp import tag_pattern2re_pattern

# Chunk Pattern to RegEx Pattern
print("Chunk Pattern : ", tag_pattern2re_pattern('<DT>?<NN.*>+'))
```

**输出:**

```
Chunk Pattern :  ()?(<(NN[^\{\}]*)>)+
```

大括号用于指定像{}这样的块，并指定可以翻转大括号{ }的缝隙模式。对于特定的短语类型，这些规则(组块和缝隙模式)可以组合成语法。

**代码#2:用 RegExParser 解析句子。**

## 蟒蛇 3

```
from nltk.chunk import RegexpParser

# Introducing the Pattern
chunker = RegexpParser(r'''
NP:
{<DT><NN.*><.*>*<NN.*>}
}<VB.*>{
''')

chunker.parse([('the', 'DT'), ('book', 'NN'), (
    'has', 'VBZ'), ('many', 'JJ'), ('chapters', 'NNS')])
```

**输出:**

```
Tree('S', [Tree('NP', [('the', 'DT'), ('book', 'NN')]), ('has', 'VBZ'), 
Tree('NP', [('many', 'JJ'), ('chapters', 'NNS')])])
```