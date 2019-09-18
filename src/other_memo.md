### RBM vs Auto encoder
```
RBM侧重于一种训练/重建的过程，一般两层。两个过程参数共享；求解过程是随机采样（gibbs）
 权重更新：W'=W+α∗CD  CD:相对熵
AE侧重与编码/解码的过程，对称的结构，至少三层，参数不一定共享。
```
- [1](https://blog.csdn.net/qq_23869697/article/details/80683163)
- [2](https://stats.stackexchange.com/questions/114385/what-is-the-difference-between-convolutional-neural-networks-restricted-boltzma)