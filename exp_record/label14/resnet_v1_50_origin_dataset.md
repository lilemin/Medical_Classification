# Bone marrow cells classfication
## Train the logits
### Basic condiction
Item | Vaule
-----|--------
Model | ResNet_v1_50
Label | 14
Image | Origin image without augument
Trainable variables |logits

### Experiments
#### Finetune from the origin resnet_v1_50
setp|clone|lr initial|lr decay_type|optimator|batch size|train loss|eval loss|train acc|eval acc|best model|备注
----|-----|----------|-------------|---------|----------|----------|---------|---------|--------|----------|----
1   |


## Train the logits/block1_2_3_4
### Basic condiction
Item | Vaule
-----|--------
Model | ResNet_v1_50
Label | 14
Image | Origin image without augument
Trainable variables |logits/block1_2_3_4

### Experiments
#### Finetune from the origin resnet_v1_50
setp|clone|lr initial|lr decay_type|opt|batch size|train loss|eval loss|train acc|eval acc|best model|备注
----|-----|----------|-------------|---------|----------|----------|---------|---------|--------|----------|----
1   | 2   |1e-2      | exp 0.6 10  |rmsprop  | 64       |0.518     |1.029    |65.58    |68.87   |1844      |稍微欠拟合
2   | 2   |1e-3      | exp 0.5 5   |rmsprop  | 64       |0.744     |0.86     |0.74     |68.52   |62464     |开始过拟合
3   | 2   |1e-3      | exp         |rmsprop  | 128      |0.4004    |1.011    |77.99    |69.52   |8794      |稍微过拟合
4   | 2   |1e-4      | exp         |rmsprop  | 128      |1.093     |1.023    |53.50    |59.77   |6689      |欠拟合，还没完全收敛
5   | 2   |1e-4      | fix         |rmsprop  | 128      |/         |/        |/        |/       |/         |严重过拟合，最高可达69,应该重新训练
    
    
    

## The model choiced finally
pick |acc  | name
-----|-----|----------------------------------------------------------------------------------------------------------
1    |68.52|train_dir/finetune/resnet_v1_50/pre_train/block1_2_3_4/label14/clone_2_lr_0.001_batch_64_exp_0.5_5_rmsprop
2    |69.52|train_dir/finetune/resnet_v1_50/pre_train/block1_2_3_4/label14/clone_2_lr_0.001_batch_128_exp_rmsprop
3    |67.10|train_dir/finetune/resnet_v1_50/pre_train/block1_2_3_4/label14/clone_2_lr_0.0001_batch_128_fix_rmsprop


















