# Separation of Concerns — Examples (Python)

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
