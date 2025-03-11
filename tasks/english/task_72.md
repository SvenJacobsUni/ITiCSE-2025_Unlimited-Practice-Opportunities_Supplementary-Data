# Input
- Programming Concept: Integer
- Context: Modern Gaming

# Generated Task Components
## Task Description
### Exercise: Modern Gaming - Player Level

In modern video games, the level of a player is often an important indicator of their progress and skills. Write a function called `player_level(xp)` that calculates and returns the level of a player based on their experience points (XP). 

The levels should be calculated as follows:
- Level 1: 0 - 999 XP
- Level 2: 1000 - 1999 XP
- Level 3: 2000 - 2999 XP
- Level 4: 3000 - 3999 XP
- Level 5: 4000 - 4999 XP
- Level 6: 5000 - 5999 XP
- Level 7: 6000 - 6999 XP
- Level 8: 7000 - 7999 XP
- Level 9: 8000 - 8999 XP
- Level 10: 9000+ XP

Example call: `player_level(4500)` returns `5`.

## Code Framework
```python
def player_level(xp):
    ## Insert code here
```

## Model Solution
```python
def player_level(xp):
    return min(xp // 1000 + 1, 10)

print(player_level(4500))
```

## Unit Tests
```python
import unittest

from main import player_level

class TestPlayerLevel(unittest.TestCase):
    def test_level_1(self):
        self.assertEqual(player_level(0), 1)
        self.assertEqual(player_level(999), 1)

    def test_level_2(self):
        self.assertEqual(player_level(1000), 2)
        self.assertEqual(player_level(1999), 2)

    def test_level_3(self):
        self.assertEqual(player_level(2000), 3)
        self.assertEqual(player_level(2999), 3)

    def test_level_4(self):
        self.assertEqual(player_level(3000), 4)
        self.assertEqual(player_level(3999), 4)

    def test_level_5(self):
        self.assertEqual(player_level(4000), 5)
        self.assertEqual(player_level(4999), 5)

    def test_level_6(self):
        self.assertEqual(player_level(5000), 6)
        self.assertEqual(player_level(5999), 6)

    def test_level_7(self):
        self.assertEqual(player_level(6000), 7)
        self.assertEqual(player_level(6999), 7)

    def test_level_8(self):
        self.assertEqual(player_level(7000), 8)
        self.assertEqual(player_level(7999), 8)

    def test_level_9(self):
        self.assertEqual(player_level(8000), 9)
        self.assertEqual(player_level(8999), 9)

    def test_level_10(self):
        self.assertEqual(player_level(9000), 10)
        self.assertEqual(player_level(10000), 10)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 490
