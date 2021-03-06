### cnn 参数计算
```
卷积层参数： (width * heigth * input_depth * filter_num) + filter_num 
```

### lstm 参数计算
```
 
```

### adversarial attack and defence
```
增强系统稳定性

1.对抗训练，加入对抗样本，增加模型鲁棒性；(缺点 分类边界会变大，分类能力变差)
2.对抗样本检测器；

攻击：
1.边界探测攻击
2.生成模型（gan）
3.梯度攻击

防御：
1.数据增广（范围和强度覆盖不全）
2.梯度正则
3.对抗检测（分类器识别是否为攻击）

常见场景：
1.人脸比对(1:1 阈值问题, 1:N 样本和top2更近) 

FGSM(快速梯度符号法)
GAN（攻击上限更高）
IPGD（攻击更稳定和可浮现）

对抗攻击与防御的评估方式：

targeted attack vs untargeted attack

其他参考：
- https://juejin.im/post/5cff1b5ae51d4556bc066f45
- [图像对抗攻击演示](https://distill.pub/2018/building-blocks/)
```


### relation extract
- https://shomy.top/2018/02/28/relation-extraction/
```
# tricks
tokens : 今天天气很好===> 今天<e>天气</e>很好
lexical-feature：实体词，实体左右的词，wordnet中实体词的上位词（实体类型）
Position feature : 每个词到多个实体词的相对距离
Position Indicator： 
Ranking Loss：输入句子，正确标签，错误标签

PCNN: position encodong + cnn
PCNN: Piece Wise CNN(实体分n段池化，每个卷积核对应n个池化结果)
APCNN : pcnn + attention
```

### text Generation
- 
```
# process
seqGAN： 梯度消失，模型崩塌
WGAN
MaliGAN
RankGAN
DP-GAN
LeakGAN
```

### LSTM CRF
```
softmax vs crf:前者是n个k分类问题，后者是1个n^k分类问题；

https://kexue.fm/archives/5542
```

### dependency parsing
- http://nlpprogress.com/english/dependency_parsing.html
```
# process
- CFG 上下文无关语法。终结符/非终结符/生成式
- Penn Treebank + HPSG Parser
- Penn Treebank tree :Head rules
- GNN
- 常见的依存句法 https://blog.csdn.net/glory1234work2115/article/details/54906343

PCFG Parser stanford corenlp demo: 
(ROOT
  (NP
    (NP (NR 中华) (NN 人民) (NN 共和国))
    (PRN (PU ()
      (NP (NR 中国))
      (PU ))
      (VP
        (ADVP (AD 很))
        (VP (VA 强大))
	  )
	)
  )
)

Shift-Reduce Parser
```

### sentence dependency parsing
```
语义依存分析
```

### seq2seq
```
teacher forcing  train时decoder的输入替换为真实输入，1.加快收敛速度;2.防止prior time steps error;  
beam searching  test时，在k时刻取词表L中top_k作为这个时刻的输出，下一个时刻在k*l 中取top_k，依次循环。（剪枝的深度搜索策略）
```

### short text similarity
```
esim: siamese network (embedding + bilstm_a + attention(sentence_1, sentence_2) + interaction(f1,f2) + max/min + fc)
drcn: siamese network (embedding + feature + interaction(p,q) + ae) + fc
```

### semantic role labeling
```
以句子为单位，分析句子的谓词-论元结构  格语法
```

### VAE
```
x ---> 两个encoder分别计算var/mean ---> 采样normal distribution ---> 采样变换reparameterization得到z --- > decorder
loss = log(p) + kl(q|p)  # reparameterization 和 kl（噪声） 相互对抗
reparameterization trick

1.计算x的均值和方差；
2.正态分布采样；
3.变换到原分布上，采样变换 reparameterization；

变分和贝叶斯理论
两个encoder的作用：
1.均值+高斯噪声
2.方差+高斯噪声
loss = p*log(q) + (mean^0.5 - sigma + (exp(0.5 * sigma) - 1))

CVAE 条件变分自编码
encoder Y类别均值，采样变换加入z
```

### WGAN
```
EM距离（Wasserstein）
weight clipping vs gradient penalty 

self.Y = tf.placeholder(tf.float32, shape=[None, *self.image_size], name='output')
self.z = tf.placeholder(tf.float32, shape=[None, self.flags.z_dim], name='latent_vector')

self.g_samples = self.generator(self.z)
_, d_logit_real = self.discriminator(self.Y)
_, d_logit_fake = self.discriminator(self.g_samples, is_reuse=True)

# discriminator loss
self.d_loss = tf.reduce_mean(d_logit_real) - tf.reduce_mean(d_logit_fake)
# generator loss
self.g_loss = -tf.reduce_mean(d_logit_fake)

同时优化 g_loss, d_loss
```

### Pointer-Generator
```

```

### automatic document summarization
```
抽取式评价指标：Edmundson 匹配句子数量。重合率p = 匹配句子/专家文摘句子

摘要式评价指标: ROUGE 
ROUGE-N(N=1、2、3、4，分别代表基于1元词到4元词的模型)，ROUGE-L，ROUGE-S, ROUGE-W，ROUGE-SU

```

### gpt/gpt-2
```
训练方式是无监督的，预测下个单词。
特定任务效果差，例如分类，抽取，问答。
通用领域，机器翻译，摘要，文本生成器，代词消解。

```