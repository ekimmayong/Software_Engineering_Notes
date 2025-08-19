# Test-Driven Development (TDD)

- Definition: TDD is a practice where tests are written before the code that implements the behavior. Cycle: Red (fail), Green (pass), Refactor.
- Discussion: TDD encourages small, testable units and frequent refactoring. Start with unit tests and expand to integration tests. Use TDD to design APIs and guard regressions.

  Example (Python - pytest):

  ```python
  # test_add.py
  from mymodule import add
  
  def test_add():
      assert add(2,3) == 5
  
  # mymodule.py
  def add(a,b):
      return a + b
  
  # Run: pytest
  ```
