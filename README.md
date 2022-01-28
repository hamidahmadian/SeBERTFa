# SeBERTFa

I use **sentence-transformers**, **transformers** and **datasets** libraries in order to create classifier for farsi sentiment analysis. there is *models* wrapper class in sentence-transformers library that is useful for loading pre-trained bert models.
so we use `pretrained_model = models.Transformer("PATH")` rather `pretrained_model = AutoModel.from_pretrained("PATH")` for loading and in this notebook pars-bert is used as a pre-trained farsi model.
for measuring the performance of the model I use `f1` score on 
