# SOLID Examples — Python

1. SRP (Single Responsibility)

```python
# SRP: separate persistence from business logic
class UserRepository:
    def __init__(self):
        self._storage = {}
    def save(self, user):
        self._storage[user['id']] = user

class UserService:
    def __init__(self, repo):
        self.repo = repo
    def register(self, user):
        # business rules
        self.repo.save(user)

repo = UserRepository()
service = UserService(repo)
service.register({'id':1, 'name':'Alice'})
```

2. OCP (Open/Closed)

```python
from abc import ABC, abstractmethod

class Formatter(ABC):
    @abstractmethod
    def format(self, data):
        pass

class JSONFormatter(Formatter):
    def format(self, data):
        import json
        return json.dumps(data)

class XMLFormatter(Formatter):
    def format(self, data):
        # simplified example
        return '<data>' + str(data) + '</data>'

# extend by adding a new Formatter without modifying existing code
formatters = [JSONFormatter(), XMLFormatter()]
for f in formatters:
    print(f.format({'x':1}))
```

3. LSP (Liskov Substitution)

```python
class Bird:
    def fly(self):
        print('flying')

class Sparrow(Bird):
    pass

# avoid forcing non-flying birds to implement fly; use composition or separate interfaces
class Ostrich(Bird):
    def fly(self):
        raise NotImplementedError('ostrich cannot fly')
```

4. ISP (Interface Segregation)

```python
class Printer:
    def print(self, doc):
        pass

class Scanner:
    def scan(self):
        pass

# multi-function device composes small interfaces
class MultiFunctionDevice(Printer, Scanner):
    def print(self, doc):
        print('printing')
    def scan(self):
        print('scanning')
```

5. DIP (Dependency Inversion)

```python
class EmailSender:
    def send(self, to, body):
        print('send email')

class NotificationService:
    def __init__(self, sender):
        self.sender = sender
    def notify(self, to, body):
        self.sender.send(to, body)

# inject dependency
ns = NotificationService(EmailSender())
ns.notify('a@b.com', 'hello')
```
