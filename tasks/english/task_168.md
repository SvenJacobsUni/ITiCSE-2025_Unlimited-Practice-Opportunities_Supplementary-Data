# Input
- Programming Concept: Logical operators (==, !=, <, >, <=, >=, or, and, not); Recursion; For loops
- Context: Streaming Services

# Generated Task Components
## Task Description
### Exercise: Most Popular Show on a Streaming Service

Write a function `most_popular_show(show_list)` that receives a list of shows and their ratings as input and returns the show with the highest rating. Each show in the list is a dictionary with keys `name` and `rating`. The function should recursively find the show with the highest rating.

Example call:
```python
shows = [
    {"name": "Show A", "rating": 8.5},
    {"name": "Show B", "rating": 9.0},
    {"name": "Show C", "rating": 7.8}
]
print(most_popular_show(shows))  # Output: "Show B"
```

Implement the function so that it recursively determines the highest rating and returns the name of the show with the highest rating.

## Code Framework
```python
def most_popular_show(show_list):
    ## Insert code here
```

## Model Solution
```python
def most_popular_show(show_list):
    if len(show_list) == 1:
        return show_list[0]['name']
    rest_best = most_popular_show(show_list[1:])
    return show_list[0]['name'] if show_list[0]['rating'] > next(s['rating'] for s in show_list if s['name'] == rest_best) else rest_best

shows = [
    {"name": "Show A", "rating": 8.5},
    {"name": "Show B", "rating": 9.0},
    {"name": "Show C", "rating": 7.8}
]
print(most_popular_show(shows))  # Output: "Show B"
```

## Unit Tests
```python
import unittest
from main import most_popular_show

class TestMostPopularShow(unittest.TestCase):
    def test_simple_case(self):
        shows = [
            {"name": "Show A", "rating": 8.5},
            {"name": "Show B", "rating": 9.0},
            {"name": "Show C", "rating": 7.8}
        ]
        self.assertEqual(most_popular_show(shows), "Show B")

    def test_same_rating(self):
        shows = [
            {"name": "Show A", "rating": 8.0},
            {"name": "Show B", "rating": 8.0},
            {"name": "Show C", "rating": 8.0}
        ]
        self.assertEqual(most_popular_show(shows), "Show A")

    def test_single_show(self):
        shows = [
            {"name": "Show A", "rating": 8.5}
        ]
        self.assertEqual(most_popular_show(shows), "Show A")

    def test_empty_list(self):
        shows = []
        with self.assertRaises(IndexError):
            most_popular_show(shows)

    def test_negative_ratings(self):
        shows = [
            {"name": "Show A", "rating": -1.0},
            {"name": "Show B", "rating": -2.0},
            {"name": "Show C", "rating": -3.0}
        ]
        self.assertEqual(most_popular_show(shows), "Show A")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 600
