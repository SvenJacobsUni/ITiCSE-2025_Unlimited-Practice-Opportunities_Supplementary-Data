# Input
- Programming Concept: Integer
- Context: Animals

# Generated Task Components
## Task Description
### Exercise: Count Animals

Write a function named `count_animals(animals)`, which takes a list of animals as input and returns the number of animals in the list as an integer.

Example usage:
```python
tiere = ["Dog", "Cat", "Bird", "Dog", "Cat"]
print(count_animals(animals))  # Output: 5
```

The function should correctly count the number of animals in the list and return it as an integer.

## Code Framework
```python
def count_animals(animals):
    ## Insert code here

```

## Model Solution
```python
def count_animals(animals):
    return len(animals)

animals = ["Dog", "Cat", "Bird", "Dog", "Cat"]
print(count_animals(animals))  # Output: 5

```

## Unit Tests
```python
import unittest
from main import count_animals

class TestCountAnimals(unittest.TestCase):
    def test_empty_list(self):
        self.assertEqual(count_animals([]), 0)

    def test_single_animal(self):
        self.assertEqual(count_animals(["Dog"]), 1)

    def test_multiple_animals(self):
        self.assertEqual(count_animals(["Dog", "Cat", "Bird", "Dog", "Cat"]), 5)

    def test_same_animals(self):
        self.assertEqual(count_animals(["Dog", "Dog", "Dog"]), 3)

    def test_different_animals(self):
        self.assertEqual(count_animals(["Dog", "Cat", "Bird"]), 3)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 500
