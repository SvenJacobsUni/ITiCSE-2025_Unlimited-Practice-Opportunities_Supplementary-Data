# Input
- Programming Concept: If-Else statements
- Context: Modern Gaming

# Generated Task Components
## Task Description
### Exercise Task: Modern Gaming - Player Selection

Write a function named `player_selection(level)` that returns an appropriate message based on the player's passed level. The function should consider the following conditions:

- If the player's level is less than 10, the message "Beginner: Welcome to the world of gaming!" should be returned.
- If the player's level is between 10 and 20 (inclusive), the message "Intermediate: You are making progress!" should be returned.
- If the player's level is greater than 20, the message "Pro: You are a true gamer!" should be returned.

Example calls:
- `player_selection(5)` returns "Beginner: Welcome to the world of gaming!"
- `player_selection(15)` returns "Intermediate: You are making progress!"
- `player_selection(25)` returns "Pro: You are a true gamer!"

## Code Framework
```python
def player_selection(level):
    ## Insert code here
```

## Model Solution
```python
def player_selection(level):
    if level < 10:
        return "Beginner: Welcome to the world of gaming!"
    elif 10 <= level <= 20:
        return "Intermediate: You are making progress!"
    else:
        return "Pro: You are a true gamer!"

# Example calls
print(player_selection(5))
print(player_selection(15))
print(player_selection(25))
```

## Unit Tests
```python
import unittest
from main import player_selection

class TestPlayerSelection(unittest.TestCase):
    def test_beginner(self):
        self.assertEqual(player_selection(5), "Beginner: Welcome to the world of gaming!")

    def test_intermediate(self):
        self.assertEqual(player_selection(15), "Intermediate: You are making progress!")

    def test_pro(self):
        self.assertEqual(player_selection(25), "Pro: You are a true gamer!")

    def test_edge_beginner(self):
        self.assertEqual(player_selection(9), "Beginner: Welcome to the world of gaming!")

    def test_edge_intermediate_lower(self):
        self.assertEqual(player_selection(10), "Intermediate: You are making progress!")

    def test_edge_intermediate_upper(self):
        self.assertEqual(player_selection(20), "Intermediate: You are making progress!")

    def test_edge_pro(self):
        self.assertEqual(player_selection(21), "Pro: You are a true gamer!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 444
