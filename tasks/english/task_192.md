# Input
- Programming Concept: Logical operators (==, !=, <, >, <=, >=, or, and, not);For loops;Tuples
- Context: Rugby

# Generated Task Components
## Task Description
### Exercise Task: Rugby Player Statistics

Write a function `player_statistics(player_list)` that takes a list of tuples as an argument. Each tuple represents a rugby player and contains the following information in this order: Name (String), Age (Integer), Number of Tries (Integer).

The function should perform the following tasks:
1. Store all players who are older than 30 years and have scored more than 5 tries in a new list.
2. Return the number of players who meet these criteria.
3. Print the names of these players to the console.

Example call:
```python
player_list = [("Max", 32, 6), ("Tom", 28, 4), ("John", 35, 7), ("Alex", 22, 3)]
number_of_players = player_statistics(player_list)
print(number_of_players)  # Output: 2
```

In this example, "Max" and "John" are the players who are older than 30 and have scored more than 5 tries.

## Code Framework
```python
def player_statistics(player_list):
    ## Insert code here

```

## Model Solution
```python
def player_statistics(player_list):
    result = [player[0] for player in player_list if player[1] > 30 and player[2] > 5]
    for name in result:
        print(name)
    return len(result)

player_list = [("Max", 32, 6), ("Tom", 28, 4), ("John", 35, 7), ("Alex", 22, 3)]
number_of_players = player_statistics(player_list)
print(number_of_players)
```

## Unit Tests
```python
import unittest
from main import player_statistics

class TestPlayerStatistics(unittest.TestCase):
    def test_multiple_players(self):
        player_list = [("Max", 32, 6), ("Tom", 28, 4), ("John", 35, 7), ("Alex", 22, 3)]
        self.assertEqual(player_statistics(player_list), 2)

    def test_no_players(self):
        player_list = [("Tom", 28, 4), ("Alex", 22, 3)]
        self.assertEqual(player_statistics(player_list), 0)

    def test_all_players(self):
        player_list = [("Max", 32, 6), ("John", 35, 7)]
        self.assertEqual(player_statistics(player_list), 2)

    def test_boundary_players(self):
        player_list = [("Max", 30, 6), ("John", 31, 5)]
        self.assertEqual(player_statistics(player_list), 0)

    def test_empty_list(self):
        player_list = []
        self.assertEqual(player_statistics(player_list), 0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 624
