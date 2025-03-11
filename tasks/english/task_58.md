# Input
- Programming Concept: Integer
- Context: Social Media

# Generated Task Components
## Task Description
### Exercise: Social Media - Follower Counter

Write a function named `follower_counter(follower_list)`, which receives a list of integers as an argument. Each integer in the list represents the number of followers of a user in a social network. The function should calculate and return the total number of followers.

Example call:
```python
follower_counter([150, 200, 350, 400])
```
should return `1100`.

## Code Framework
```python
def follower_counter(follower_list):
    ## Insert code here
```

## Model Solution
```python
def follower_counter(follower_list):
    return sum(follower_list)

print(follower_counter([150, 200, 350, 400]))
```

## Unit Tests
```python
import unittest

from main import follower_counter

class TestFollowerCounter(unittest.TestCase):
    def test_simple_case(self):
        self.assertEqual(follower_counter([150, 200, 350, 400]), 1100)

    def test_empty_list(self):
        self.assertEqual(follower_counter([]), 0)

    def test_single_element(self):
        self.assertEqual(follower_counter([500]), 500)

    def test_negative_value(self):
        self.assertEqual(follower_counter([100, -50, 200]), 250)

    def test_mixed_values(self):
        self.assertEqual(follower_counter([100, 200, 300, 400, 500]), 1500)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 476
