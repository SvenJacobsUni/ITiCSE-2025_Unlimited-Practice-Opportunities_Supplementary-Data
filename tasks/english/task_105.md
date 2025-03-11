# Input
- Programming Concept: Logical operators (==, !=, <, >, <=, >=, or, and, not);While loops
- Context: Modern Gaming

# Generated Task Components
## Task Description
### Exercise: Modern Gaming - Player Level

Write a function named `player_level(points)` that determines the level of a player based on their points. The function should return a message with the achieved level. Use logical operators and a while loop to check the points and determine the corresponding level.

The levels are defined as follows:
- Level 1: 0 to 99 points
- Level 2: 100 to 199 points
- Level 3: 200 to 299 points
- Level 4: 300 to 399 points
- Level 5: 400 or more points

Example call:
```python
print(player_level(150))  # Output: "You are on Level 2!"
print(player_level(350))  # Output: "You are on Level 4!"
```

Implement the function `player_level(points)` that takes the player's points as an argument and returns the corresponding level as a message.

## Code Framework
```python
def player_level(points):
    ## Insert code here
```

## Model Solution
```python
def player_level(points):
    level = 1
    while points >= 100:
        points -= 100
        level += 1
    return f"You are on Level {level}!"

print(player_level(150))  # Output: "You are on Level 2!"
print(player_level(350))  # Output: "You are on Level 4!"
```

## Unit Tests
```python
import unittest

from main import player_level

class TestPlayerLevel(unittest.TestCase):
    def test_level_1(self):
        self.assertEqual(player_level(50), "You are on Level 1!")

    def test_level_2(self):
        self.assertEqual(player_level(150), "You are on Level 2!")

    def test_level_3(self):
        self.assertEqual(player_level(250), "You are on Level 3!")

    def test_level_4(self):
        self.assertEqual(player_level(350), "You are on Level 4!")

    def test_level_5(self):
        self.assertEqual(player_level(450), "You are on Level 5!")

    def test_exact_boundary_level_1(self):
        self.assertEqual(player_level(99), "You are on Level 1!")

    def test_exact_boundary_level_2(self):
        self.assertEqual(player_level(100), "You are on Level 2!")

    def test_exact_boundary_level_3(self):
        self.assertEqual(player_level(200), "You are on Level 3!")

    def test_exact_boundary_level_4(self):
        self.assertEqual(player_level(300), "You are on Level 4!")

    def test_exact_boundary_level_5(self):
        self.assertEqual(player_level(400), "You are on Level 5!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 537
