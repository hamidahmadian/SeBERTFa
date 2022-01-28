# SeBERTFa

I use **sentence-transformers**, **transformers** and **datasets** libraries in order to create classifier for farsi sentiment analysis. there is *models* wrapper class in sentence-transformers library that is useful for loading pre-trained bert models.
so we use `pretrained_model = models.Transformer("PATH")` rather `pretrained_model = AutoModel.from_pretrained("PATH")` for loading and in this notebook [pars-bert](https://github.com/hooshvare/parsbert) is used as a pre-trained farsi model.
for measuring the performance of the model I use `f1` score on SentiPers(Multi Class) [dataset](https://github.com/JoyeBright/DeepSentiPers/tree/master/Dataset) and in this notebook we show how we could outperform the previous works ([pars-bert](https://doi.org/10.1007/s11063-021-10528-4) and [deepsentipers](https://arxiv.org/pdf/2004.05328.pdf)) by using the output of all hidden layers and getting average over them to represent the sentences.

I implement it with the using all benefits of **sentence-transformers**, **transformers** and **datasets** libraries and let these powerful libraries handle details like **training loop**, **distributed training**, **text bachify** and I just **connect** them with each other that help me without losing any customization for the problem.

Beacause of using **Se**ntence-transformers, **BERT** based pre-trained model in **Fa**rsi we call it SeBERTFa.

# Results

`f1` score on SentiPers(Multi Class) [dataset](https://github.com/JoyeBright/DeepSentiPers/tree/master/Dataset)



| Dataset | SeBERTFa | ParsBERT | DeepSentiPers |
| ----------- | ----------- | ----------- | ----------- |
| SentiPers (Multi Class) | 73.54 | 71.31 | 69.33 |
