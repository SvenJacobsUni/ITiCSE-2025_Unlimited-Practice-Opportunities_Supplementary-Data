# Input
- Programming Concept: Recursion
- Context: Virtual Reality

# Generated Task Components
## Task Description
Exercise: Recursive Calculation of VR World Depth

In virtual reality (VR), there are various levels nested within each other. Each level can contain further sub-levels, which in turn can contain more sub-levels, and so on. Your task is to write a function that calculates the maximum depth of these nested levels.

Write a function `calculate_depth(vr_world)` that computes the depth of a VR world. The VR world is represented as a nested list, where each list can contain further lists representing sub-levels.

Example:
```python
vr_world = [[], [[], []], [[[]]], [[], [[], [[], []]]]]
```

In this example, the VR world has a maximum depth of 4.

Implement the function `calculate_depth(vr_world)` that returns the maximum depth of the VR world as an integer.

Example calls:
```python
print(calculate_depth([[], [[], []], [[[]]], [[], [[], [[], []]]]]))  # Output: 4
print(calculate_depth([[], [[], []], [[[]]]]))  # Output: 3
print(calculate_depth([[]]))  # Output: 2
print(calculate_depth([]))  # Output: 1
```

## Code Framework
```python
def calculate_depth(vr_world):
    ## Insert code here
    pass
```

## Model Solution
```python
def calculate_depth(vr_world):
    if not isinstance(vr_world, list):
        return 0
    return 1 + max((calculate_depth(level) for level in vr_world), default=0)

print(calculate_depth([[], [[], []], [[[]]], [[], [[], [[], []]]]]))  # Output: 4
print(calculate_depth([[], [[], []], [[[]]]]))  # Output: 3
print(calculate_depth([[]]))  # Output: 2
print(calculate_depth([]))  # Output: 1
```

## Unit Tests
```python
import unittest
from main import calculate_depth

class TestCalculateDepth(unittest.TestCase):
    def test_simple_vr_world(self):
        self.assertEqual(calculate_depth([[], [[], []], [[[]]], [[], [[], [[], []]]]]), 4)

    def test_medium_vr_world(self):
        self.assertEqual(calculate_depth([[], [[], []], [[[]]]]), 3)

    def test_simple_nesting(self):
        self.assertEqual(calculate_depth([[]]), 2)

    def test_empty_vr_world(self):
        self.assertEqual(calculate_depth([]), 1)

    def test_deeply_nested_vr_world(self):
        self.assertEqual(calculate_depth([[[[[[]]]]]]), 6)

    def test_no_nesting(self):
        self.assertEqual(calculate_depth([1, 2, 3]), 1)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 491
