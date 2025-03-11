# Input
- Programming Concept: If-Else statements; While loops; Boolean and None
- Context: Modern Gaming

# Generated Task Components
## Task Description
### Exercise Task: Modern Gaming - Player Level and Experience Points

Write a function `level_up(player_level, experience_points)` that checks if a player can level up based on their experience points. 

- If the player has 1000 or more experience points, they level up and the function returns `True`.
- If the player has less than 1000 experience points, they remain at the current level and the function returns `False`.
- If the player has no experience points (None), the function also returns `False`.

Additionally, the function should use a while loop to reduce the player's experience points until they are below 1000 if the player levels up.

Example call:
```python
level_up(5, 1200)  # returns True and reduces experience points to 200
level_up(3, 800)   # returns False
level_up(2, None)  # returns False
```

## Code Framework
```python
def level_up(player_level, experience_points):
    ## Insert code here
```

## Model Solution
```python
def level_up(player_level, experience_points):
    if experience_points is None or experience_points < 1000:
        return False
    while experience_points >= 1000:
        experience_points -= 1000
        player_level += 1
    return True

# Example calls
print(level_up(5, 1200))  # True
print(level_up(3, 800))   # False
print(level_up(2, None))  # False
```

## Unit Tests
```python
import unittest

from main import level_up

class TestLevelUp(unittest.TestCase):
    def test_level_up_with_enough_experience(self):
        self.assertTrue(level_up(5, 1200))

    def test_level_up_with_not_enough_experience(self):
        self.assertFalse(level_up(3, 800))

    def test_level_up_with_no_experience(self):
        self.assertFalse(level_up(2, None))

    def test_level_up_with_exact_experience(self):
        self.assertTrue(level_up(1, 1000))

    def test_level_up_with_multiple_levels(self):
        self.assertTrue(level_up(1, 2500))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 618
