# NLP |词性标注–单词语料库

> 原文:[https://www . geesforgeks . org/NLP-词性-标记词-语料库/](https://www.geeksforgeeks.org/nlp-part-of-speech-tagged-word-corpus/)

**什么是词性标注？**
这是一个将句子转换成形式的过程——单词列表、元组列表(其中每个元组都有一个形式(单词、标签))。的标记是词性标记，表示该词是否是名词、形容词、动词等。
![](img/ff7c190a02d627b2b4652c4b63247129.png)

**词性标注语料库示例**

```
The/at-tl expense/nn and/cc time/nn involved/vbn are/ber astronomical/jj ./.

```

标记语料库的格式为**单词/标记**的形式。每个单词都有一个标记来表示它的位置。比如 **nn** 指名词， **vb** 指动词。
![](img/05b4a789bf2bd00424b24b51cec33895.png)

**代码#1 :** 创建 TaggedCorpusReader。为了文字

```
# Using TaggedCorpusReader
from nltk.corpus.reader import TaggedCorpusReader

# intitializing
x = TaggedCorpusReader('.', r'.*\.pos')

words = x.words()
print ("Words : \n", words)

tag_words = x.tagged_words()
print ("\ntag_words : \n", tag_words)
```

**输出:**

```
Words : 
['The', 'expense', 'and', 'time', 'involved', 'are', ...]

tag_words : 
[('The', 'AT-TL'), ('expense', 'NN'), ('and', 'CC'), ...]

```

**代码#2 :** 用于句子

```
tagged_sent = x.tagged_sents()
print ("tagged_sent : \n", tagged_sent)
```

**输出:**

```
tagged_sent : 
[[('The', 'AT-TL'), ('expense', 'NN'), ('and', 'CC'), ('time', 'NN'),
('involved', 'VBN'), ('are', 'BER'), ('astronomical', 'JJ'), ('.', '.')]]

```

**代码#3 :** 为段落

```
para = x.para()
print ("para : \n", para)

tagged_para = x.tagged_paras()
print ("\ntagged_paras : \n", tagged_paras)
```

**输出:**

```
para: 
[[['The', 'expense', 'and', 'time', 'involved', 'are', 'astronomical', '.']]]

tagged_paras : 
[[[('The', 'AT-TL'), ('expense', 'NN'), ('and', 'CC'), ('time', 'NN'),
('involved', 'VBN'), ('are', 'BER'), ('astronomical', 'JJ'), ('.', '.')]]] 
```