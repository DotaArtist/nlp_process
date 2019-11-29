### RBM vs Auto encoder
```
RBM侧重于一种训练/重建的过程，一般两层。两个过程参数共享；求解过程是随机采样（gibbs）
 权重更新：W'=W+α∗CD  CD:相对熵
AE侧重与编码/解码的过程，对称的结构，至少三层，参数不一定共享。
```
- [1](https://blog.csdn.net/qq_23869697/article/details/80683163)
- [2](https://stats.stackexchange.com/questions/114385/what-is-the-difference-between-convolutional-neural-networks-restricted-boltzma)

### WMD
```
词移距离
规划问题 argmin Tij*c(i,j)

```

### SVD LSI/LSA
```
LSI主题模型，进行一次奇异值分解。高维矩阵奇异值分解计算量非常大。
SVD的求解。R(m*n) = P(m*k)*Q(k*n)  r(ui) = p(u)*q(i)^T   argmin(p,q) sum(r-p*q)^2 + a(p^2+q^2)

```

### FTRL
```
SGD + L1 稀疏性解决的不够好
TG 梯度截断，每间隔k步，在Wt绝对值小于a时，梯度减一个常数。
FOBOS 在梯度下降的基础上，添加附近权重查找和正则化。（梯度精确性高）
RDA 正则对偶平均。梯度积分中值，加正则，加辅助正则。（稀疏性好）
FTRL FOBOS+RDA。W(t+1) = argmin[w](梯度积分中值*W+L1+L2+|W-Wt|^2)

https://zhuanlan.zhihu.com/p/55135954
```

### 分布问题
```
二项分布
正态分布
卡方分布
指数分布
泊松分布

```

### 数据增强（Data Augmentation）regularization
```
大背景：
在最小化损失的前提下，只要训练数据足够，模型参数不变的情况下，经验风险最小化（ERM）一定能收敛。
另外，模型参数与训练数据一般呈正相关。

所以存在两个问题；
1.如何在模型参数不变的情况下，提高模型的学习能力；
2.训练测试数据的分布差异，导致的模型泛化能力减弱。

数据增强解决；
在现有训练集上，提高模型泛化能力，构建更加健壮的数据让模型训练。

# cutout
随机选择一个区域mask, 鼓励模型在做出决策时，考虑更多的次要特征，避免过度依赖主要特征。

# cutmix 
a.区域dropout 有助于模型捕获图片中较重要的区域；
但是区域黑化/白化/随机噪声会导致训练困难；通过裁剪粘贴的数据增强策略有助于改善这种状况。

# Shake-shake


# Mixup（2018 效果不错）
选取训练集
x_new = lambda * x_a + (1 - lambda) * x_b
y_new = lambda * y_a + (1 - lambda) * y_b

```

### AutoEncoder(自编码器)
```
# 训练技巧
Weight Tying（权重绑定）
weight tied  减缓overfitting，加速训练时间。

分层训练


```
