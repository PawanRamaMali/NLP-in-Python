# Stopwords

TK add explanation of stopwords, + examples + some sample code + code we would actually use (eg NLTK)

We will be using this tweet (don't worry, we will get to train some models):

```
tweet = """I’m amazed how often in practice, not only does a @huggingface NLP model solve your problem, but one of their public finetuned checkpoints, is good enough for the job.

Both impressed, and a little disappointed how rarely I get to actually train a model that matters :("""
```

We will be using the NLTK library for removing stopwords. NLTK comes with several stopword corpora, we will be using the English corpus. This corpus contains a huge number of English stopwords like a, the, be, for, do, and so on.

```py
from nltk.corpus import stopwords

stop_words = stopwords.words('english')

stop_words[:5]
```
