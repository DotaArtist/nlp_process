## nlp research process
### automatic document summarization(自动摘要)

### semantic role labeling(语义角色标注)
- dataset:
  - FrameNet
  - PropBank
  - Chinese Proposition Bank(CPB)

### opinion extraction(观点抽取)

### adversarial examples(对抗样本)

### event extraction(事件抽取)

### relation extraction(关系抽取)
- dataset:
  - https://nlp.stanford.edu/projects/tacred/
- code:
  - https://github.com/roomylee/awesome-relation-extraction
  - https://github.com/thunlp/NRE
- other:
  - http://nlpprogress.com/english/relationship_extraction.html
  - https://shomy.top/2018/02/28/relation-extraction/
- model:
  - CRCNN(Classifying Relations by Ranking with CNN)
  - PCNN(Piece Wise CNN)

### machine reading comprehension(阅读理解)
- dataset:
  - http://www.qizhexie.com/data/RACE_leaderboard.html

### semantic textual similarity(语义文本相似)
- dataset:
  - [MRPC(Microsoft Research Paraphrase Corpus)](https://www.microsoft.com/en-us/download/details.aspx?id=52398)
  - [QQP(Quora Question Pairs)](https://www.quora.com/q/quoradata/First-Quora-Dataset-Release-Question-Pairs)
  - [lcqmc](http://icrc.hitsz.edu.cn/info/1037/1146.htm)
  - https://dc.cloud.alipay.com/index?click_from=MAIL&_bdType=acafbbbiahdahhadhiih#/topic/intro?id=3
- code:
  - https://github.com/terrifyzhao/text_matching

### named entity recognition(命名实体识别)/Slot Filling(槽填充)

### text classification(文本分类)
- other:
  - https://github.com/ChenChengKuan/awesome-text-generation

### sentiment Analysis(情感分析)
- dataset:
  - [sst](http://ai.stanford.edu/~amaas/data/sentiment/)

### machine translation(机器翻译)

### text generation(文本生成)
-

### knowledge graph(知识图谱)
- dataset:
  - http://openkg.cn/dataset/symptom-in-chinese

### entity linking(实体链接)

### dependency parsing(依存句法分析)
- other:
  - http://nlpprogress.com/english/dependency_parsing.html

### textual entailment(文本蕴含)
- dataset:
  - [MNLI(Multi-Genre Natural Language Inference)](http://www.nyu.edu/projects/bowman/multinli/)

### question answering(问答)
- dataset:
  - https://rajpurkar.github.io/SQuAD-explorer/

## transfer learning(迁移学习)
- dataset:
  - https://github.com/brightmart/roberta_zh

## graph neural network(图网络)
- other
  - https://github.com/rusty1s/pytorch_geometric

## overall info


### process
- https://github.com/sebastianruder/NLP-progress

### task
- semeval
- ccks task
- https://cloud.tencent.com/developer/article/1117928

### data
- http://www.xuwei.io/2018/11/30/文本分类-glue数据集介绍/
- https://www.jiqizhixin.com/articles/062402

### tools
- [ner for label](https://rasahq.github.io/rasa-nlu-trainer/)
- [tmVar for api](https://www.ncbi.nlm.nih.gov/research/bionlp/Tools/tmvar/)
- [re for label](http://brat.nlplab.org/installation.html)

### 中文评测任务
- 讯飞杯
  - 举办了三届。阅读理解。
- 法研杯
  - 文本匹配，实体抽取，阅读理解。
- ccks(全国知识图谱与语义计算大会)
  - 关系抽取，实体抽取。
- 看山杯
  - 举办了三届。
