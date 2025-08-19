# YAGNI — You Aren't Gonna Need It

- Definition: YAGNI reminds developers not to add functionality until it is necessary.
- Discussion: Avoid speculative features and premature optimization. Implement the simplest solution that works and refactor later when real requirements emerge.

  Example (Python):

  ```python
  # don't over-engineer: start simple
  class Config:
      def __init__(self, options):
          self.options = options
  
  # Later, if needed, add validation or nesting
  ```
