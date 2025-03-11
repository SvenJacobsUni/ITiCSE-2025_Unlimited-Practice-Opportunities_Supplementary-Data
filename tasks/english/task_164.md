# Input
- Programming Concept: Tuples; Float; Higher-order functions
- Context: Gardening

# Generated Task Components
## Task Description
### Exercise: Gardening with Python

Write a function called `calculate_areas(tuple_list, function)` that takes a list of tuples and a function as arguments. Each tuple in the list represents the length and width of a rectangular garden bed in meters. The function passed as the second argument should be applied to each tuple to calculate the area of the respective garden bed. The `calculate_areas` function should return a list of the calculated areas.

Example call:
```python
def area(tuple):
    return tuple[0] * tuple[1]

garden_beds = [(2.5, 3.0), (4.0, 1.5), (3.5, 2.0)]
print(calculate_areas(garden_beds, area))
```

Expected Output:
```
[7.5, 6.0, 7.0]
```

Implement the `calculate_areas(tuple_list, function)` function.

## Code Framework
```python
def calculate_areas(tuple_list, function):
    ## Insert code here

```

## Model Solution
```python
def calculate_areas(tuple_list, function):
    return [function(t) for t in tuple_list]

def area(tuple):
    return tuple[0] * tuple[1]

garden_beds = [(2.5, 3.0), (4.0, 1.5), (3.5, 2.0)]
print(calculate_areas(garden_beds, area))
```

## Unit Tests
```python
import unittest
from main import calculate_areas

def area(tuple):
    return tuple[0] * tuple[1]

class TestCalculateAreas(unittest.TestCase):
    def test_simple_areas(self):
        garden_beds = [(2.5, 3.0), (4.0, 1.5), (3.5, 2.0)]
        self.assertEqual(calculate_areas(garden_beds, area), [7.5, 6.0, 7.0])

    def test_empty_list(self):
        garden_beds = []
        self.assertEqual(calculate_areas(garden_beds, area), [])

    def test_single_element(self):
        garden_beds = [(5.0, 5.0)]
        self.assertEqual(calculate_areas(garden_beds, area), [25.0])

    def test_zero_area(self):
        garden_beds = [(0, 5.0), (5.0, 0)]
        self.assertEqual(calculate_areas(garden_beds, area), [0.0, 0.0])

    def test_negative_values(self):
        garden_beds = [(-2.0, 3.0), (4.0, -1.5)]
        self.assertEqual(calculate_areas(garden_beds, area), [-6.0, -6.0])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 596
