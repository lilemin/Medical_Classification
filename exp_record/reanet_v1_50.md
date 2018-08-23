# ResNet_v1_50
## Basic Condition
Item | Value
-----|------
model | resnet_v1_50
image | origin dataset without augument
label | 14
## Experiments
Item | Train loss |Eval loss |Train acc |Eval acc
-----|------------|----------|----------|--------
clone_2_lr_0.1_batch_256_fix_rmsprop|1.880|1.650|48.62|53.65
clone_2_lr_0.1_0.01_batch_256_64_fix_rmsprop| | | | |
clone_2_lr_0.1_0.01_0.001_batch_256_64_fix_rmsprop|0.08|1.261|95.35|69.94
clone_2_lr_0.1_0.01_0.001_0.0001_batch_256_64_fix_rmsprop|clone_2_lr_0.1_0.01_0.001_batch_256_64_fix_rmsprop/model.ckpt-2456|
