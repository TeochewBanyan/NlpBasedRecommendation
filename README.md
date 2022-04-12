# README

### Recommendation system based on review analysis

#### Env:

+ colab
+ pytorch+transformer



#### Data

+ Data source: https://github.com/SophonPlus/ChineseNlpCorpus
+ df.sample(n=16000, replace=False)
  + train_df_large.csv: (12800, 2)
  + val_df_large.csv: (1600, 2)
  + test_df_large.csv: (1600, 2)

+ dataset split frac: 8-1-1



#### Model:

+ Pre-trained model "bert-base-chinese"
  + num_label: 5
  + dropout: 0.3
+ tokenization params:
  + reference: https://huggingface.co/docs/transformers/main/en/model_doc/bert#transformers.BertForMaskedLM
  + padding = True
  + truncation = True
  + token MAX_LEN: 256
+ training params:
  + batch size: 8
  + EPOCHS: 5
  + lr: 2e-5