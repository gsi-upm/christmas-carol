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

# Citation

To be added
