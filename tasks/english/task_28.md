# Input
- Programming Concept: While loops
- Context: Social Media

# Generated Task Components
## Task Description
### Exercise: Follower Counter

Write a function named `follower_counter(start_followers, target_followers)` that calculates the number of days needed to reach a certain number of followers on a social media platform.

- `start_followers` is the number of followers you have at the beginning.
- `target_followers` is the number of followers you aim to achieve.

Every day you gain 10 new followers. The function should return the number of days needed to reach or exceed the `target_followers`.

Example call: `follower_counter(100, 150)` returns `5`.

## Code Framework
```python
def follower_counter(start_followers, target_followers):
    ## Insert code here
```

## Model Solution
```python
def follower_counter(start_followers, target_followers):
    return (target_followers - start_followers + 9) // 10

print(follower_counter(100, 150))
```

## Unit Tests
```python
import unittest
from main import follower_counter

class TestFollowerCounter(unittest.TestCase):
    def test_simple_case(self):
        self.assertEqual(follower_counter(100, 150), 5)

    def test_no_increase_needed(self):
        self.assertEqual(follower_counter(100, 100), 0)

    def test_one_day_needed(self):
        self.assertEqual(follower_counter(100, 109), 1)

    def test_multiple_days_needed(self):
        self.assertEqual(follower_counter(100, 200), 10)

    def test_large_increase(self):
        self.assertEqual(follower_counter(100, 1000), 90)

    def test_start_and_target_equal(self):
        self.assertEqual(follower_counter(0, 0), 0)

    def test_start_greater_than_target(self):
        self.assertEqual(follower_counter(150, 100), 0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 446
