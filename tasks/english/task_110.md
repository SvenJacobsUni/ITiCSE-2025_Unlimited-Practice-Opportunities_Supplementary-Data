# Input
- Programming Concept: Boolean and None; Logical operators (==, !=, <, >, <=, >=, or, and, not)
- Context: Social Media

# Generated Task Components
## Task Description
### Exercise: Social Media - Check User Activity

Write a function named `is_active(username, posts, followers)`, which checks if a user is considered active on a social media platform. A user is considered active if they have posted at least 10 times **and** have more than 100 followers. The function should return a Boolean value (`True` or `False`).

Example calls:
- `is_active("MaxMustermann", 15, 150)` returns `True`.
- `is_active("ErikaMustermann", 5, 200)` returns `False`.

## Code Framework
```python
def is_active(username, posts, followers):
    ## Insert code here

```

## Model Solution
```python
def is_active(username, posts, followers):
    return posts >= 10 and followers > 100

# Example calls
print(is_active("MaxMustermann", 15, 150))  # True
print(is_active("ErikaMustermann", 5, 200))  # False
```

## Unit Tests
```python
import unittest
from main import is_active

class TestIsActive(unittest.TestCase):
    def test_active(self):
        self.assertTrue(is_active("MaxMustermann", 15, 150))

    def test_not_active_few_posts(self):
        self.assertFalse(is_active("ErikaMustermann", 5, 200))

    def test_not_active_few_followers(self):
        self.assertFalse(is_active("HansMustermann", 20, 50))

    def test_not_active_few_posts_and_followers(self):
        self.assertFalse(is_active("AnnaMustermann", 5, 50))

    def test_boundary_posts(self):
        self.assertFalse(is_active("BoundaryPosts", 9, 150))
        self.assertTrue(is_active("BoundaryPosts", 10, 150))

    def test_boundary_followers(self):
        self.assertFalse(is_active("BoundaryFollowers", 15, 100))
        self.assertTrue(is_active("BoundaryFollowers", 15, 101))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 542
