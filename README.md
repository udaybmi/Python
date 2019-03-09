# Python


#### converting df to lower
```
data=data.apply(lambda x: x.astype(str).str.lower())
```
####  Turn a Unicode string to plain ASCII
```

import unicodedata
import string

all_letters = string.ascii_letters + " .,;'"
n_letters = len(all_letters)
def unicode_to_ascii(s):
    return ''.join(
        c for c in unicodedata.normalize('NFD', s)
        if unicodedata.category(c) != 'Mn'
        and c in all_letters
    )

print(unicode_to_ascii('Ślusàrski'))
```
