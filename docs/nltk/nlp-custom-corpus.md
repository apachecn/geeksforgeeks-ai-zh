# NLP |自定义语料库

> 原文:[https://www.geeksforgeeks.org/nlp-custom-corpus/](https://www.geeksforgeeks.org/nlp-custom-corpus/)

**什么是语料库？**
语料库可以定义为文本文档的集合。它可以被认为只是一个目录中的一堆文本文件，通常与文本文件的许多其他目录放在一起。

**是怎么做到的？**
NLTK 已经在 **nltk.data.path** 中定义了数据路径或目录列表。我们的定制语料库必须存在于任何给定的路径中，这样 NLTK 才能找到它。
我们还可以在主目录中创建一个自定义的 nltk_data 目录，并验证它是否在 **nltk.data.path.** 指定的已知路径列表中

**代码#1:创建自定义目录并验证。**

```py
# importing libraries
import os, os.path

# using the given path
path = os.path.expanduser('~/nltk_data')

# checking
if not os.path.exists(path):
    os.mkdir(path)

print ("Does path exists : ", os.path.exists(path))

import nltk.data
print ("\nDoes path exists in nltk : ", 
       path in nltk.data.path)
```

**输出:**

```py
Does path exists : True
Does path exists in nltk : True
```

**代码#2:创建单词列表文件。**

```py
# loading libraries
import nltk.data

nltk.data.load('corpora/cookbook/word_file.txt', format ='raw')
```

**输出:**

```py
b'nltk\n'
```

**这一切是如何运作的？**

*   **nltk.data.load()** 识别格式–“生”、“泡菜”和“yaml”。
*   如果没有给出格式，它会根据文件的扩展名猜测格式。
*   与上面的代码一样，需要指定“原始”格式。
*   与上面的代码一样，需要指定“原始”格式。
*   如果文件以'结尾。“yaml ”,则无需指定格式。

**代码#3:如何加载 YAML 文件**

```py
import nltk.data

# loading file using the path
nltk.data.load('corpora/cookbook/synonyms.yaml')
```

**输出:**

```py
{'bday': 'birthday'}
```