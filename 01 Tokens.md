# Tokens

We breifly mentioned the word token in the last section, where I described it as a word. In some cases this is true, in others not. A token is a single unit, or piece of information. Typically in NLP we will find that models consume a token, which can represent a multitude of different things, such as:

* A word
* Part of a word
* A single character
* Puntuation mark [,!-.]
* Special token like \<URL>, or \<NAME>
* Model-specific special tokens, like [CLS] and [SEP] for BERT

Taking our previous tweet example, we can split it into word tokens using the split method:
