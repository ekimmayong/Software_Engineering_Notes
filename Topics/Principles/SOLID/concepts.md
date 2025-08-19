# SOLID Principles — Concepts and Discussion

1. Single Responsibility Principle (SRP)
- Definition: A class/module should have one, and only one, reason to change.
- Discussion: Keep classes focused; if a class handles persistence and business rules, split responsibilities.

  Example (Python):

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

2. Open/Closed Principle (OCP)
- Definition: Software entities should be open for extension but closed for modification.
- Discussion: Achieve via abstraction and polymorphism (e.g., inherit or inject behaviors instead of changing existing code).

  Example (Python):

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

3. Liskov Substitution Principle (LSP)
- Definition: Objects of a superclass should be replaceable with objects of a subclass without affecting correctness.
- Discussion: Subclasses should fulfill the contract of the base class and not weaken preconditions or strengthen postconditions.

  Example (Python):

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

4. Interface Segregation Principle (ISP)
- Definition: Many client-specific interfaces are better than one general-purpose interface.
- Discussion: Prefer smaller, focused interfaces to avoid forcing implementations to provide unused methods.

  Example (Python):

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

5. Dependency Inversion Principle (DIP)
- Definition: High-level modules should not depend on low-level modules; both should depend on abstractions.
- Discussion: Use inversion of control and dependency injection to decouple components.

  Example (Python):

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
