# README

### Recommendation system based on review analysis

#### Env:

+ colab
+ pytorch+transformer



#### Data

+ Data source: https://github.com/SophonPlus/ChineseNlpCorpus
+ dataset split frac: 8-2-2



#### Model:

+ Pre-trained model "bert-base-chinese"
  + num_label: 5
  + dropout: 0.1
+ tokenization params:
  + reference: https://huggingface.co/docs/transformers/main/en/model_doc/bert#transformers.BertForMaskedLM
  + padding = True
  + truncation = True
  + token MAX_LEN: 256
+ training params:
  + batch size: 16
  + EPOCHS: 5
  + lr: 2e-5