# Input
- Programming Concept: Operations with numbers;Integer
- Context: Modern Gaming

# Generated Task Components
## Task Description
### Exercise: Modern Gaming - Player Level Calculation

In modern video games, it is common for players to level up by collecting experience points (XP). Write a function named `calculate_level(xp)` that calculates and returns the current level of a player based on the collected experience points.

The level calculation follows this scheme:
- Level 1: 0 - 999 XP
- Level 2: 1000 - 1999 XP
- Level 3: 2000 - 2999 XP
- Level 4: 3000 - 3999 XP
- Level 5: 4000 - 4999 XP
- etc.

Each additional level requires 1000 more XP.

Example calls:
- `calculate_level(1500)` returns `2`.
- `calculate_level(4500)` returns `5`.

Implement the function `calculate_level(xp)` that performs the calculation as described above.

## Code Framework
```python
def calculate_level(xp):
    ## Insert code here
```

## Model Solution
```python
def calculate_level(xp):
    return xp // 1000 + 1

# Example calls
print(calculate_level(1500))  # Output: 2
print(calculate_level(4500))  # Output: 5
```

## Unit Tests
```python
import unittest
from main import calculate_level

class TestCalculateLevel(unittest.TestCase):
    def test_level_1(self):
        self.assertEqual(calculate_level(0), 1)
        self.assertEqual(calculate_level(999), 1)

    def test_level_2(self):
        self.assertEqual(calculate_level(1000), 2)
        self.assertEqual(calculate_level(1999), 2)

    def test_level_3(self):
        self.assertEqual(calculate_level(2000), 3)
        self.assertEqual(calculate_level(2999), 3)

    def test_level_4(self):
        self.assertEqual(calculate_level(3000), 4)
        self.assertEqual(calculate_level(3999), 4)

    def test_level_5(self):
        self.assertEqual(calculate_level(4000), 5)
        self.assertEqual(calculate_level(4999), 5)

    def test_high_levels(self):
        self.assertEqual(calculate_level(10000), 11)
        self.assertEqual(calculate_level(12345), 13)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 547
