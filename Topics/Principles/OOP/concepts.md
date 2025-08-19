# OOP Concepts — Definitions & Discussions (Python)

This file explains the fundamental OOP concepts with Python-focused discussions.

1. Classes & Objects

- Definition: A class is a blueprint that defines attributes and behaviors (methods). An object (instance) is a concrete realization of a class.
- Discussion: Use classes to model real-world or domain entities. Keep classes focused on a single responsibility. Prefer composition to combine behavior from multiple classes.

  Example (Python):

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

2. Encapsulation

- Definition: Encapsulation hides internal state and implementation details behind a public interface.
- Discussion: In Python, use naming conventions (_protected, __private) and properties for controlled access. Encapsulation helps maintain invariants and simplifies refactoring.

  Example (Python - properties):

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

3. Inheritance

- Definition: Inheritance allows a class (subclass) to reuse attributes and methods from another class (superclass).
- Discussion: Use inheritance for "is-a" relationships. Avoid deep inheritance trees—consider composition or interfaces (abstract base classes) when appropriate.

  Example (Python):

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

4. Polymorphism

- Definition: Polymorphism lets code operate on objects of different types through a common interface (duck typing in Python).
- Discussion: Rely on behavior rather than strict types. Use abstract base classes (ABC) to formalize interfaces when needed.

  Example (Python - duck typing):

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

  def serialize(obj):
      return obj.to_json()

  print(serialize(Person('Eve')))
  ```

5. Abstraction

- Definition: Abstraction simplifies complex reality by modeling essential features and hiding details.
- Discussion: Design classes that expose a clear API and hide implementation. Use modules and classes to create meaningful abstractions.

  Example (Python - ABC for an interface):

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
  ```

6. SOLID Principles (brief)

- Definition: SOLID is a set of design principles to create maintainable object-oriented systems: Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion.
- Discussion: Use SOLID as guidelines, not strict rules. Start applying SRP and DI early; learn others as complexity grows.

  Example (Python - SRP & DI simple):

  ```python
  # Single Responsibility: separate concerns
  class EmailService:
      def send(self, to, subject, body):
          print(f"sending to {to}: {subject}")

  class UserRegistration:
      def __init__(self, email_service):
          self.email_service = email_service

      def register(self, email):
          # register user (omitted)
          self.email_service.send(email, 'Welcome', 'Thanks for registering')

  # Dependency Injection: pass dependency from outside
  email_service = EmailService()
  reg = UserRegistration(email_service)
  reg.register('user@example.com')
  ```
