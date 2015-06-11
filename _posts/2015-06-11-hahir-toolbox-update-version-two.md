---
layout: post
title: 哈希图像检索工具包HABIR更新至V2.0
categories: [image retrieval]
---

[HABIR](http://yongyuan.name/habir/)是本小子在做哈希图像检索研究时对将一些经典且近年来比较流行的方法进行总结整理后集成的一个Matlab工具包，在上一次更新后，陆陆续续收到使用该工具包的小伙伴们反馈过来的一些信息和bug。对于那些能及时处理的bug，本小子本地修复完后基本都及时push上去了，而对于一些未完善的指标评价及写得不是很合理的某些地方，一则因为改动得比较大，二则由于自己忙于写另外一篇关于哈希检索方面的论文，所以没及时push上去。这几天终于把文章的初稿写完了，不是很忙了，所以把自上次更新后所作的一些代码修改的地方做了整理，推送上去了，好让小伙伴们早点用上更好的工具。

此次更新主要是将原来一些结构写得不是很合理的地方重新做了稍微的调整，添加了新的评价指标，截止到该v2.0版，评价指标已经基本涵盖了论文中的常用对比指标，另外还添加了两种新的哈希方法，代码说明文档写得更详细和规范。下面晒晒在Caltech-256上用VGG在imageNet上训练好的模型提取的1024维特征做的一些实验结果。
![precision-recall-128bits]({{ site.url }}/images/posts/2015-06-11/128bits.png)
![precision-recall-64bits]({{ site.url }}/images/posts/2015-06-11/64bits.png)
![precision-recall-32bits]({{ site.url }}/images/posts/2015-06-11/32bits.png)
![precision-recall-16bits]({{ site.url }}/images/posts/2015-06-11/16bits.png)
![precision-recall-8bits]({{ site.url }}/images/posts/2015-06-11/8bits.png)