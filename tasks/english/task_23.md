# Input
- Programming Concept: Higher-order functions
- Context: Rugby

# Generated Task Components
## Task Description
### Practice Task: Higher-order Functions in a Rugby Context

Write a function `filter_players(player_list, criterion_function)` that takes a list of rugby players and a criterion function as arguments. The function should return a new list that only contains the players who meet the criterion.

Each player is represented by a dictionary that contains at least the following keys:
- `name`: The player's name (String)
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
    def test_points_greater_than_10(self):
        player_list = [
            {"name": "Max", "position": "Forward", "points": 15},
            {"name": "Tom", "position": "Defender", "points": 5},
            {"name": "Leo", "position": "Forward", "points": 20}
        ]
        def criterion(player):
            return player["points"] > 10
        expected = [
            {"name": "Max", "position": "Forward", "points": 15},
            {"name": "Leo", "position": "Forward", "points": 20}
        ]
        self.assertEqual(filter_players(player_list, criterion), expected)

    def test_position_forward(self):
        player_list = [
            {"name": "Max", "position": "Forward", "points": 15},
            {"name": "Tom", "position": "Defender", "points": 5},
            {"name": "Leo", "position": "Forward", "points": 20}
        ]
        def criterion(player):
            return player["position"] == "Forward"
        expected = [
            {"name": "Max", "position": "Forward", "points": 15},
            {"name": "Leo", "position": "Forward", "points": 20}
        ]
        self.assertEqual(filter_players(player_list, criterion), expected)

    def test_empty_list(self):
        player_list = []
        def criterion(player):
            return player["points"] > 10
        expected = []
        self.assertEqual(filter_players(player_list, criterion), expected)

    def test_all_players_meet_criterion(self):
        player_list = [
            {"name": "Max", "position": "Forward", "points": 15},
            {"name": "Tom", "position": "Defender", "points": 12},
            {"name": "Leo", "position": "Forward", "points": 20}
        ]
        def criterion(player):
            return player["points"] > 10
        expected = [
            {"name": "Max", "position": "Forward", "points": 15},
            {"name": "Tom", "position": "Defender", "points": 12},
            {"name": "Leo", "position": "Forward", "points": 20}
        ]
        self.assertEqual(filter_players(player_list, criterion), expected)

    def test_none_meet_criterion(self):
        player_list = [
            {"name": "Max", "position": "Forward", "points": 5},
            {"name": "Tom", "position": "Defender", "points": 3},
            {"name": "Leo", "position": "Forward", "points": 2}
        ]
        def criterion(player):
            return player["points"] > 10
        expected = []
        self.assertEqual(filter_players(player_list, criterion), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 441
