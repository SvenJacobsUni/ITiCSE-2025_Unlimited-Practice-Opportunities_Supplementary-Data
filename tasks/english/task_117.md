# Input
- Programming Concept: Boolean and None; Higher-order functions
- Context: Social Media

# Generated Task Components
## Task Description
### Exercise: Social Media - Check User Activity

Write a function `is_active(user)` that checks if a user is active on a social network. A user is considered active if they have posted at least one post in the last 30 days. The function should return a Boolean value (`True` or `False`).

Additionally, implement a function `filter_active_users(user_list, filter_function)` that takes a list of users and a filter function as arguments. This function should return a new list containing only the active users.

A user is represented by a dictionary containing at least the following keys:
- `name`: The name of the user (String)
- `last_post`: The date of the last post in days from the current date (Integer)

Example:
```python
user1 = {"name": "Alice", "last_post": 10}
user2 = {"name": "Bob", "last_post": 40}
user3 = {"name": "Charlie", "last_post": 5}

user_list = [user1, user2, user3]

# Call of the function
active_users = filter_active_users(user_list, is_active)

# Expected output: [{"name": "Alice", "last_post": 10}, {"name": "Charlie", "last_post": 5}]
print(active_users)
```

Implement the functions `is_active(user)` and `filter_active_users(user_list, filter_function)`.

## Code Framework
```python
def is_active(user):
    ## Insert code here

def filter_active_users(user_list, filter_function):
    ## Insert code here

```

## Model Solution
```python
def is_active(user):
    return user['last_post'] <= 30

def filter_active_users(user_list, filter_function):
    return [user for user in user_list if filter_function(user)]

user1 = {"name": "Alice", "last_post": 10}
user2 = {"name": "Bob", "last_post": 40}
user3 = {"name": "Charlie", "last_post": 5}

user_list = [user1, user2, user3]

active_users = filter_active_users(user_list, is_active)

print(active_users)
```

## Unit Tests
```python
import unittest
from main import is_active, filter_active_users

class TestSocialMedia(unittest.TestCase):
    def test_is_active_true(self):
        user = {"name": "Alice", "last_post": 10}
        self.assertTrue(is_active(user))

    def test_is_active_false(self):
        user = {"name": "Bob", "last_post": 40}
        self.assertFalse(is_active(user))

    def test_filter_active_users(self):
        user1 = {"name": "Alice", "last_post": 10}
        user2 = {"name": "Bob", "last_post": 40}
        user3 = {"name": "Charlie", "last_post": 5}
        user_list = [user1, user2, user3]
        expected_output = [user1, user3]
        self.assertEqual(filter_active_users(user_list, is_active), expected_output)

    def test_empty_list(self):
        user_list = []
        expected_output = []
        self.assertEqual(filter_active_users(user_list, is_active), expected_output)

    def test_all_inactive(self):
        user1 = {"name": "Alice", "last_post": 40}
        user2 = {"name": "Bob", "last_post": 50}
        user_list = [user1, user2]
        expected_output = []
        self.assertEqual(filter_active_users(user_list, is_active), expected_output)

    def test_all_active(self):
        user1 = {"name": "Alice", "last_post": 10}
        user2 = {"name": "Bob", "last_post": 20}
        user_list = [user1, user2]
        expected_output = [user1, user2]
        self.assertEqual(filter_active_users(user_list, is_active), expected_output)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 549
