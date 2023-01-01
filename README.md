# 神经网络与深度学习课程设计--Wasserstein GAN

=================================

# 实验环境
- python
- pytorch
- torchvision
- lmdb
- 相关环境和包可以通过pip或conda自行安装，详情查看requirements.txt文件。

# 数据集下载
- Cifar10： http://www.cs.toronto.edu/~kriz/cifar.html pytorch可以自动下载。
- LSUN：http://dl.yf.io/lsun/scenes/  需要手动下载。
如果使用LSUN，将下载好后的路径参数传给--dataroot

# 运行方式
### 使用cifar10数据集
```bash
python main.py --dataset cifar10 --dataroot [数据集路径] --cuda
```
### 使用LSUN数据集
```bash
python main.py --dataset lsun --dataroot [数据集路径] --cuda
```
### 使用训练得到的配置文件与权值参数，生成指定数量的图片
```bash
python generate.py -c samples\generator_config.json -w samples\netG_epoch_49.pth -o [保存路径] -n [图片数量] --cuda
```
其他更多参数设置请看代码

# 实验结果
### 学习率对比实验：
![image](https://github.com/sjh126/nnet/blob/main/pic/0.00001.png)
![image](https://github.com/sjh126/nnet/blob/main/pic/25new.png)
![image](https://github.com/sjh126/nnet/blob/main/pic/0.0001.png)
### Adam:
![image](https://github.com/sjh126/nnet/blob/main/pic/adam.png)
### improved_resuit:
![image](https://github.com/sjh126/nnet/blob/main/pic/improved_result.jpg)



