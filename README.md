# SeBERTFa

I use **sentence-transformers**, **transformers** and **datasets** libraries in order to create classifier for farsi sentiment analysis. there is *models* wrapper class in sentence-transformers library that is useful for loading pre-trained bert models.
so we use `pretrained_model = models.Transformer("PATH")` rather `pretrained_model = AutoModel.from_pretrained("PATH")` for loading and in this notebook [pars-bert](https://github.com/hooshvare/parsbert)is used as a pre-trained farsi model.
for measuring the performance of the model I use `f1` score on SentiPers(Multi Class) [dataset](https://github.com/JoyeBright/DeepSentiPers/tree/master/Dataset) and in this notebook we show how we could outperform the previous works (pars-bert and deepsentipers) by using the output of all hidden layers and getting average over them to represent the sentences.
