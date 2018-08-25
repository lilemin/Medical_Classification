# Bone marrow cells classfication
## Train the logits/block1_2_3_4
### Basic condiction
Item | Vaule
-----|--------
Model | ResNet_v1_50
Label | 8_1
Image | Origin image without augument
Trainable variables |logits/block1_2_3_4

### Experiments
#### Finetune from the origin resnet_v1_50
setp|clone|lr_initial|lr_decay_type|optimator|batch_size|train loss|eval loss|train acc|eval acc|best model|备注
----|-----|----------|-------------|---------|----------|----------|---------|---------|--------|----------|-----
1   |1    |1e-3      |exp          |rmsprop  |128       |0.2879    |0.5477   |78.80    |78.28   |6013      |基本拟合，略欠拟合
2   |1    |1e-4      |exp          |rmsprop  |128       |
 
