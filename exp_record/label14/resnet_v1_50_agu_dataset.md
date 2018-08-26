# Bone marrow cells classfication
## Train the logits/blocks1_2_3_4
### Basic condiction
Item | Vaule
-----|--------
Model | ResNet_v1_50
Label | 14
Image | augument image
Trainable variables |logits/block1_2_3_4

### Experiments
#### Finetune from the origin resnet_v1_50
setp|clone|lr initial|lr decay_type|optimator|batch size|train loss|eval loss|train acc|eval acc|best model|备注
----|-----|----------|-------------|---------|----------|----------|---------|---------|--------|----------|----
1   |1    |1e-3      |exp          |rmsprop  |128       |0.3286    |0.6792   |84.99    |82.29   |23.56k    |拟合，但应该i还可以进一步提高
