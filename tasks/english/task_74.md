# Input
- Programming Concept: Higher-order functions
- Context: Rugby

# Generated Task Components
## Task Description
### Practice Task: Higher-order Functions in Rugby Context

Write a function `filter_players(player_list, criterion_function)` that accepts a list of rugby players and a function as parameters. The function should return a new list containing only the players that meet the criteria of the passed function.

Each player is represented by a dictionary that contains at least the keys `name` and `position`.

Example:

```python
player_list = [
    {"name": "Max", "position": "Forward"},
    {"name": "Tom", "position": "Defender"},
    {"name": "Leo", "position": "Forward"},
    {"name": "Paul", "position": "Defender"}
]

def is_forward(player):
    return player["position"] == "Forward"

# Function call
result = filter_players(player_list, is_forward)
# Expected result: [{"name": "Max", "position": "Forward"}, {"name": "Leo", "position": "Forward"}]
```

Implement the `filter_players` function and test it with different criteria.

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
    {"name": "Max", "position": "Forward"},
    {"name": "Tom", "position": "Defender"},
    {"name": "Leo", "position": "Forward"},
    {"name": "Paul", "position": "Defender"}
]

def is_forward(player):
    return player["position"] == "Forward"

result = filter_players(player_list, is_forward)
print(result)
```

## Unit Tests
```python
import unittest
from main import filter_players

class TestFilterPlayers(unittest.TestCase):
    def setUp(self):
        self.player_list = [
            {"name": "Max", "position": "Forward"},
            {"name": "Tom", "position": "Defender"},
            {"name": "Leo", "position": "Forward"},
            {"name": "Paul", "position": "Defender"}
        ]

    def test_is_forward(self):
        def is_forward(player):
            return player["position"] == "Forward"
        expected = [
            {"name": "Max", "position": "Forward"},
            {"name": "Leo", "position": "Forward"}
        ]
        self.assertEqual(filter_players(self.player_list, is_forward), expected)

    def test_is_defender(self):
        def is_defender(player):
            return player["position"] == "Defender"
        expected = [
            {"name": "Tom", "position": "Defender"},
            {"name": "Paul", "position": "Defender"}
        ]
        self.assertEqual(filter_players(self.player_list, is_defender), expected)

    def test_empty_list(self):
        def is_forward(player):
            return player["position"] == "Forward"
        self.assertEqual(filter_players([], is_forward), [])

    def test_no_matches(self):
        def is_goalkeeper(player):
            return player["position"] == "Goalkeeper"
        self.assertEqual(filter_players(self.player_list, is_goalkeeper), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 492
