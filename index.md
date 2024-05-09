---
layout: default
---

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

# 比赛简介

微表情是一种微弱的、短暂的和无意识的面部情感表达，通常发生在有压力的情境下，伴随着个体尝试掩盖其内心真实想法时产生。由于微表情能有效地揭露个体的真实情感和意图，所以准确识别微表情在刑侦审讯、临床心理、商业洽淡等多个领域都有重要的应用价值。微表情自动识别旨在让机器有足够的智能，感知人脸视频序列的微表情运动特征，并理解对应的隐藏情绪。近年来，微表情识别研究已经吸引了大量情感计算研究者们的关注，但微表情运动微弱、短暂且局部，以及缺乏大规模训练样本，严重制约了微表情识别及应用的发展。

本挑战赛使用目前规模最大的DFME动态人脸微表情数据集的**部分数据**作为训练及测试数据，旨在促进在数据更充分条件下的微表情识别方法的探索，进而推进本领域研究的交流和发展。本次挑战赛的任务主要是进行微表情情感标签分类识别，即对给定的微表情视频样本，参赛者需要设计识别算法模型以预测其对应的七种情感类别。

特别说明的是，为了保证比较的公平性和客观性，本次比赛采用**A/B榜的竞赛方法**，A榜成绩决定参赛队伍能否进入决赛B榜（_取A榜前**6**名_），最终比赛排名由B榜决定。

## 日程安排

| **时间节点**                         | **相关事宜**                                                    |
|----------------------------------|-------------------------------------------------------------|
| 2024年5月5日     8:00 AM（GMT+08:00） | 任务发布与报名启动，                                                  |
| 2024年5月15日   8:00 AM（GMT+08:00）  | 训练数据发布                                                      |
| 2024年5月30日   8:00 AM（GMT+08:00）  | **A榜测试集**数据发布，A榜提交入口发布|
| 2024年6月30日   8:00 AM（GMT+08:00）  | **A榜**提交截止（报名结束）                                                |
| 2024年7月1日     8:00 AM（GMT+08:00） | **A榜**成绩公布 ；**B榜**测试数据发布；**B榜**提交入口发布（**3次**提交机会）                           |
| 2024年7月5日     8:00 AM（GMT+08:00） | **B榜**提交截止                               |
| 2024年7月8日     8:00 AM（GMT+08:00） | 2-3页技术报告提交                                                  |
| 2024年7月10日 10:00 AM（GMT+08:00）   | B榜成绩及最终比赛结果公布                                               |
| 2024年7月20日 10:00 AM（GMT+08:00）   | CCAC2022大会召开及颁奖典礼                                           |

## 注意事项

* **A榜**中，验证集可自行划分，测试集不提供情感标签，提交测试集预测标签，每天限制提交**1**次
* **B榜**中，总共只有**三次**提交机会
* **B榜**中，最后一次提交，需给出代码github地址

# 比赛任务

本次比赛的任务为七分类人脸微表情识别，参赛者需要设计识别方法，对测试集中的每个微表情样本，从**高兴、愤怒、鄙视、厌恶、恐惧、伤心** 和 **惊讶**七种类别中选择一种情感标签进行预测。如果预测标签与数据集中的真实标签一致则视为该样本识别正确，否则为识别错误。比赛将根据识别准确程度对参赛者提交的方法进行排名，识别准确度具体评价指标参见第四节。

# 比赛数据说明

## 数据获取

- 所有参赛者首先需要获得DFME数据集使用许可和参赛队伍注册表，具体信息请参见如下网站查看：[link](https://mea-lab-421.github.io/)
- DFME数据集协议请从如下网址获取：[link](https://mea-lab-421.github.io/files/DFME_license.pdf)
- 参赛队伍注册：[link](https://docs.qq.com/form/page/DQ3dVQ3NDVkdnSHNm)
- 由于人脸数据特别敏感，请仔细阅读数据使用协议，这里对一些注意事项再次进行说明：
  - DFME数据集仅可使用于包括本次比赛在内的学术研究相关用途，严禁商用；
  - 学生参赛者在申请DFME数据集时需要导师同意并提供导师签名的数据集协议；
  - 部分被试人脸图片数据不可被用于论文展示，具体信息请参考协议；
  - 所有/部分数据样本不能擅自公开发布，或者提供给第三者使用。
- DFME数据集论文引用格式如下：
```
Sirui Zhao, Huaying Tang, Xinglong Mao, Shifeng Liu, Hao Wang, Tong Xu, Enhong Chen. DFME: A New Benchmark for Dynamic Facial Micro-expression Recognition," in IEEE Transactions on Affective Computing [J]. IEEE Transactions on Affective Computing, doi: 10.1109/TAFFC.2023.3341918，2023.
```

## DFME数据集介绍

DFME数据集是目前数量规模最大、采集帧率最高的动态自发微表情数据集，共有来自671名被试（656名实际有效）的7526个微表情视频样本，包含了七种情感类别：高兴（happiness）、愤怒（anger）、鄙视（contempt）、厌恶（disgust）、恐惧（fear）、伤心（sadness）和惊讶（surprise）。采集帧率覆盖了200、300或500fps。本次比赛使用DFME中**259名被试**的**2629个微表情**视频样本。此外还提供了起始帧、峰值帧及结束帧的标注以及AU标签的标注。

## 数据划分

本次比赛使用DFME中259名被试的2629个微表情视频样本。其中176名被试的1856个样本作为训练集，这部分数据及其关键帧标签和情绪类别标签在比赛开始时将提供给所有参赛者；剩下的样本将不重复划分为A榜和B榜两部分测试集，为了保证比赛的公平性，测试集在比赛评测阶段前将对参赛者不可见。评测阶段时，仅向参赛者提供测试集样本及样本名及帧率信息等信息，但不提供情绪类别标签，全部数据及标签将在后续比赛结束后向申请者提供。**为减少被试身份信息的影响，这三部分数据的被试互不重叠**。

### 注意事项

* 参赛者可以使用除DFME测试集外的微表情/表情数据用于训练。但如果使用了除DFME训练集以外的数据，请在后续的技术分享中进行说明，以便后续研究参考。使用额外数据不会对排名产生影响，但使用额外数据必须给出数据获取方式以保证方法的可复现性，否则成绩无效。
* 训练数据为未进行人脸裁剪、对齐等操作的原始数据，预处理方法的选择（或不进行预处理）是参赛方案的一部分 ，参赛者可以自行选择。


# 评估协议

## 评价指标
本比赛评估指标同DFME数据集论文所示，使用了UF1、UAR及ACC指标，其中以UF1作为排名依据。

### ACC
ACC is one of the most common metrics, which can evaluate the overall performance of the recognition method on the database. It is calculated as follows: 
$$A C C=\frac{\sum_{i=1}^{K} T P_i}{\sum_{i=1}^{K} N_i}$$
where $K$ represents the number of the classes, $N_i$ stands for the sample number of the $i$-th class and $TP_i$ is the number of true positive samples of the $i$-th class. 


### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
