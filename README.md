# README

### Recommendation system based on review analysis

#### Env:

+ colab
+ pytorch+transformer



#### Data

+ Data source: https://github.com/SophonPlus/ChineseNlpCorpus
+ df.sample(n=16000, replace=False)

+ preprocess: 

  + manually revise the inconsistency between comments and ratings

    ![](./img/inconsistency/fig1.png)

  + dataset split

    +  frac: 8-1-1

#### Model:

+ Pre-trained model "bert-base-chinese"
  + num_label: 5
  + dropout: 0.2
+ tokenization params:
  + reference: https://huggingface.co/docs/transformers/main/en/model_doc/bert#transformers.BertForMaskedLM
  + padding = True
  + truncation = True
  + token MAX_LEN: 512
+ training params:
  + batch size: 16
  + EPOCHS: 5
  + lr: 1e-5