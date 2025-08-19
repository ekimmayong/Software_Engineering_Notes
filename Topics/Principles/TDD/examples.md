# TDD Examples — Python (pytest)

```python
# test_add.py
from mymodule import add

def test_add():
    assert add(2,3) == 5

# mymodule.py
def add(a,b):
    return a + b
```

Run: pytest
