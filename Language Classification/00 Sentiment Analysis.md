
## Sentiment Analysis

Sentiment analysis is one of the most widely used applications of NLP. It consists of a language classification task where our goal is to classify positive, negative, and neutral sentiments. Given the following three statements we would aim to identify whether each is good, bad, or neutral:

* GBP rallies after stronger than ever economic performance.
* GBP slips on fears of a divided economy.
* GBP is one of several European currencies.


When reading each of these examples, we percieve an overall feeling (the sentiment) behind each statement. The first sounds like great news, and so we see this as a positive statement. For the second statement, things seem more bleak, and so we perceive a more negative feeling. The final statement has neither positive nor negative connatations - it is simply a factual statement.

From this, we can say that statement (1) has a positive sentiment, (2) is negative, and (3) is neutral.

The typical flow of information through a sentiment classification model consists of four steps:

1. Raw text data is tokenized (converted into numerical IDs that map that word to a vector representation of the same word)

2. Token IDs are fed into the sentiment model

3. A set of values are output, each value represents a class, and the value represents probability of that being the correct sentiment class, from zero (definitely not) to one (definitely yes).

4. The argmax of this output array is taken to give us our winning sentiment classification.

We do not always have the three outputs classes [positive, negative, and neutal], often we will find models that predict just [positive, negative], or models that are more granular [very positive, somewhat positive, neutral, somewhat negative, very negative]. We can change the number of outputs classes (step 3) to fit to the correct number of classes.
