# Input
- Programming Concept: If-Else statements;Tuples;Float
- Context: Rugby

# Generated Task Components
## Task Description
### Exercise: Rugby Player Weight

Write a function named `player_weight(player)`, which receives a tuple as an argument. The tuple contains the player's name and weight in kilograms as a float. The function should check whether the player's weight is above or below 100 kg and return an appropriate message.

- If the player's weight is 100 kg or more, the message should be: "`[Name] is a heavy player.`"
- If the player's weight is below 100 kg, the message should be: "`[Name] is a light player.`"

Example call:
```python
player_weight(("Max", 105.5))  # returns "Max is a heavy player."
player_weight(("Tom", 95.0))   # returns "Tom is a light player."
```

## Code Framework
```python
def player_weight(player):
    ## Insert code here
```

## Model Solution
```python
def player_weight(player):
    name, weight = player
    if weight >= 100:
        return f"{name} is a heavy player."
    else:
        return f"{name} is a light player."

player_weight(("Max", 105.5))
player_weight(("Tom", 95.0))
```

## Unit Tests
```python
import unittest
from main import player_weight

class TestPlayerWeight(unittest.TestCase):
    def test_heavy_player(self):
        self.assertEqual(player_weight(("Max", 105.5)), "Max is a heavy player.")

    def test_light_player(self):
        self.assertEqual(player_weight(("Tom", 95.0)), "Tom is a light player.")

    def test_boundary_heavy_player(self):
        self.assertEqual(player_weight(("John", 100.0)), "John is a heavy player.")

    def test_boundary_light_player(self):
        self.assertEqual(player_weight(("Alex", 99.9)), "Alex is a light player.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 608
