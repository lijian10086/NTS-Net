# NTS-Net

This is a PyTorch implementation of the ECCV2018 paper "Learning to Navigate for Fine-grained Classification" (Ze Yang, Tiange Luo, Dong Wang, Zhiqiang Hu, Jun Gao, Liwei Wang).

## Requirements
- python 3+
- pytorch 0.4+
- numpy
- datetime

## Datasets
Download the [CUB-200-2011](http://www.vision.caltech.edu/visipedia-data/CUB-200-2011/CUB_200_2011.tgz) datasets and put it in the root directory named **CUB_200_2011**, You can also try other fine-grained datasets.

## Train the model
If you want to train the NTS-Net, just run ``python train.py``. You may need to change the configurations in ``config.py``. The parameter ``PROPOSAL_NUM`` is ``M`` in the original paper and the parameter ``CAT_NUM`` is ``K`` in the original paper. During training, the log file and checkpoint file will be saved in ``save_dir`` directory. You can change the parameter ``resume`` to choose the checkpoint model to resume.

## Test the model
If you want to test the NTS-Net, just run ``python test.py``. You need to specify the ``test_model`` in ``config.py`` to choose the checkpoint model for testing.

## Model
We also provide the checkpoint model trained by ourselves, you can download it from [here](https://drive.google.com/file/d/1F-eKqPRjlya5GH2HwTlLKNSPEUaxCu9H/view?usp=sharing). If you test on our provided model, you will get a 87.6% test accuracy.

## Reference
If you are interested in our work and want to cite it, please acknowledge the following paper:

```
@inproceedings{Yang2018Learning,
author = {Yang, Ze and Luo, Tiange and Wang, Dong and Hu, Zhiqiang and Gao, Jun and Wang, Liwei},
title = {Learning to Navigate for Fine-grained Classification},
booktitle = {ECCV},
year = {2018}
}
```
## 李剑备注：
1.https://zhuanlan.zhihu.com/p/62106844?utm_source=wechat_session&utm_medium=social&utm_oi=589576447262199808 本代码的博文：细粒度识别之 Learning to Navigate
2.https://github.com/lijian10086/NTS-Net-keras keras版本的源码
