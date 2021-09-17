
## Sentiment with Flair

Flair offers models that we can use out-of-the-box. One of those is the English sentiment model, which we will learn how to use here.

First, we need to make sure Flair has been installed, we do this in our CLI with:

pip install flair
Flair uses PyTorch/TensorFlow in under the hood, so it's essential that you also have one of the two libraries (or both) installed. There are a few steps in applying sentiment analysis, these are:

Initializing the model.

Tokenizing input text.

Processing with the model.

(Optional) Formatting the outputs.

We then load the English sentiment model like so:

```py
import flair
model = flair.models.TextClassifier.load('en-sentiment')
```

```
text = "I like you. I love you"  # we are expecting a confidently positive sentiment here

sentence = flair.data.Sentence(text)

sentence
```

```
sentence.to_tokenized_string()
```

```
model.predict(sentence)
```

```
sentence
```

```
text = "I hate it when I'm not learning"
sentence = flair.data.Sentence(text)
model.predict(sentence)
sentence
```

```
sentence.get_labels()
```

```
sentence.get_labels()[0]
```

```
sentence.get_labels()[0].score
```

```
sentence.get_labels()[0].value
```

```
sentence.labels[0].score, sentence.labels[0].value
```






