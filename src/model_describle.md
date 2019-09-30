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
### Text Generation
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

### Dependency parsing
- http://nlpprogress.com/english/dependency_parsing.html
```
# process
- CFG
- Penn Treebank + HPSG Parser
- Penn Treebank tree :Head rules
- GNN

```