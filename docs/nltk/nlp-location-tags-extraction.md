# NLP |位置标签提取

> 原文:[https://www.geeksforgeeks.org/nlp-location-tags-extraction/](https://www.geeksforgeeks.org/nlp-location-tags-extraction/)

不同种类的 ChunkParserI 子类可以用来识别位置块。因为它使用地名录语料库来识别位置词。地名词典语料库是包含以下位置词的`WordListCorpusReader class`:

*   国家名称
*   美国各州和缩写
*   墨西哥各州
*   美国主要城市
*   加拿大各省

`LocationChunker class`通过迭代标记的句子来寻找在地名词典语料库中找到的单词。当它找到一个或多个位置词时，它使用 IOB 标签创建一个位置块。在`iob_locations()`中产生 IOB 位置标签，并且`parse()`方法将 IOB 标签转换成树。

**代码#1 : LocationChunker 类**

```py
from nltk.chunk import ChunkParserI
from nltk.chunk.util import conlltags2tree
from nltk.corpus import gazetteers

class LocationChunker(ChunkParserI):
    def __init__(self):
        self.locations = set(gazetteers.words())
        self.lookahead = 0
        for loc in self.locations:
            nwords = loc.count(' ')
        if nwords > self.lookahead:
            self.lookahead = nwords
```

**代码#2 : iob_locations()方法**

```py
def iob_locations(self, tagged_sent):

    i = 0
    l = len(tagged_sent)
    inside = False

    while i < l:
        word, tag = tagged_sent[i]
        j = i + 1
        k = j + self.lookahead
        nextwords, nexttags = [], []
        loc = False

    while j < k:
        if ' '.join([word] + nextwords) in self.locations:
            if inside:
                yield word, tag, 'I-LOCATION'
            else:
                yield word, tag, 'B-LOCATION'
            for nword, ntag in zip(nextwords, nexttags):
                yield nword, ntag, 'I-LOCATION'
                loc, inside = True, True
                i = j
                break

        if j < l:
            nextword, nexttag = tagged_sent[j]
            nextwords.append(nextword)
            nexttags.append(nexttag)
            j += 1
        else:
            break
        if not loc:
            inside = False
            i += 1
            yield word, tag, 'O'

    def parse(self, tagged_sent):
        iobs = self.iob_locations(tagged_sent)
        return conlltags2tree(iobs)
```

**代码#3:使用 LocationChunker 类解析句子**

```py
from nltk.chunk import ChunkParserI
from chunkers import sub_leaves
from chunkers import LocationChunker

t = loc.parse([('San', 'NNP'), ('Francisco', 'NNP'),
               ('CA', 'NNP'), ('is', 'BE'), ('cold', 'JJ'), 
               ('compared', 'VBD'), ('to', 'TO'), ('San', 'NNP'),
               ('Jose', 'NNP'), ('CA', 'NNP')])

print ("Location : \n", sub_leaves(t, 'LOCATION'))
```

**输出:**

```py
Location : 
[[('San', 'NNP'), ('Francisco', 'NNP'), ('CA', 'NNP')], 
[('San', 'NNP'), ('Jose', 'NNP'), ('CA', 'NNP')]]

```