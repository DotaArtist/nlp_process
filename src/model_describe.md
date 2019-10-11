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

```

### semantic role labeling
```
以句子为单位，分析句子的谓词-论元结构  格语法
```

### VAE
```
x ---> 两个encoder分别计算var/mean ---> 采样normal distribution ---> 采样变换reparameterization --- > decorder
loss = log(p) + kl(q|p)  # reparameterization 和 kl（噪声） 相互对抗
reparameterization trick
```

### WGAN
```

```
