# 孪生LSTM网络(Siamese-LSTM)
本项目是基于孪生LSTM网络+注意力机制+曼哈顿距离(Manhattan distance)实现的句对相似度计算。<br>
中文训练数据为蚂蚁金服句对数据，约4万组，正负样本比例1:3.6；英文训练数据来自Kaggle上的Quora句对数据，约40万组，正负样本比例1:1.7。
![](https://cloud.githubusercontent.com/assets/9861437/20479493/6ea8ad12-b004-11e6-89e4-53d4d354d32e.png)

## 资料
- 参考文献
    - [Siamese Recurrent Architectures for Learning Sentence Similarity](http://www.mit.edu/~jonasm/info/MuellerThyagarajan_AAAI16.pdf)
    - [How to predict Quora Question Pairs using Siamese Manhattan LSTM](https://medium.com/mlreview/implementing-malstm-on-kaggles-quora-question-pairs-competition-8b31b0b16a07)
    - 中国大陆可能无法访问《How to predict...Manhattan LSTM》一文，请直接查看本项目中附件之参考博客
- 其它数据
    - 英文词向量：[GoogleNews-vectors-negative300.bin.gz](https://drive.google.com/file/d/0B7XkCwpI5KDYNlNUTTlSS21pQmM/edit?usp=sharing)
    - 英文词向量：[GoogleNews-vectors-negative300.bin.gz的百度网盘地址](https://pan.baidu.com/s/1dEENGPV)
    - 中文词向量：[基于120G中文语料训练的64维、128维词向量](https://weibo.com/p/23041816d74e01f0102x77v)
- 工程参考
    - [likejazz/Siamese-LSTM](https://github.com/likejazz/Siamese-LSTM) Original author's GitHub
    - [做个聊天机器人/智能客服](https://zhuanlan.zhihu.com/p/31638132) 一些网络设计思路

## 使用
### 训练
```
$ python3 train.py
$ type cn for Chinese Data or en for English Data
```

### 预测
```
$ python3 predict.py
$ type cn for Chinese Data or en for English Data
```

### 效果
```
$ 根据数据比例来看，中文训练集的基准准确率应为0.78，英文为0.63
$ 英文数据在GoogleNews300维词向量上的实际训练效果为0.80
$ 中文数据在120G语料的128维词向量上的实际训练效果为0.80，几乎没有效果，和英文形成鲜明对比；可能是因为蚂蚁金服数据句子太相似了，领域太狭窄
```
