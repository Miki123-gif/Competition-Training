[TOC]

# Completion training

为了锻炼自己的编程能力和对算法的理解，我准备使用kaggle比赛实战来提神自己，参考的教程是kaggle上大佬们写的notebook

三个教程使用的方法都不一样，学习的方法就是遇到不会的先跟着做，查询资料

第一个小的比赛使用的是泰坦尼克号数据，请参照Titanic\_tutories这个教程

[参考教程1 主要是参考这个教程](https://www.kaggle.com/ldfreeman3/a-data-science-framework-to-achieve-99-accuracy)

[参考教程2 和之前的教程1进行对比](https://www.kaggle.com/startupsci/titanic-data-science-solutions)

[参考教程3 也是很优秀的教程](https://www.kaggle.com/arthurtok/introduction-to-ensembling-stacking-in-python)

参考了特征工程入门这本书，之前的教程都没教如何提升模型，以及为什么要这样进行特征工程。现在系统地学习了一遍。这本书相当不错。

# 比赛平台介绍

介绍：数据挖掘比赛主要两个平台是国外的Kaggle和国内阿里的天池比赛。

- kaggle 比赛官网 www.kaggle.com
- 天池比赛官网 https://tianchi.aliyun.com/competition/gameList/activeList

# 比赛1 Titanic生存预测



比赛地址：https://www.kaggle.com/c/titanic

数据地址：https://github.com/Miki123-gif/train_kaggle/tree/master/Titanic/Data

赛题说明：1912年的时候，因为撞击了iceberg，导致泰坦尼克号下沉。非常不幸的是，泰坦尼克号上没有足够多的救生艇。因此2224名旅客和工作人员中，有1502人死亡。

在这次挑战中，我们希望你构建一个模型，利用每位船员的属性比如：姓名，年龄，性别，社会阶级等**回答什么样的人更有可能存活下去**。

赛题分析：因为是预测生存，所以属于二分类问题。可以使用所有分类算法进行尝试。

# 比赛2 Hours Price Predict



比赛地址：https://www.kaggle.com/c/house-prices-advanced-regression-techniques

数据地址：https://github.com/Miki123-gif/train_kaggle/tree/master/House%20Prices/Data

赛题说明：什么对房价的影响最大？是距离铁路的距离，还是房子卧室的数量？这个数据集中含有79个解释性变量，描述了爱荷华州房子的方方面面，训练集标签是每个房子的房价。希望你能使用机器学习算法，利用79个特征变量，对房价进行预测。

赛题分析：因为是对房价进行预测，标签是连续型变量，所以属于回归问题。可以使用回归算法，或者使用神经网络进行对房价预测。

# 比赛3 Digit Recognizer

比赛地址：https://www.kaggle.com/c/digit-recognizer

数据地址：

赛题说明：MINIST数据集包含了大量的手写数字集，有0-9一共10个类别的手写数字。在这次挑战中，你的目标是准确识别这些手写数字。希望你能使用不同的机器学习算法，比较各种算法的不同。

赛题分析：典型的图像识别问题，可以使用knn等分类算法，也可以使用cnn神经网络，涉及到可以用pytorch搭建神经网络。knn准确率虽然也能达到百分之89.但是还是存在问题。因为忽略了数字集在空间上可能有些规律。

# 比赛4 二手车交易价格预测

比赛地址：https://tianchi.aliyun.com/competition/entrance/231784/information

数据地址：

赛题说明：你的任务是根据提供的特征，对二手车的交易价格进行预测。该数据来自某交易平台的二手车交易记录，总数据量超过40w，包含31列变量信息，其中15列为匿名变量。为了保证比赛的公平性，将会从中抽取15万条作为训练集，5万条作为测试集A，5万条作为测试集B，同时会对name、model、brand和regionCode等信息进行脱敏。

赛题分析：和房价预测类似，都是属于回归问题。使用回归算法或者神经网络算法进行预测。

# 比赛5 O2O优惠券使用预测

比赛地址：https://tianchi.aliyun.com/competition/entrance/231593/information

数据地址：

赛题说明：什么是O2O，表示线上online，对线下online。我们知道一个商家投放消费券给客户，如果投放给老客户，可以促进他们二次消费，如果投放给新用户，可以吸引他们进店消费。如果滥发消费券，很容易造成资源浪费。本赛题提供用户在2016年1月1日至2016年6月30日之间真实线上线下消费行为，预测用户在2016年7月领取优惠券后15天以内的使用情况。注意： 为了保护用户和商家的隐私，所有数据均作匿名处理，同时采用了有偏采样和必要过滤。

赛题分析：这个赛题是预测15天以内的消费行为，属于之前没遇到过的时间序列问题。并且赛题非常贴近生活。

# 比赛6 工业蒸汽量预测

比赛地址：https://tianchi.aliyun.com/competition/entrance/231693/information

数据地址：

赛题说明：蒸汽可以推动发电机旋转，产生电能。在这一些列的能量转换中，影响发电效率的核心是锅炉的燃烧效率。锅炉的燃烧效率的影响因素很多，包括锅炉的可调参数，如燃烧给量，一二次风，引风，返料风，给水水量；以及锅炉的工况，比如锅炉床温、床压，炉膛温度、压力，过热器的温度等。在本次比赛中，**经脱敏后的锅炉传感器采集的数据（采集频率是分钟级别），根据锅炉的工况，预测产生的蒸汽量。**

赛题分析：数据回归类问题，可以尝试线性回归，决策树回归，梯度提升树回归等模型进行预测。

