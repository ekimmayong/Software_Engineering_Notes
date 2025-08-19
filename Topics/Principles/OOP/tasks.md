# OOP Tasks — Exercises & Projects (Python)

Beginner tasks

1. Build a Task class
- Create a `Task` class with title, description, and completed attributes.
- Add methods: `complete()`, `to_dict()`.
- Write a small script that creates tasks, marks some complete, and prints incomplete tasks.

2. Implement a simple BankAccount
- Implement deposit, withdraw, and transfer methods.
- Ensure the balance cannot go negative; raise exceptions for invalid operations.

Intermediate tasks

3. Todo app using classes
- Build a small CLI todo app using a `Task` and `TodoList` class.
- Persist tasks to a local JSON file and load them on start.

4. Implement an InMemoryRepository with CRUD
- Create a generic repository class supporting create/read/update/delete for objects with `id`.
- Add simple filtering by attribute values.

Advanced tasks

5. Design patterns practice
- Implement at least two design patterns in Python (Factory, Strategy, Observer, or Adapter).

6. Mini project: Library management system
- Model entities: Book, Member, Loan. Implement borrowing/returning logic and enforce constraints (e.g., max loans per member).

Testing

- Write unit tests for at least two tasks using `pytest` or `unittest`.
- Mock dependencies where appropriate.

Deliverables

- For each task, include a README with how to run the code and tests.
- Keep commits small and descriptive.
