# Input
- Programming Concept: Lists;If-Else statements
- Context: Rugby

# Generated Task Components
## Task Description
### Exercise: Filter Rugby Players

Write a function named `filter_players(player_list)` that takes a list of rugby player names and their positions as input. The function should return a new list containing only the names of players who play in the position "Forward".

The input list is formatted as:
```python
[("Name1", "Position1"), ("Name2", "Position2"), ...]
```

Example:
```python
player_list = [("Max", "Forward"), ("Tom", "Defender"), ("Lukas", "Forward"), ("Paul", "Winger")]
```

Call:
```python
filter_players(player_list)
```

Expected Output:
```python
["Max", "Lukas"]
```

Implement the function `filter_players(player_list)` to fulfill the above task.

## Code Framework
```python
def filter_players(player_list):
    ## Insert code here
```

## Model Solution
```python
def filter_players(player_list):
    return [name for name, position in player_list if position == "Forward"]

player_list = [("Max", "Forward"), ("Tom", "Defender"), ("Lukas", "Forward"), ("Paul", "Winger")]
print(filter_players(player_list))
```

## Unit Tests
```python
import unittest
from main import filter_players

class TestFilterPlayers(unittest.TestCase):
    def test_multiple_forwards(self):
        self.assertEqual(filter_players([("Max", "Forward"), ("Tom", "Defender"), ("Lukas", "Forward"), ("Paul", "Winger")]), ["Max", "Lukas"])

    def test_no_forwards(self):
        self.assertEqual(filter_players([("Tom", "Defender"), ("Paul", "Winger")]), [])

    def test_all_forwards(self):
        self.assertEqual(filter_players([("Max", "Forward"), ("Lukas", "Forward")]), ["Max", "Lukas"])

    def test_empty_list(self):
        self.assertEqual(filter_players([]), [])

    def test_single_forward(self):
        self.assertEqual(filter_players([("Max", "Forward")]), ["Max"])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 553
