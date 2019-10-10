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
FTRL FOBOS+RDA。W(t+1) = argmin[w](梯度积分中值+L1+L2+|W-Wt|^2)
```
