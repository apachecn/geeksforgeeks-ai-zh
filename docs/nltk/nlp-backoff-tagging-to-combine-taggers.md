# NLP |回退标记来组合标记器

> 原文:[https://www . geesforgeks . org/NLP-back back-taging-to-combine-taggers/](https://www.geeksforgeeks.org/nlp-backoff-tagging-to-combine-taggers/)

**什么是词性标注？**
这是一个将句子转换成形式的过程——单词列表、元组列表(其中每个元组都有一个形式(单词、标签))。的标记是词性标记，表示该词是否是名词、形容词、动词等。
![](img/7553b3c29942831a554c69fa800f3e0b.png)

**什么是回退标记？**
这是**sequentialbackfftagger**最重要的特性之一，因为它允许将 taggers 组合在一起。这样做的好处是，如果标记者不知道单词的标记，那么它可以将这个标记任务传递给下一个回退标记者。如果那一个做不到，它可以将该字传递给下一个
退避标记器，以此类推，直到没有退避标记器留下来检查。

**代码#1:执行标记**

```
# Loading Libraries 
from nltk.tag import SequentialBackoffTagger
from nltk.tag import DefaultTagger 
from nltk.tag import UnigramTagger  

from nltk.corpus import treebank

# initializing training and testing set    
train_data = treebank.tagged_sents()[:3000]
test_data = treebank.tagged_sents()[3000:]

# Defining Tag 
tag1 = DefaultTagger('NN')

# Tagging
tag2 = UnigramTagger(train_data, backoff = tag1)

# Evaluation
tag2.evaluate(test_data)
```

**输出:**

```
0.8752428232246924

```

**它是如何工作的？**
sequentialbackfftagger 类可以接受 backoff 关键字参数，其值是 sequentialbackfftagger 的另一个实例。在上面的代码中，unigram 词性标记器与 Default 标记器进行了补偿，并在 **treebank.tagged_sents()** 数据集上进行了训练。

**代码#2:准备回退标记员内部列表**

```
from nltk.tag import SequentialBackoffTagger

print (tag1._taggers == [tag1])

print ("\n", tag2._taggers == [tag2, tag1])
```

**输出:**

```
True

True

```

**它是如何工作的？**

*   SequentialBackoffTagger 类被初始化，创建一个 backoff taggers 的内部列表，第一个元素是它自己。
*   如果给定了回退标记符，则回退标记符的内部标记符列表会被追加。
*   SequentialBackoffTagger 类 uses _ taggers list 是调用 tag()方法时 backoff taggers 的内部列表。
*   在每个标签上调用 choose_tag()，它会遍历标签列表。
*   当找到标记时，它停止并返回标记。
*   如果主标记器可以标记单词，将返回标记。
*   否则，它返回无，并尝试下一个标记器，以此类推，直到找到一个标记，否则返回无。

**代码#3:用泡菜保存并装载一个训练有素的标记器。**

```
# Loading Libraries
import pickle

# Opening file and writing
file = open('tagger.pickle', 'wb')
pickle.dump(tagger, file)
file.close()

# Reading file
file = open('tagger.pickle', 'rb')
# Loading
tagger = pickle.load(f)
```

**输出:**

```
nltk.data.load('tagger.pickle') will load the file 

```