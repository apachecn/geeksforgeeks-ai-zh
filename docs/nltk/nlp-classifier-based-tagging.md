# NLP |基于分类器的标记

> 原文:[https://www.geeksforgeeks.org/nlp-classifier-based-tagging/](https://www.geeksforgeeks.org/nlp-classifier-based-tagging/)

**分类器类**:

*   它是分类标签器的一个子类，使用分类技术来做词性标注。
*   从单词中提取特征，然后传递给内部分类器。
*   它对特征进行分类，并返回一个标签，即词性标签。
*   特征检测器找到多个长度后缀，进行一些正则表达式匹配，并查看单字、二元模型和三元模型历史，为每个单词生成一组相当完整的特征

**代码#1:使用分类后标签**

```
from nltk.tag.sequential import ClassifierBasedPOSTagger
from nltk.corpus import treebank

# initializing training and testing set    
train_data = treebank.tagged_sents()[:3000]
test_data = treebank.tagged_sents()[3000:]

tagging = ClassifierBasedPOSTagger(train = train_data)

a = tagging.evaluate(test_data)

print ("Accuracy : ", a)
```

**输出:**

```
Accuracy : 0.9309734513274336

```

分类器类继承了分类器类，只实现了一个 feature_detector()方法。所有的训练和标记都是在分类标签器中完成的。

**代码#2:使用 MaxentClassifier**

```
from nltk.classify import MaxentClassifier
from nltk.corpus import treebank

# initializing training and testing set    
train_data = treebank.tagged_sents()[:3000]
test_data = treebank.tagged_sents()[3000:]

tagger = ClassifierBasedPOSTagger(
        train = train_sents, classifier_builder = MaxentClassifier.train)

a = tagger.evaluate(test_data)

print ("Accuracy : ", a)
```

**输出:**

```
Accuracy : 0.9258363911072739

```

**自定义特征检测器检测特征**
有两种方法可以做到:

1.  子类 ClassifierBasedTagger 并实现一个 feature_detector()方法。
2.  在初始化时，将一个函数作为 feature_detector 关键字参数传递给 ClassifierBasedTagger。

**代码#3:自定义特征检测器**

```
from nltk.tag.sequential import ClassifierBasedTagger
from tag_util import unigram_feature_detector
from nltk.corpus import treebank

# initializing training and testing set    
train_data = treebank.tagged_sents()[:3000]
test_data = treebank.tagged_sents()[3000:]

tag = ClassifierBasedTagger(
        train = train_data, 
        feature_detector = unigram_feature_detector)

a = tagger.evaluate(test_data)

print ("Accuracy : ", a)
```

**输出:**

```
Accuracy : 0.8733865745737104

```