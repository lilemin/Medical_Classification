# Bone marrow cells classfication
## Train the logits/block1_2_3_4
### Basic condiction
Item | Vaule
-----|--------
Model | ResNet_v1_50
Label | 6_1
Image | Origin image without augument
Trainable variables |logits/block1_2_3_4

### Experiments
#### Finetune from the origin resnet_v1_50
setp|clone|lr initial|lr decay_type|optimator|batch size|train loss|eval loss|train acc|eval acc|best model|备注
----|-----|----------|-------------|---------|----------|----------|---------|---------|--------|----------|----
1   |1    |1e-3      | exp         |rmsprop  |128       |0.2322    | 0.3057  |87.95    |82.90   |10565     |拟合























