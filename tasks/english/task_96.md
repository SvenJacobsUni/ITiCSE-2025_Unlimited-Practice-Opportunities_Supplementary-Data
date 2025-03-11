# Input
- Programming Concept: Higher-order functions
- Context: Sports

# Generated Task Components
## Task Description
### Exercise: Higher-order functions in Sports

Write a function named `filter_athletes(athlete_list, criterion_function)` that takes a list of athletes and a function as parameters. The function should return a new list that only contains the athletes who meet the criterion of the passed function.

An athlete is represented by a dictionary that contains at least the keys `name` and `sport`.

Example:

```python
athlete_list = [
    {"name": "Anna", "sport": "Tennis"},
    {"name": "Ben", "sport": "Football"},
    {"name": "Clara", "sport": "Swimming"},
    {"name": "David", "sport": "Tennis"}
]

def is_tennis_player(athlete):
    return athlete["sport"] == "Tennis"

# Calling the function
filtered_athletes = filter_athletes(athlete_list, is_tennis_player)
# Expected output: [{"name": "Anna", "sport": "Tennis"}, {"name": "David", "sport": "Tennis"}]
```

Implement the function `filter_athletes` so that it filters the list of athletes based on the passed criterion function and returns the filtered list.

## Code Framework
```python
def filter_athletes(athlete_list, criterion_function):
    ## Insert code here
```

## Model Solution
```python
def filter_athletes(athlete_list, criterion_function):
    return [athlete for athlete in athlete_list if criterion_function(athlete)]

athlete_list = [
    {"name": "Anna", "sport": "Tennis"},
    {"name": "Ben", "sport": "Football"},
    {"name": "Clara", "sport": "Swimming"},
    {"name": "David", "sport": "Tennis"}
]

def is_tennis_player(athlete):
    return athlete["sport"] == "Tennis"

filtered_athletes = filter_athletes(athlete_list, is_tennis_player)
print(filtered_athletes)
```

## Unit Tests
```python
import unittest
from main import filter_athletes

class TestFilterAthletes(unittest.TestCase):
    def test_tennis_players(self):
        athlete_list = [
            {"name": "Anna", "sport": "Tennis"},
            {"name": "Ben", "sport": "Football"},
            {"name": "Clara", "sport": "Swimming"},
            {"name": "David", "sport": "Tennis"}
        ]
        def is_tennis_player(athlete):
            return athlete["sport"] == "Tennis"
        self.assertEqual(filter_athletes(athlete_list, is_tennis_player), [
            {"name": "Anna", "sport": "Tennis"},
            {"name": "David", "sport": "Tennis"}
        ])

    def test_football_players(self):
        athlete_list = [
            {"name": "Anna", "sport": "Tennis"},
            {"name": "Ben", "sport": "Football"},
            {"name": "Clara", "sport": "Swimming"},
            {"name": "David", "sport": "Tennis"}
        ]
        def is_football_player(athlete):
            return athlete["sport"] == "Football"
        self.assertEqual(filter_athletes(athlete_list, is_football_player), [
            {"name": "Ben", "sport": "Football"}
        ])

    def test_no_athletes(self):
        athlete_list = []
        def is_tennis_player(athlete):
            return athlete["sport"] == "Tennis"
        self.assertEqual(filter_athletes(athlete_list, is_tennis_player), [])

    def test_all_athletes(self):
        athlete_list = [
            {"name": "Anna", "sport": "Tennis"},
            {"name": "Ben", "sport": "Football"},
            {"name": "Clara", "sport": "Swimming"},
            {"name": "David", "sport": "Tennis"}
        ]
        def all_athletes(athlete):
            return True
        self.assertEqual(filter_athletes(athlete_list, all_athletes), athlete_list)

    def test_no_tennis_players(self):
        athlete_list = [
            {"name": "Ben", "sport": "Football"},
            {"name": "Clara", "sport": "Swimming"}
        ]
        def is_tennis_player(athlete):
            return athlete["sport"] == "Tennis"
        self.assertEqual(filter_athletes(athlete_list, is_tennis_player), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 514
