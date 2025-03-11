# Input
- Programming Concept: Lists; Recursion
- Context: Amusement Park

# Generated Task Components
## Task Description
### Exercise: Amusement Park - Counting Attractions

Write a recursive function named `count_attractions(attractions)` that counts the number of attractions in an amusement park. The list may contain individual attractions as well as further lists of attractions. The function should return the total number of attractions.

Example:

```python
attractions = ["Rollercoaster", ["Ferris Wheel", "Carousel"], "Haunted House", ["Waterslide", ["Log Flume", "Wave Pool"]]]
```

A call to `count_attractions(attractions)` should return the total number of attractions in the list.

```python
print(count_attractions(attractions))  # Output: 7
```

Implement the function `count_attractions(attractions)` that recursively counts the number of attractions in the list.

## Code Framework
```python
def count_attractions(attractions):
    ## Insert code here

```

## Model Solution
```python
def count_attractions(attractions):
    if not attractions:
        return 0
    if isinstance(attractions[0], list):
        return count_attractions(attractions[0]) + count_attractions(attractions[1:])
    return 1 + count_attractions(attractions[1:])

attractions = ["Rollercoaster", ["Ferris Wheel", "Carousel"], "Haunted House", ["Waterslide", ["Log Flume", "Wave Pool"]]]
print(count_attractions(attractions))  # Output: 7

```

## Unit Tests
```python
import unittest

from main import count_attractions

class TestCountAttractions(unittest.TestCase):
    def test_simple_list(self):
        self.assertEqual(count_attractions(["Rollercoaster", "Ferris Wheel", "Carousel"]), 3)

    def test_nested_list(self):
        self.assertEqual(count_attractions(["Rollercoaster", ["Ferris Wheel", "Carousel"], "Haunted House"]), 4)

    def test_deeply_nested_list(self):
        self.assertEqual(count_attractions(["Rollercoaster", ["Ferris Wheel", ["Carousel", "Haunted House"]], "Waterslide"]), 5)

    def test_empty_list(self):
        self.assertEqual(count_attractions([]), 0)

    def test_list_with_empty_sublists(self):
        self.assertEqual(count_attractions(["Rollercoaster", [], "Ferris Wheel", []]), 2)

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 540
