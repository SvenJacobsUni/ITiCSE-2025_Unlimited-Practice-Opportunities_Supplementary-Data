# Input
- Programming Concept: Boolean and None;For loops;Operations with numbers
- Context: Virtual Reality

# Generated Task Components
## Task Description
### Exercise: Virtual Reality - Visibility Calculation

In virtual reality, it is important to calculate the visibility of objects to optimize performance. Write a function `calculate_visibility(objects)`, which receives a list of objects. Each object is represented by a number indicating the distance of the object from the viewer.

The function should return the number of objects that are within a certain viewing distance. The viewing distance is 100 units. If the list is empty, the function should return `None`.

Example call:
```python
objects = [50, 150, 30, 200, 90]
calculate_visibility(objects)
```
Expected return:
```
3
```

### Requirements:
- Implement the function `calculate_visibility(objects)`.
- The function should return the number of objects within the viewing distance of 100 units.
- If the list is empty, the function should return `None`.

## Code Framework
```python
def calculate_visibility(objects):
    ## Insert code here
```

## Model Solution
```python
def calculate_visibility(objects):
    if not objects:
        return None
    return sum(1 for obj in objects if obj <= 100)

objects = [50, 150, 30, 200, 90]
print(calculate_visibility(objects))
```

## Unit Tests
```python
import unittest
from main import calculate_visibility

class TestCalculateVisibility(unittest.TestCase):
    def test_empty_list(self):
        self.assertIsNone(calculate_visibility([]))

    def test_all_objects_within_view(self):
        self.assertEqual(calculate_visibility([10, 20, 30, 40, 50]), 5)

    def test_no_objects_in_view(self):
        self.assertEqual(calculate_visibility([110, 120, 130, 140, 150]), 0)

    def test_mixed_objects(self):
        self.assertEqual(calculate_visibility([50, 150, 30, 200, 90]), 3)

    def test_boundary_view_distance(self):
        self.assertEqual(calculate_visibility([100, 101, 99, 102, 98]), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 610
