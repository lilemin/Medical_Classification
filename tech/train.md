# The train/eval loss
Train loss| Test loss | Analyse
----------|-----------|--------
不断下降 |不断下降 | 网络仍在学习
不断下降 |趋于不变 | 网络过拟合
趋于不变 |不断下降 | 数据集100%有问题
趋于不变 | 趋于不变 | 学习遇到瓶颈，需要减小学习率或批量数目
不断上升 |不断上升 | 网络结构设计不当，训练超参数设置不当，数据集经过清洗等问题。

[neural-networks-3](http://cs231n.github.io/neural-networks-3/)
![](loss.png) ![](accuracy.png)
