# CSRNet_paddle

Paper: Conditional Sequential Modulation for Efficient Global Image Retouching.

[Paper](https://paperswithcode.com/paper/conditional-sequential-modulation-for-1)

作者: Jingwen He等

Paddle 复现版本

## 数据集

非原数据集，对照为hdrtvnet论文数据

https://pan.baidu.com/s/1OSLVoBioyen-zjvLmhbe2g

提取码: 2me9

## 训练模型

最优权重:

链接：https://pan.baidu.com/s/1j5qy_cQscpvDpuzVNe9Y8A?pwd=hh66 
提取码：hh66

## 训练步骤

### train 

```bash
python train.py -opt config/train/train_CSRNet.yml
```

```
多卡仅需
​```bash
python -m paddle.distributed.launch train.py --launcher fleet -opt config_file_path
```

## 测试步骤

```bash
python test.py -opt config/test/test_CSRNet.yml
```

## 复现指标

|        | PSNR  |
| ------ | ----- |
| Paddle | 37.36 |

注：因显存限制，测试结果为测试图片降采样到1080p的结果 