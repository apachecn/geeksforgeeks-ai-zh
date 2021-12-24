# NLP |训练分词器并过滤句子中的停用词

> 原文:[https://www . geesforgeks . org/NLP-training-a-token izer-and-filling-stop words-in-a-in-a-句子/](https://www.geeksforgeeks.org/nlp-training-a-tokenizer-and-filtering-stopwords-in-a-sentence/)

**为什么我们需要训练一个句子标记器？**
在 NLTK 中，默认句子标记器用于通用目的，效果非常好。但是对于某些类型的文本来说，它可能不是最好的，因为该文本可能使用非标准的标点符号，或者它可能具有独特的格式。因此，为了处理这种情况，训练句子标记器可以产生更精确的句子标记。

为了理解这个概念，让我们考虑下面的文本。这种文本在任何网络文本语料库中都很常见。

```
Example of TEXT:
A guy: So, what are your plans for the party?
B girl: well! I am not going!
A guy: Oh, but u should enjoy.
```

要下载文本文件，点击这里的。

**代码#1:训练标记器**

```
# Loading Libraries
from nltk.tokenize import PunktSentenceTokenizer
from nltk.corpus import webtext

text = webtext.raw('C:\\Geeksforgeeks\\data_for_training_tokenizer.txt')
sent_tokenizer = PunktSentenceTokenizer(text)
sents_1 = sent_tokenizer.tokenize(text)

print(sents_1[0])
print("\n"sents_1[678])
```

**输出:**

```
'White guy: So, do you have any plans for this evening?'

'Hobo: Got any spare change?'

```

**代码#2:默认句子标记器**

```
from nltk.tokenize import sent_tokenize
sents_2 = sent_tokenize(text)

print(sents_2[0])
print("\n"sents_2[678])
```

**输出:**

```
'White guy: So, do you have any plans for this evening?'

'Girl: But you already have a Big Mac...\r\nHobo: Oh, this is all theatrical.'

```

第二个输出中的这种差异很好地说明了为什么训练自己的句子标记器是有用的，尤其是当您的文本不是典型的段落-句子结构时。

**训练是如何进行的？**
`PunktSentenceTokenizer class`遵循无监督学习算法来学习什么构成断句。它是无监督的，因为这样就不需要给出任何带标签的训练数据，只需要原始文本。

### 筛选标记化句子中的停用词

**Stopwords** 是出现在文本中的常用词，但通常不会影响句子的意思。对于信息检索和自然语言处理来说，它们几乎不重要。例如–“the”和“a”。大多数搜索引擎会从搜索查询和文档中过滤掉停止词。
NLTK 库附带了一个 stopwords 语料库–`nltk_data/corpora/stopwords/`，其中包含多种语言的单词列表。

**代码 Python 中的 Stopwords】**

```
# Loading Library
from nltk.corpus import stopwords

# Using stopwords from English Languages
english_stops = set(stopwords.words('english'))

# Printing stopword list present in English
words = ["Let's", 'see', 'how', "it's", 'working']

print ("Before stopwords removal: ", words)
print ("\nAfter stopwords removal : ",
       [word for word in words if word not in english_stops])
```

**输出:**

```
Before stopwords removal:  ["Let's", 'see', 'how', "it's", 'working']

After stopwords removal :  ["Let's", 'see', 'working']
?
```

**代码# 4:NLTK stop words 中使用的语言的完整列表。**

```
stopwords.fileids()
```

**输出:**

```
['danish', 'dutch', 'english', 'finnish', 'french', 'german',
'hungarian', 'italian', 'norwegian', 'portuguese', 'russian',
'spanish', 'swedish', 'turkish']
```