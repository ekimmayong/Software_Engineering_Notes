# OOP Examples — Python

Run these examples in a Python REPL or save them in files and run with python3.

1. Classes & Instances

```python
class User:
    def __init__(self, username, email):
        self.username = username
        self.email = email

    def greet(self):
        return f"Hello, {self.username}!"

u = User('alice', 'alice@example.com')
print(u.greet())
```

2. Encapsulation with properties

```python
class BankAccount:
    def __init__(self, owner, balance=0):
        self._owner = owner
        self._balance = balance

    @property
    def balance(self):
        return self._balance

    def deposit(self, amount):
        if amount <= 0:
            raise ValueError('amount must be positive')
        self._balance += amount

acc = BankAccount('Bob')
acc.deposit(100)
print(acc.balance)
```

3. Inheritance and method overriding

```python
class Animal:
    def speak(self):
        return '...'

class Dog(Animal):
    def speak(self):
        return 'woof'

class Cat(Animal):
    def speak(self):
        return 'meow'

for a in (Dog(), Cat()):
    print(a.speak())
```

4. Polymorphism and duck typing

```python
class JSONSerializable:
    def to_json(self):
        raise NotImplementedError

class Person(JSONSerializable):
    def __init__(self, name):
        self.name = name

    def to_json(self):
        import json
        return json.dumps({'name': self.name})

# function using duck typing
def serialize(obj):
    return obj.to_json()

print(serialize(Person('Eve')))
```

5. Using Abstract Base Classes (ABC)

```python
from abc import ABC, abstractmethod

class Repository(ABC):
    @abstractmethod
    def save(self, obj):
        pass

class InMemoryRepo(Repository):
    def __init__(self):
        self._items = []

    def save(self, obj):
        self._items.append(obj)

repo = InMemoryRepo()
repo.save({'id': 1})
```
