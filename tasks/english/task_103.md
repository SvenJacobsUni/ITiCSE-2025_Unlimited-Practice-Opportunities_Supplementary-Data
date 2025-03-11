# Input
- Programming Concept: Boolean and None; Float
- Context: Animals

# Generated Task Components
## Task Description
### Exercise: Animal Information

Write a function named `animal_info(name, weight)`, which returns information about an animal based on its name and weight. The function should fulfill the following requirements:

1. If the name of the animal is "Elephant" and the weight is greater than 5000.0 (in kilograms), the function should return `True`.
2. If the name of the animal is "Mouse" and the weight is less than 0.05 (in kilograms), the function should return `True`.
3. In all other cases, the function should return `None`.

Example calls:
- `animal_info("Elephant", 6000.0)` returns `True`.
- `animal_info("Mouse", 0.03)` returns `True`.
- `animal_info("Dog", 10.0)` returns `None`.

## Code Framework
```python
def animal_info(name, weight):
    ## Insert code here
```

## Model Solution
```python
def animal_info(name, weight):
    if name == "Elephant" and weight > 5000.0:
        return True
    if name == "Mouse" and weight < 0.05:
        return True
    return None

print(animal_info("Elephant", 6000.0))  # True
print(animal_info("Mouse", 0.03))       # True
print(animal_info("Dog", 10.0))         # None
```

## Unit Tests
```python
import unittest

from main import animal_info

class TestAnimalInfo(unittest.TestCase):
    def test_elephant_heavy(self):
        self.assertEqual(animal_info("Elephant", 6000.0), True)

    def test_mouse_light(self):
        self.assertEqual(animal_info("Mouse", 0.03), True)

    def test_dog(self):
        self.assertEqual(animal_info("Dog", 10.0), None)

    def test_elephant_light(self):
        self.assertEqual(animal_info("Elephant", 4000.0), None)

    def test_mouse_heavy(self):
        self.assertEqual(animal_info("Mouse", 0.1), None)

    def test_edge_case_elephant(self):
        self.assertEqual(animal_info("Elephant", 5000.0), None)

    def test_edge_case_mouse(self):
        self.assertEqual(animal_info("Mouse", 0.05), None)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 535
