# Separation of Concerns (SoC)

- Definition: SoC is the principle of organizing code so that different concerns (UI, business logic, persistence) are separated into distinct modules.
- Discussion: Separation makes code easier to test, maintain, and evolve. Apply SoC by layering applications (presentation, domain, data) and using clear module boundaries.

  Example (Python):

  ```python
  # presentation layer
  def render_user(user):
      return f"User: {user['name']}"
  
  # domain layer
  def format_user(user):
      return {'name': user['name'].title()}
  
  # data layer
  def save_user(user, repo):
      repo.save(user)
  
  # compose them in a controller-like function
  
  def create_user(raw, repo):
      user = format_user(raw)
      save_user(user, repo)
      return render_user(user)
  ```
