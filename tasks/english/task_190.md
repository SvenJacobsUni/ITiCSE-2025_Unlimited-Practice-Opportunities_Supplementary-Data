# Input
- Programming Concept: Integer;Lists;String
- Context: Rugby

# Generated Task Components
## Task Description
### Exercise: Rugby Player Statistics

Write a function named `player_statistics(player_list)` that receives a list of player names and their scores in a rugby game. The list contains strings in the format "Name:Points", where "Name" is the player's name and "Points" are the points scored as an integer.

The function should fulfill the following tasks:
1. Calculate and return the total score of all players.
2. Return the name of the player with the most points. If multiple players have the same highest score, the first one in the list should be returned.

Example call:
```python
player_list = ["Max:5", "Anna:3", "Tom:7", "Lisa:7"]
total_points, best_player = player_statistics(player_list)
print(total_points)  # Output: 22
print(best_player)  # Output: Tom
```

Implement the function `player_statistics(player_list)` to meet the requirements above.

## Code Framework
```python
def player_statistics(player_list):
    ## Insert code here
```

## Model Solution
```python
def player_statistics(player_list):
    total_points = 0
    best_player = ""
    max_points = -1
    for entry in player_list:
        name, points = entry.split(":")
        points = int(points)
        total_points += points
        if points > max_points:
            max_points = points
            best_player = name
    return total_points, best_player

player_list = ["Max:5", "Anna:3", "Tom:7", "Lisa:7"]
total_points, best_player = player_statistics(player_list)
print(total_points)  # Output: 22
print(best_player)  # Output: Tom
```

## Unit Tests
```python
import unittest

from main import player_statistics

class TestPlayerStatistics(unittest.TestCase):
    def test_simple_case(self):
        player_list = ["Max:5", "Anna:3", "Tom:7", "Lisa:7"]
        total_points, best_player = player_statistics(player_list)
        self.assertEqual(total_points, 22)
        self.assertEqual(best_player, "Tom")

    def test_all_players_same_points(self):
        player_list = ["Max:5", "Anna:5", "Tom:5", "Lisa:5"]
        total_points, best_player = player_statistics(player_list)
        self.assertEqual(total_points, 20)
        self.assertEqual(best_player, "Max")

    def test_single_player(self):
        player_list = ["Max:10"]
        total_points, best_player = player_statistics(player_list)
        self.assertEqual(total_points, 10)
        self.assertEqual(best_player, "Max")

    def test_empty_list(self):
        player_list = []
        total_points, best_player = player_statistics(player_list)
        self.assertEqual(total_points, 0)
        self.assertEqual(best_player, "")

    def test_negative_points(self):
        player_list = ["Max:-5", "Anna:3", "Tom:7", "Lisa:7"]
        total_points, best_player = player_statistics(player_list)
        self.assertEqual(total_points, 12)
        self.assertEqual(best_player, "Tom")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 622
