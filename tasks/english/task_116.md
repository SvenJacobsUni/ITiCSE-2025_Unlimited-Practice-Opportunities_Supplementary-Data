# Input
- Programming Concept: If-Else statements;Operations with numbers
- Context: Modern Gaming

# Generated Task Components
## Task Description
### Exercise: Modern Gaming - Player Level

Write a function called `player_level(points)` that determines the level of a player based on their score. The function should return a message that indicates the player's level.

The levels are defined as follows:
- Less than 1000 points: "Beginner"
- 1000 to 4999 points: "Intermediate"
- 5000 to 9999 points: "Pro"
- 10000 or more points: "Legend"

Example calls:
- `player_level(750)` returns "Beginner".
- `player_level(3200)` returns "Intermediate".
- `player_level(7500)` returns "Pro".
- `player_level(12000)` returns "Legend".


## Code Framework
```python
def player_level(points):
    ## Insert code here

```

## Model Solution
```python
def player_level(points):
    if points < 1000:
        return "Beginner"
    elif points < 5000:
        return "Intermediate"
    elif points < 10000:
        return "Pro"
    else:
        return "Legend"

# Example calls
print(player_level(750))    # Beginner
print(player_level(3200))   # Intermediate
print(player_level(7500))   # Pro
print(player_level(12000))  # Legend

```

## Unit Tests
```python
import unittest
from main import player_level

class TestPlayerLevel(unittest.TestCase):
    def test_beginner(self):
        self.assertEqual(player_level(750), "Beginner")

    def test_intermediate(self):
        self.assertEqual(player_level(3200), "Intermediate")

    def test_pro(self):
        self.assertEqual(player_level(7500), "Pro")

    def test_legend(self):
        self.assertEqual(player_level(12000), "Legend")

    def test_boundary_beginner_intermediate(self):
        self.assertEqual(player_level(1000), "Intermediate")

    def test_boundary_intermediate_pro(self):
        self.assertEqual(player_level(5000), "Pro")

    def test_boundary_pro_legend(self):
        self.assertEqual(player_level(10000), "Legend")

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 548
