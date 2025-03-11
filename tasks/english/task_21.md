# Input
- Programming Concept: Higher-order functions
- Context: Rugby

# Generated Task Components
## Task Description
### Practice Task: Higher-order functions in the Rugby context

Write a function `filter_players(player_list, criterion_function)` that takes a list of rugby players and a criterion function as arguments. The function should return a new list containing only the players that meet the criterion.

Each player is represented by a dictionary that contains at least the following keys:
- `name`: The name of the player (String)
- `position`: The player's position (String)
- `points`: The number of points scored (Integer)

Example:
```python
player_list = [
    {"name": "Max", "position": "Forward", "points": 15},
    {"name": "Tom", "position": "Defender", "points": 5},
    {"name": "Leo", "position": "Forward", "points": 20}
]

def criterion(player):
    return player["points"] > 10

result = filter_players(player_list, criterion)
# result should be [{"name": "Max", "position": "Forward", "points": 15}, {"name": "Leo", "position": "Forward", "points": 20}]
```

Implement the function `filter_players(player_list, criterion_function)`.

## Code Framework
```python
def filter_players(player_list, criterion_function):
    ## Insert code here
```

## Model Solution
```python
def filter_players(player_list, criterion_function):
    return [player for player in player_list if criterion_function(player)]

player_list = [
    {"name": "Max", "position": "Forward", "points": 15},
    {"name": "Tom", "position": "Defender", "points": 5},
    {"name": "Leo", "position": "Forward", "points": 20}
]

def criterion(player):
    return player["points"] > 10

result = filter_players(player_list, criterion)
print(result)
```

## Unit Tests
```python
import unittest
from main import filter_players

class TestFilterPlayers(unittest.TestCase):
    def test_all_players_meet_criterion(self):
        player_list = [
            {"name": "Max", "position": "Forward", "points": 15},
            {"name": "Leo", "position": "Forward", "points": 20}
        ]
        def criterion(player):
            return player["points"] > 10
        self.assertEqual(filter_players(player_list, criterion), player_list)

    def test_no_player_meets_criterion(self):
        player_list = [
            {"name": "Tom", "position": "Defender", "points": 5},
            {"name": "Jim", "position": "Defender", "points": 3}
        ]
        def criterion(player):
            return player["points"] > 10
        self.assertEqual(filter_players(player_list, criterion), [])

    def test_some_players_meet_criterion(self):
        player_list = [
            {"name": "Max", "position": "Forward", "points": 15},
            {"name": "Tom", "position": "Defender", "points": 5},
            {"name": "Leo", "position": "Forward", "points": 20}
        ]
        def criterion(player):
            return player["points"] > 10
        expected_result = [
            {"name": "Max", "position": "Forward", "points": 15},
            {"name": "Leo", "position": "Forward", "points": 20}
        ]
        self.assertEqual(filter_players(player_list, criterion), expected_result)

    def test_empty_list(self):
        player_list = []
        def criterion(player):
            return player["points"] > 10
        self.assertEqual(filter_players(player_list, criterion), [])

    def test_criterion_always_true(self):
        player_list = [
            {"name": "Max", "position": "Forward", "points": 15},
            {"name": "Tom", "position": "Defender", "points": 5},
            {"name": "Leo", "position": "Forward", "points": 20}
        ]
        def criterion(player):
            return True
        self.assertEqual(filter_players(player_list, criterion), player_list)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 439
