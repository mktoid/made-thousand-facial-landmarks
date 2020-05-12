# MADE CV Homework #1 
Thousand Facial Landmarks
https://www.kaggle.com/c/made-thousand-facial-landmarks/

Основное в решении:
сменил ResNet18 на более мощный,
нормальнизию на imagenet,
пробовал использовать Wing Loss (https://arxiv.org/pdf/1711.06753.pdf), а так же информацию из этого же пейпера, что для задачи  Facial Landmark Localisation, L1 и smooth L1 loss дают лучшее качестве чем L2.

В итоге лучшее мое решение - соло, 6 эпох, fnn.l1_loss

Команда для обучения
python hack_train.py --name "resnext101wsl 99 L1 imgnetnorm b34" --batch-size 34 --epochs 6  --data "../../data/" --gpu

![Liderboard position](https://raw.githubusercontent.com/mktoid/made-thousand-facial-landmarks/master/LB.png)
