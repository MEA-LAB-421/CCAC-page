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

* 所有参赛者首先需要获得DFME数据集使用许可和参赛队伍注册表，具体信息请参见如下网站查看：[link](https://mea-lab-421.github.io/)
* 
##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

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
