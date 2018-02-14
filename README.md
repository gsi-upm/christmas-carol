# christmas-carol
Repository of the paper "A Carol of Love and Hate. How Christmas Polarizes Opinions in Social Media"

---

# Sentiment Lexicon

File `christmas-sedlex.txt` contains the generated sentiment lexicon, as described in the paper.
To use this lexicon, you can use [pandas](https://pandas.pydata.org/) to easily read the lexicon, and start using it:

```python
import pandas as pd

# read the lexicon
lexicon = pd.read_csv('./christmas-sedlex.txt', delimiter='\t').set_index('word')['value'].to_dict()
# and use it through a dict in python
lexicon['regalos'] # this outputs 0.59240964850835087
```
# Sentiment word counts

There are three `csv` files in this repository with the word counts in negative, positive and neutral Tweets.
The count is done over all original tweets, not taking retweets into account.
The list is limited to the most common 1000 words that are at least 3 characters long.


# Sampled tweets 

`labeled_tweets_sampled.csv` contains the count of original tweets, retweets and replies per minute and sentiment annotation.
It can be loaded in pandas as follows:

```python
import pandas as pd

labeled = pd.read_csv('labeled_tweets_sampled.csv', index_col=0, skipinitialspace=True, header=[0, 1])
```

# Citation

To be added
