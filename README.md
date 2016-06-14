
# Today I Learned #

*A log of things I learn as I learn them.*

I'm going to try to commit to keeping this log. I want to post occassional
summaries of things I learned relating to math, programming, and similar topics.

## Recent #

### Python Dictionary Comprehensions #

*2016 Jun 14*

I learned that you can use dictionary comprehesions that same as a list
comprehesion.

For example, it is easy to create the following list:

```python
import random
number_list = [random.randint(1,5)for i in range(0,10)]
```

This yields the list: 2, 5, 3, 4, 5, 3, 2, 5, 4, 3.

What I didn't realize before was that you can use similar shorthand to create
a dictionary:

```python
number_dict = {e:number_list.count(e)for e in range(1,6)}
```

This yields the dictionary:

| Key | Value |
| --- | --- |
| 1 | 0 |
| 2 | 2 |
| 3 | 3 |
| 4 | 2 |
| 5 | 3 |