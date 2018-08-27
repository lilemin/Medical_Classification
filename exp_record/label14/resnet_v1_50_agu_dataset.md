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
1   |1    |1e-3      |exp          |rmsprop  |128       |0.3286    |0.6792   |84.99    |82.29   |23.56k    |拟合，有待优化
**2   |1    |1e-2      |exp          |rmsprop  |128       |0.03862   |0.4714   |88.41    |87.00   |10.19k   |前面效果很好，但稍过拟合**
4   |1    |1e-2      |exp 0.8      |rmsprop  |128       |

#### Finetune from the pre-trained resnet_v1_50
setp|clone|lr initial|lr decay_type|optimator|batch size|pre_trained model|train loss|eval loss|train acc|eval acc|best model|备注
----|-----|----------|-------------|---------|----------|----------|----------|---------|---------|--------|----------|----
3   |1    |1e-4      |exp          |rmsprop  |128       |setp2/model.ckpt-10578| | | | | |最新的模型已经过拟合很严重了，该换模型微调
