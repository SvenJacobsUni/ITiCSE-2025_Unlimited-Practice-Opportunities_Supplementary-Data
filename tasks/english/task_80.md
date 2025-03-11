# Input
- Programming Concept: Recursion
- Context: Pets

# Generated Task Components
## Task Description
### Exercise: Recursive Counting of Pets

Write a recursive function named `count_pets(pets)` that counts the number of pets in a nested list. The list may contain both individual pets and further lists of pets.

Example:
```python
pets = ["Dog", ["Cat", "Bird"], ["Fish", ["Hamster", "Rabbit"]]]
```

A call to `count_pets(pets)` should return the total number of pets in the list.

```python
count_pets(pets)  # should return 6
```

Implement the function `count_pets(pets)` that correctly counts the number of pets in the nested list.

## Code Framework
```python
def count_pets(pets):
    ## Insert code here
```

## Model Solution
```python
def count_pets(pets):
    if not pets:
        return 0
    if isinstance(pets[0], list):
        return count_pets(pets[0]) + count_pets(pets[1:])
    return 1 + count_pets(pets[1:])

pets = ["Dog", ["Cat", "Bird"], ["Fish", ["Hamster", "Rabbit"]]]
print(count_pets(pets))  # should return 6
```

## Unit Tests
```python
import unittest
from main import count_pets

class TestCountPets(unittest.TestCase):
    def test_simple_list(self):
        self.assertEqual(count_pets(["Dog", "Cat", "Bird"]), 3)

    def test_nested_list(self):
        self.assertEqual(count_pets(["Dog", ["Cat", "Bird"], ["Fish", ["Hamster", "Rabbit"]]]), 6)

    def test_empty_list(self):
        self.assertEqual(count_pets([]), 0)

    def test_single_pet(self):
        self.assertEqual(count_pets(["Dog"]), 1)

    def test_deeply_nested_list(self):
        self.assertEqual(count_pets(["Dog", ["Cat", ["Bird", ["Fish", ["Hamster", "Rabbit"]]]]]), 6)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 498
