# YouOnlyLockOnce

基于YOLOv5的FPS外挂锁头系统

## 项目介绍

YouOnlyLockOnce是一个基于YOLOv5的FPS外挂锁头系统，可以帮助FPS玩家快速锁定目标，该项目仅供学习，请公平游戏，不要作弊

## 项目特点

- 采用mss进行实时屏幕采集
- 可以自由使用YOLOv5的预训练模型进行训练，理论上适配所有FPS
- 采用YOLOv5s微调模型进行目标检测，速度快，精度高
- 除了FPS外挂锁头系统，还可以用于其他场景，比如工业检测、智能安防等
- 项目架构简单，易于上手，适合初学者学习


## 快速开始

### 环境准备

- Python 3.10
- Pytorch 2.3.0
- CUDA 12.4
- CUDNN 8.2.4
- 使用**pip install -r requirements.txt**安装依赖

### 训练模型

- 下载YOLOv5s预训练模型，放入model文件夹
- 运行train.py脚本，修改参数进行训练，指令如下：
  !python train.py --batch-size 2 --epochs 200 --data det_data/data.yaml --weights weight/yolov5s.pt
- 训练完成后，会在runs文件夹下生成对应的权重文件，将其放入model文件夹下

### 运行程序
- 运行detect5.py脚本，修改参数进行运行，指令如下：
  !python detect5.py