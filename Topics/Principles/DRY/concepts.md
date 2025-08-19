# DRY — Don't Repeat Yourself

- Definition: DRY states that every piece of knowledge should have a single, unambiguous representation in a system.
- Discussion: Avoid duplicated logic by extracting common functionality into functions, classes, or modules. Duplication increases maintenance cost and bug risk. Balance DRY with readability—don't over-abstract trivial duplication.

  Example (Python):

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
