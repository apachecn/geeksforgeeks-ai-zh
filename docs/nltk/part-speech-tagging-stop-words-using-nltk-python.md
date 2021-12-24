# python 中使用 NLTK 的带停止词的词性标注

> 原文:[https://www . geeksforgeeks . org/词性标注-停止-单词-使用-nltk-python/](https://www.geeksforgeeks.org/part-speech-tagging-stop-words-using-nltk-python/)

自然语言工具包是一个用于构建文本分析程序的平台。NLTK 模块更强大的方面之一是词性标注。

为了运行下面的 python 程序，您必须安装 NLTK。请遵循安装步骤。

*   打开终端，运行 **pip 安装 nltk** 。
*   在命令提示符下编写 python，这样 python Interactive Shell 就可以执行您的代码/脚本了。
*   键入**导入 nltk**
*   **nltk.download()**

将弹出一个图形用户界面，然后选择下载所有软件包的“全部”，然后单击“下载”。这将为您提供所有的标记器、分块器、其他算法和所有的语料库，所以这就是为什么安装将花费相当长的时间。
示例:

```
import nltk
nltk.download()

```

让我们来敲出一些快速词汇:
**语料库:**正文，单数。语料库是这个的复数。
**词汇:**单词及其含义。
**令牌:**每一个“实体”都是基于规则被分割的事物的一部分。

在语料库语言学中，**词性标注** ( **词性标注**或**词性标注**或 **POST** ，也称**语法标注**或**词类消歧**。

```
Input: Everything is all about money.
Output: [('Everything', 'NN'), ('is', 'VBZ'), 
          ('all', 'DT'),('about', 'IN'), 
          ('money', 'NN'), ('.', '.')] 

```

以下是标签列表、它们的含义以及一些示例:

> CC 并列连词
> CD 基数数字
> DT 限定词
> EX 存现存在那里(T5】像 : “有”……把它想成像 【存在】 ) FW 外来词
> IN 介词 / 比较级 【更大的】 JJS 形容词最高级 【最大的】T53】LS 列表标记1 MD 情态竟能T64】会
> NN 名词 单数【Harrison】 NNPS 专有名词复数 【美国人】 PDT 预定者 【所有的孩子】 POS 所有格结尾父母s
> PRP 人称代词 I
> UH 感叹词 errrrrrrrm
> VB 动词，基本形式取
> VBD 动词，过去式取
> VBG 动词，动名词/现在分词取
> VBN 动词，过去分词取
> VBP 动词，sing。现在，非 3d 带
> VBZ 动词，第三人称唱。现在进行时
> WDT wh-限定词哪个
> WP wh-代词谁，什么
> WP$所有格 wh-代词谁的
> WRB wh-ab 动词在哪里，什么时候

文本可能包含停止词，如“the”、“is”、“are”。可以从要处理的文本中过滤出停止词。在 nlp 研究中没有通用的停止词列表，但是 nltk 模块包含一个停止词列表。
可以添加自己的 Stop 字。去你的 NLTK 下载**目录路径** - > **语料库**->**stop words**->更新 stop words**文件**取决于你使用的语言。这里我们使用英语(stopwords.words('english ')。

```
import nltk
from nltk.corpus import stopwords
from nltk.tokenize import word_tokenize, sent_tokenize
stop_words = set(stopwords.words('english'))

// Dummy text
txt = "Sukanya, Rajib and Naba are my good friends. " \
    "Sukanya is getting married next year. " \
    "Marriage is a big step in one’s life." \
    "It is both exciting and frightening. " \
    "But friendship is a sacred bond between people." \
    "It is a special kind of love between us. " \
    "Many of you must have tried searching for a friend "\
    "but never found the right one."

# sent_tokenize is one of instances of 
# PunktSentenceTokenizer from the nltk.tokenize.punkt module

tokenized = sent_tokenize(txt)
for i in tokenized:

    # Word tokenizers is used to find the words 
    # and punctuation in a string
    wordsList = nltk.word_tokenize(i)

    # removing stop words from wordList
    wordsList = [w for w in wordsList if not w in stop_words] 

    #  Using a Tagger. Which is part-of-speech 
    # tagger or POS-tagger. 
    tagged = nltk.pos_tag(wordsList)

    print(tagged)
```

输出:

```
[('Sukanya', 'NNP'), ('Rajib', 'NNP'), ('Naba', 'NNP'), ('good', 'JJ'), ('friends', 'NNS')]
[('Sukanya', 'NNP'), ('getting', 'VBG'), ('married', 'VBN'), ('next', 'JJ'), ('year', 'NN')]
[('Marriage', 'NN'), ('big', 'JJ'), ('step', 'NN'), ('one', 'CD'), ('’', 'NN'), ('life', 'NN')]
[('It', 'PRP'), ('exciting', 'VBG'), ('frightening', 'VBG')]
[('But', 'CC'), ('friendship', 'NN'), ('sacred', 'VBD'), ('bond', 'NN'), ('people', 'NNS')]
[('It', 'PRP'), ('special', 'JJ'), ('kind', 'NN'), ('love', 'VB'), ('us', 'PRP')]
[('Many', 'JJ'), ('must', 'MD'), ('tried', 'VB'), ('searching', 'VBG'), ('friend', 'NN'), 
('never', 'RB'), ('found', 'VBD'), ('right', 'RB'), ('one', 'CD')]

```

**基本上，词性标注器的目标是将语言(主要是语法)信息分配给子句子单位。这种单位被称为记号，在大多数情况下，对应于单词和符号(例如标点符号)**。