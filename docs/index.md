---
layout: default
---

<!-- 
[Link to another page](./another-page.html). -->



# 关于Tmark_kg
互联网上存在着海量的数据，尤其以文字为代表的自然语言更是一个十足的知识宝库，但是现如今很多知识的提取只能依赖于人类手工去整理效率真的没法说了。
依赖于现如今深度学习的技术进步，让机器代替人类从这些海量的数据中提取有价值的信息变得越来越可行了。

## 会用到什么
会用到什么命名实体，Bert，Trandformer，聚类，文本相似度。
BERT中注意力机制真的很强。
![alt text](https://raw.githubusercontent.com/napoler/tmark_kg/master/docs/src/640.png "BERT中注意力机制")
## 思路
现有的很多知识提取大多是是从句子中提取的，但是文本中的数据往往是结构不全的，还有语义消解等等问题需要解决，引入BERT文章级别提取后就可以不用考虑这些了。

https://colab.research.google.com/drive/1Nlhh2vwlQdKleNMqpmLDBsAwrv_7NnrB


### 测试一下
tmark_Description中测试的效果

![alt text](https://raw.githubusercontent.com/napoler/tmark_Description/master/ner_train/static/pre_test.png "效果测试")
已经可以提取出文章中关于边境牧羊犬的相关知识了。

## 标注数据
这是一切的开始。[开源描述标注](https://www.terrychan.org/tmark_Description/)

标注工具
https://github.com/t-web/ChineseAnnotator

标注工具Ai_bert
https://github.com/t-web/ChineseAnnotator/tree/Ai_bert 加入了自动提取实体和描述。



### 格式BMES

BMES

B表示一个词的词首位值，M表示一个词的中间位置，E表示一个词的末尾位置，S表示一个单独的字词。


| [开源描述标注](https://www.terrychan.org/tmark_Description/)|基于实体提取对应文章中的描述|
| [tkitMarker_bert描述标注](https://www.terrychan.org/tkitMarker_bert/)|使用bert做实体描述提取|


##

| [句子相似](https://www.terrychan.org/transformers-SentenceSimilarity/)|利用预训练的中文模型实现基于bert的语义匹配模型 数据集为LCQMC官方数据|

## 联系我

如果您有任何意见都可以随时联系我

Github上留言：
https://github.com/napoler/tmark_kg/issues

邮箱：
napoler2008{@}gmail.com

