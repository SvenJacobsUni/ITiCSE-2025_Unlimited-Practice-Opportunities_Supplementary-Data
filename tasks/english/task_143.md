# Input
- Programming Concept: Lists; Recursion
- Context: Social Media

# Generated Task Components
## Task Description
### Exercise: Follower Count in Social Media

In social media, it is often important to know the number of followers a user has. Write a recursive function `count_followers(follower_list)` that counts the number of followers in a nested list. The list can contain both individual followers and further lists of followers.

Example:
```python
follower_list = ["Anna", ["Ben", "Clara"], "David", ["Eva", ["Frank", "Grace"]]]
```

In this example, the user has a total of 6 followers.

Implement the function `count_followers(follower_list)` that returns the number of followers in the nested list.

Example call:
```python
print(count_followers(follower_list))  # Output: 6
```

## Code Framework
```python
def count_followers(follower_list):
    ## Insert code here
```

## Model Solution
```python
def count_followers(follower_list):
    if not follower_list:
        return 0
    if isinstance(follower_list[0], list):
        return count_followers(follower_list[0]) + count_followers(follower_list[1:])
    return 1 + count_followers(follower_list[1:])

follower_list = ["Anna", ["Ben", "Clara"], "David", ["Eva", ["Frank", "Grace"]]]
print(count_followers(follower_list))  # Output: 6
```

## Unit Tests
```python
import unittest

from main import count_followers

class TestCountFollowers(unittest.TestCase):
    def test_simple_list(self):
        self.assertEqual(count_followers(["Anna", "Ben", "Clara"]), 3)

    def test_nested_list(self):
        self.assertEqual(count_followers(["Anna", ["Ben", "Clara"], "David", ["Eva", ["Frank", "Grace"]]]), 6)

    def test_empty_list(self):
        self.assertEqual(count_followers([]), 0)

    def test_single_follower(self):
        self.assertEqual(count_followers(["Anna"]), 1)

    def test_deeply_nested_list(self):
        self.assertEqual(count_followers(["Anna", ["Ben", ["Clara", ["David", ["Eva"]]]]]), 5)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 575
