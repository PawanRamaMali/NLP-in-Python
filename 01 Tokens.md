# Tokens

We breifly mentioned the word token in the last section, where I described it as a word. In some cases this is true, in others not. A token is a single unit, or piece of information. Typically in NLP we will find that models consume a token, which can represent a multitude of different things, such as:

* A word
* Part of a word
* A single character
* Puntuation mark [,!-.]
* Special token like \<URL>, or \<NAME>
* Model-specific special tokens, like [CLS] and [SEP] for BERT

Taking our previous tweet example, we can split it into word tokens using the split method:

```py
tweet = """I’m amazed how often in practice, not only does a @huggingface NLP model solve your problem, but one of their public finetuned checkpoints, is good enough for the job.

Both impressed, and a little disappointed how rarely I get to actually train a model that matters :("""

tweet.split()
```
This is the rawest form of word-level tokens, the alternative to word-level is character-level, which looks like this:

```py

[char for char in tweet][:10]
```
