# ResNet_v1_50
## Train
* 采用细胞增强数据集，微调resnet_v1_50的logits层，得出最优模型
* 采用细胞增强数据集，
## Exp1
### Condition
Item | Value
------|--------
Model | ResNet_v1_50
Image | Augument image
Optimazer | Adam
Trainable variables | logits


### Experiment Results
Item |Finetune model| Train acc | Eval acc | Train loss | Eval loss| Remark
-----|--------------|-----------|----------|------------|----------|--------
clone_2_lr_0.1_batch_256_fix | resnet_v1_50.ckpt |53.29|52.42|1.211|1.442|欠拟合
clone_2_lr_0.1_0.01_batch_256_128_fix | clone_2_lr_0.1_batch_256_fix/model.cpkt-6103 |74.57|66.48|0.2683|0.9717|开始过拟合
clone_2_lr_0.1_0.01_0.001_batch_256_128_fix|clone_2_lr_0.1_0.01_batch_256_128_fix/model.ckpt-3926
