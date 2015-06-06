---
layout: post
title:  基于词袋模型的object retrieval
categories: [machine learning]
---

**数据集**：Oxford Building数据集(5063张图片)，共55张查询图片，按Oxford Building标的goundtruth进行查询，注意查询的时候，按boundingbox所在的区域进行查询。因为采用的是SIFT，所以对于boundingbox区域外的SIFT特征点，利用SIFT特征点的坐标可以剔除掉那些boundingbox区域外的SIFT特征点的特征点。

### rootSIFT+BoVW+Spatial Verification
使用rootSIFT结合词袋模型，并加上对前n个返回结果进行空间(也称几何)校正的重排后，其计算得到的mAP如下：
1   74.82%
20  77.77%
40  79.86%
60  81.01%
80  81.70%
100 82.18%
120 82.48%
140 82.78%
160 83.07%
180 83.25%
200 83.35%
400 84.73%
600 85.01%
800 85.36%
1000 85.52%
1500 85.69%
2000 85.73%

### rootSIFT+BoVW
不利用几何校正方法进行重排，mAP为74.82%