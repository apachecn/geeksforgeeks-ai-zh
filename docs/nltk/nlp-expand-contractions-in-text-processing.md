# NLP–在文本处理中扩展收缩

> 原文:[https://www . geesforgeks . org/NLP-expand-contracts-in-text-processing/](https://www.geeksforgeeks.org/nlp-expand-contractions-in-text-processing/)

文本预处理是自然语言处理的关键步骤。清理我们的文本数据，以便将其转换为可分析和可预测的可呈现形式，这就是所谓的文本预处理。在这篇文章中，我们将讨论缩写以及如何处理文本中的缩写。

**什么是宫缩？**

缩略词是通过删除字母并用撇号替换而缩短的单词或单词组合。

如今，一切都在网上转移，我们更多地通过短信或在不同的社交媒体上发布帖子与他人交流，如脸书、Instagram、Whatsapp、推特、领英等。以文本的形式。有这么多人在聊天，我们依靠缩写和单词的缩写来给人们发短信。

**比如**我 5 分钟内到。你不在那里吗？我是不是出去玩了？我想在 d 公园附近见到你。

在英语缩略词中，我们经常把一个单词的元音去掉，形成缩略词。删除缩写有助于文本标准化，并且当我们处理推特数据、产品评论时非常有用，因为这些词在情感分析中起着重要作用。

**宫缩如何扩张？**

**1。使用收缩库**

首先，安装库。你可以在谷歌 colab 上尝试这个库，因为安装这个库变得超级流畅。

**使用画中画:**

```py
!pip install contractions

```

**在朱皮特笔记本中:**

```py
import sys  
!{sys.executable} -m pip install contractions

```

#### 代码 1:使用收缩库扩展收缩

## 蟒蛇 3

```py
# import library
import contractions
# contracted text
text = '''I'll be there within 5 min. Shouldn't you be there too? 
          I'd love to see u there my dear. It's awesome to meet new friends.
          We've been waiting for this day for so long.'''

# creating an empty list
expanded_words = []    
for word in text.split():
  # using contractions.fix to expand the shotened words
  expanded_words.append(contractions.fix(word))   

expanded_text = ' '.join(expanded_words)
print('Original text: ' + text)
print('Expanded_text: ' + expanded_text)
```

**输出:**

```py
Original text: I'll be there within 5 min. Shouldn't you be there too? 
          I'd love to see u there my dear. It's awesome to meet new friends.
          We've been waiting for this day for so long.
Expanded_text: I will be there within 5 min. should not you be there too? 
          I would love to see you there my dear. it is awesome to meet new friends. 
          we have been waiting for this day for so long.

```

在形成词向量之前去除收缩有助于降维。

**代码 2:简单使用缩写，修复扩展文本。**

## 蟒 3

```py
text = '''She'd like to know how I'd done that! 
          She's going to the park and I don't think I'll be home for dinner.
          Theyre going to the zoo and she'll be home for dinner.'''

contractions.fix(text)
```

**输出:**

```py
'she would like to know how I would done that! 
 she is going to the park and I do not think I will be home for dinner.
 they are going to the zoo and she will be home for dinner.'

```

收缩也可以使用其他技术来处理，如字典映射，也可以使用 pycontractions 库。您可以参考 pycontractions 库的文档了解更多信息:[https://pypi.org/project/pycontractions/](https://pypi.org/project/pycontractions/)