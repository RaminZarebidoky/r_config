# r_config

a customized way to use config

## usage:

#### from str:

```python
from r_config import RConfig

rc = RConfig()

str_yaml = """
    yek:
      ramin: 2
      mehran: 'salam'
    # comment to test
    dow:
      se:
        p1: 2.2
      f1: 'khodafez'
"""

rc.update_from_str(str_yaml)

```

#### from file:

```python
from r_config import RConfig
from pathlib import Path

rc = RConfig()

path = Path('/path/to/config.yaml')

rc.update_from_file(path)

```

#### from dict:

```python
from r_config import RConfig

r_dict = {'a': 10, 'b': 'salam', 'f': {'p': 2, 'q': 3}}

rc = RConfig(r_dict)

```