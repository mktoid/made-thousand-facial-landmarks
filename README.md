# MADE CV Homework #1 

http://data.mail.ru/

Thousand Facial Landmarks
https://www.kaggle.com/c/made-thousand-facial-landmarks/

Основное в решении:
resnext101wsl,
нормализация imagenet,
пробовал использовать Wing Loss (https://arxiv.org/pdf/1711.06753.pdf), а так же информацию из этого же пейпера, что для задачи  Facial Landmark Localisation, L1 и smooth L1 loss дают лучшее качестве чем L2.

Аугментации (яркость/контраст/affine) - не улучшили

В итоге решение - соло, 6 эпох, l1_loss

Команда для обучения
python hack_train.py --name "resnext101wsl 99 L1 imgnetnorm b34" --batch-size 34 --epochs 6  --data "../../data/" --gpu

![Liderboard position](https://raw.githubusercontent.com/mktoid/made-thousand-facial-landmarks/master/LB.png)
