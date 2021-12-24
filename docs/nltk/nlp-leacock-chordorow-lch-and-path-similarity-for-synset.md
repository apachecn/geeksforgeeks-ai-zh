# NLP | Leacock Chordorow (LCH)和 Synset 的路径相似性

> 原文:[https://www . geesforgeks . org/NLP-leacock-chordorow-lch-和-path-相似性-for-synset/](https://www.geeksforgeeks.org/nlp-leacock-chordorow-lch-and-path-similarity-for-synset/)

**基于路径的相似性:**它是一种相似性度量，用于找出两个合成集之间最短路径的长度。

**Leacock Chordorow (LCH) :** 这是一种相似性度量，是基于路径的相似性的扩展版本，因为它结合了分类学的深度。因此，它是两个概念(synset_1 和 synset_2)之间最短路径(spath)的负对数除以分类法总深度(D)的两倍，如下图所示。
T3】

**代码#1:引入 Synsets。**

```
from nltk.corpus import wordnet 

syn1 = wordnet.synsets('hello')[0] 
syn2 = wordnet.synsets('selling')[0] 

print ("hello name : ", syn1.name()) 
print ("selling name : ", syn2.name()) 
```

**输出:**

```
hello name :   hello.n.01
selling name :   selling.n.01

```

**代码#2:路径相似性**

```
syn1.path_similarity(syn2) 
```

**输出:**

```
0.08333333333333333

```

**代码#3 : Leacock Chordorow (LCH)相似度**

```
syn1.lch_similarity(syn2) 
```

**输出:**

```
1.1526795099383855

```