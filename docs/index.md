---
layout: default
---

<!-- 
[Link to another page](./another-page.html). -->



# 关于Tmark_kg
互联网上存在着海量的数据，尤其以文字为代表的自然语言更是一个十足的知识宝库，但是现如今很多知识的提取只能依赖于人类手工去整理效率真的没法说了。
依赖于现如今深度学习的技术进步，让机器代替人类从这些海量的数据中提取有价值的信息变得越来越可行了。

还有就是开放信息提取，而不是规定几十种特定关系的提取，那样子会很熟限制的，毕竟文本数据是海量的。
## 会用到什么
会用到什么

命名实体，Bert，Trandformer，聚类，文本相似度。
scrapy

BERT中注意力机制真的很强。
![alt text](https://raw.githubusercontent.com/napoler/tmark_kg/master/docs/src/640.png "BERT中注意力机制")
## 思路
现有的很多知识提取大多是是从句子中提取的，但是文本中的数据往往是结构不全的，还有语义消解等等问题需要解决，引入BERT文章级别提取后就可以不用考虑这些了。
直接让神经网络学到实体和知识点之间挂钩，至于各种指代词之类的也就不用考虑了。

## 文本数据（准备数据）
这里应该是祭出爬虫的时候了。
除了scrapy这个爬虫框架外，还可以引入基于密度的正文提取，只有这样子才可以做到泛化内容提取。
## 现有数据
| 数据 | 描述 |
| ------------ | ------------ |
| [百度Ai开放数据](https://ai.baidu.com/broad/download?dataset=duconv) | 找到Information Extraction和Knowledge Extraction下载就是了。一个信息提取，一个知识提取感觉差距都不是很多，规定了几十种关系，想要做到开放数据提取还要更多的标记才行，还有就是句子级别的。|
| [tmark_Description开源描述标注](https://www.terrychan.org/tmark_Description/) | 基于实体提取对应文章中的描述 |
| [openkg](http://openkg.cn/) | openkg里更多数据和工具，如果是做句子级别的可以在这里找到已经提取的知识然后用知识作为关键词配合elasticsearch构建自己的数据 |




## 标注数据（准备数据）
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









### 实体
命名实体这个基本不用夺取赘述了，很多都可以做。无论是使用现有的还是自己去构建命名实体还都是比较轻松。

### 实体+关系+描述 
至于更具体些的想要学习 
实体+关系+描述 

如同上面的思路只要把提取分成两步就简单多了。
实体+关系
（实体+关系）+描述 
当然这个效率不是很高，不过好在还是蛮有效率的，可以提取很多意想不到的知识。


https://colab.research.google.com/drive/1Nlhh2vwlQdKleNMqpmLDBsAwrv_7NnrB


### 测试一下
使用tmark_Description数据训练的测试效果

![alt text](https://raw.githubusercontent.com/napoler/tmark_Description/master/ner_train/static/pre_test.png "效果测试")
已经可以提取出文章中关于边境牧羊犬的相关知识了。


##

| [句子相似](https://www.terrychan.org/transformers-SentenceSimilarity/)|利用预训练的中文模型实现基于bert的语义匹配模型 数据集为LCQMC官方数据|




## 其他项目
jiagu
很强，可以做句子级别的知识提取

## 联系我

如果您有任何意见都可以随时联系我

Github上留言：
https://github.com/napoler/tmark_kg/issues

邮箱：
napoler2008{@}gmail.com

