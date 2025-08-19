# DRY Examples — Python

```python
# before (duplication)
def send_welcome_email(user):
    print(f"Sending email to {user['email']}")

def send_password_reset(user):
    print(f"Sending email to {user['email']}")

# after (DRY)
def send_email(user, template):
    print(f"Sending {template} to {user['email']}")

send_email({'email':'a@b.com'}, 'welcome')
```
