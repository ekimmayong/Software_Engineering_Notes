# FP Examples — Python

```python
# pure function
def add(a, b):
    return a + b

# higher-order function
def apply_twice(f, x):
    return f(f(x))

print(apply_twice(lambda x: x*2, 3))  # 12

# avoid shared mutable state
from copy import deepcopy

def update_user(user, new_name):
    u = deepcopy(user)
    u['name'] = new_name
    return u
```
