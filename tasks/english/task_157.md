# Input
- Programming Concept: Functions as variables; Logical operators (==, !=, <, >, <=, >=, or, and, not); Lists
- Context: Virtual Reality

# Generated Task Components
## Task Description
### Exercise: Virtual Reality - User Management

In a virtual reality system, users need to be managed. Each user has a name and age. Write a function `manage_users(user_list)` that takes a list of user names and their ages as input and performs the following tasks:

1. **Create a list of users who are older than 18 years.**
2. **Create a list of users who are 18 years old or younger.**
3. **Return the count of users in each list.**

The function should return a dictionary containing the count of users in both lists. The dictionary should have the following keys: `"adults"` and `"minors"`.

Example call:
```python
user_list = [("Alice", 22), ("Bob", 17), ("Charlie", 19), ("Diana", 15)]
result = manage_users(user_list)
print(result)  # Output: {"adults": 2, "minors": 2}
```

Implement the function `manage_users(user_list)` to meet the above requirements.

## Code Framework
```python
def manage_users(user_list):
    ## Insert code here
```

## Model Solution
```python
def manage_users(user_list):
    adults = [u for u in user_list if u[1] > 18]
    minors = [u for u in user_list if u[1] <= 18]
    return {"adults": len(adults), "minors": len(minors)}

user_list = [("Alice", 22), ("Bob", 17), ("Charlie", 19), ("Diana", 15)]
result = manage_users(user_list)
print(result)
```

## Unit Tests
```python
import unittest
from main import manage_users

class TestManageUsers(unittest.TestCase):
    def test_mixed_users(self):
        user_list = [("Alice", 22), ("Bob", 17), ("Charlie", 19), ("Diana", 15)]
        self.assertEqual(manage_users(user_list), {"adults": 2, "minors": 2})

    def test_only_adults(self):
        user_list = [("Alice", 22), ("Charlie", 19)]
        self.assertEqual(manage_users(user_list), {"adults": 2, "minors": 0})

    def test_only_minors(self):
        user_list = [("Bob", 17), ("Diana", 15)]
        self.assertEqual(manage_users(user_list), {"adults": 0, "minors": 2})

    def test_empty_list(self):
        user_list = []
        self.assertEqual(manage_users(user_list), {"adults": 0, "minors": 0})

    def test_boundary_18(self):
        user_list = [("Alice", 18), ("Bob", 18)]
        self.assertEqual(manage_users(user_list), {"adults": 0, "minors": 2})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 589
