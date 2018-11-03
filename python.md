# python

## How to convert a nested OrderedDict to dict?
```
from json import loads, dumps
from collections import OrderedDict

def to_dict(input_ordered_dict):
    return loads(dumps(input_ordered_dict))
```
