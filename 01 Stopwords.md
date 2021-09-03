# Stopwords

TK add explanation of stopwords, + examples + some sample code + code we would actually use (eg NLTK)

We will be using this tweet (don't worry, we will get to train some models):

```py
tweet = """I’m amazed how often in practice, not only does a @huggingface NLP model solve your problem, but one of their public finetuned checkpoints, is good enough for the job.

Both impressed, and a little disappointed how rarely I get to actually train a model that matters :("""
```

We will be using the NLTK library for removing stopwords. NLTK comes with several stopword corpora, we will be using the English corpus. This corpus contains a huge number of English stopwords like a, the, be, for, do, and so on.

```py
from nltk.corpus import stopwords

stop_words = stopwords.words('english')

stop_words[:5]
```

Now we have a list of stopwords. When we process our text data we will iterate through each word, if it is present in stop_words it will be removed. To optimize the speed of the stopword lookup we can convert stop_words to a set object.

```py
stop_words = set(stop_words)
```
First we need to lowercase our text (because all of our stopwords are lowercased). Then we use split our input text into a list of tokens (each token is a word seperated by a space).

```py
tweet = tweet.lower().split()

tweet
```

And now we can iterate through the list, we check if each word exists in stop_words - if it does we discard it.

```py
tweet_no_stopwords = [word for word in tweet if word not in stop_words]

print("With stopwords:", ' '.join(tweet))
print("Without:", ' '.join(tweet_no_stopwords))
```

With stopwords: i’m amazed how often in practice, not only does a @huggingface nlp model solve your problem, but one of their public finetuned checkpoints, is good enough for the job. both impressed, and a little disappointed how rarely i get to actually train a model that matters :(

Without: i’m amazed often practice, @huggingface nlp model solve problem, one public finetuned checkpoints, good enough job. impressed, little disappointed rarely get actually train model matters :(

It's that easy! We'll move onto more preprocessing methods in the following sections.
