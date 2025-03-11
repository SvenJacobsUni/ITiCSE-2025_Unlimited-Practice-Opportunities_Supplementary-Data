# Input
- Programming Concept: If-Else statements
- Context: Social Media

# Generated Task Components
## Task Description
### Exercise: Social Media - User Status

Write a function called `user_status(number_of_followers)` that determines the status of a user on a social media platform based on their number of followers. The function should return an appropriate message with `return`.

- If the number of followers is less than 100, the message 'Newbie' should be returned.
- If the number of followers is between 100 and 1000 (inclusive), the message 'Rising Star' should be returned.
- If the number of followers is more than 1000, the message 'Influencer' should be returned.

Example calls:
- `user_status(50)` returns 'Newbie'.
- `user_status(500)` returns 'Rising Star'.
- `user_status(1500)` returns 'Influencer'.

## Code Framework
```python
def user_status(number_of_followers):
    ## Insert code here
```

## Model Solution
```python
def user_status(number_of_followers):
    if number_of_followers < 100:
        return 'Newbie'
    elif number_of_followers <= 1000:
        return 'Rising Star'
    else:
        return 'Influencer'

# Example calls
print(user_status(50))    # Newbie
print(user_status(500))   # Rising Star
print(user_status(1500))  # Influencer
```

## Unit Tests
```python
import unittest

from main import user_status

class TestUserStatus(unittest.TestCase):
    def test_newbie(self):
        self.assertEqual(user_status(50), 'Newbie')

    def test_rising_star(self):
        self.assertEqual(user_status(500), 'Rising Star')

    def test_influencer(self):
        self.assertEqual(user_status(1500), 'Influencer')

    def test_boundary_newbie_rising_star(self):
        self.assertEqual(user_status(100), 'Rising Star')

    def test_boundary_rising_star_influencer(self):
        self.assertEqual(user_status(1000), 'Rising Star')

    def test_zero_followers(self):
        self.assertEqual(user_status(0), 'Newbie')

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 458
