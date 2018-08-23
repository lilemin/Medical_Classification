# ResNet_v1_50
## Train the logits
### Basic Condition
Item | Value
-----|------
model | resnet_v1_50
image | origin dataset without augument
label | 14
trainable | logits

### Experiments1
Item | Train loss |Eval loss |Train acc |Eval acc
-----|------------|----------|----------|--------
clone_2_lr_0.1_batch_256_fix_rmsprop|1.880|1.650|48.62|53.65
clone_2_lr_0.1_0.01_batch_256_64_fix_rmsprop| | | | |
clone_2_lr_0.1_0.01_0.001_batch_256_64_fix_rmsprop|0.08|1.261|95.35|**69.94**
clone_2_lr_0.1_0.01_0.001_0.0001_batch_256_64_fix_rmsprop|clone_2_lr_0.1_0.01_0.001_batch_256_64_fix_rmsprop/model.ckpt-2456|

## Train the blocks
### Basic Condition
Item | Value
-----|------
model | resnet_v1_50
image | origin dataset without augument
label | 14
trainable | logits, block4
## Experiments1
Item | Train loss |Eval loss |Train acc |Eval acc| Best model| 备注
-----|------------|----------|----------|--------|------------|-----
clone_2_lr_0.1_batch_64_fix_rmsprop|0.7404|1.046|68.03|64.52|3584|准确率可以比前面的实验都提升得快，但2个测试后，就过拟合
clone_2_lr_0.01_batch_64_fix_rmsprop|0.4328|1.681|68.50|62.45|3407|严重过拟合
clone_2_lr_0.001_batch_64_fix_rmsprop|0.4215|0.8843|75.42|66.65|14.35k|
clone_2_lr_0.0001_batch_64_fix_rmsprop|