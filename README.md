# TextClassification--ByBERT
本次任务是对<a href="https://www.biendata.com/" target="_blank">biendata</a>“平安医疗科技疾病问答迁移学习比赛”中提供的<a href="https://www.biendata.com/competition/chip2019/data/" target="_blank">数据</a>进行的多分类实验，有diabetes，hypertension、hepatitis、aids、breast_cancer5个类别。


## Requirement
1. Python 3.7
2. PyTorch 1.3.1
3. <a href="https://github.com/huggingface/transformers" target="_blank">Transformer</a> v2.3.0


## Annotation
1. example_01：用huggingface/transformers提供的BertTokenizer,BertForSequenceClassification；
2. example_02：由于1中huggingface提供的BertTokenizer在对句子做encode的时候是基于字逐字切分的，所以我想试试按词切分的效果，引入HanLP提供的PerceptronSegmenter感知器分词，对训练集数据做切词处理，添加进BERT pre-trian model（<a href="https://storage.googleapis.com/bert_models/2018_11_03/chinese_L-12_H-768_A-12.zip" target="_blank">BERT-Base, Chinese</a>）中的vocab.txt
