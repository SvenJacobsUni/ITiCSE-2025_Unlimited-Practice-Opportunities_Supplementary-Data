# Input
- Programming Concept: Boolean and None
- Context: Pets

# Generated Task Components
## Task Description
### Exercise: Pets and Boolean

Write a function named `is_pet(name)` that checks if the given name belongs to a known pet. The function should return `True` if the name is in the list of known pets, and `False` if not. If the name is `None`, the function should also return `False`.

Known pets are:
- "Dog"
- "Cat"
- "Hamster"
- "Rabbit"
- "Parrot"

Example calls:
- `is_pet("Dog")` returns `True`.
- `is_pet("Elephant")` returns `False`.
- `is_pet(None)` returns `False`.

## Code Framework
```python
def is_pet(name):
    ## Insert code here
```

## Model Solution
```python
def is_pet(name):
    return name in ["Dog", "Cat", "Hamster", "Rabbit", "Parrot"]

# Test cases
print(is_pet("Dog"))      # True
print(is_pet("Elephant"))   # False
print(is_pet(None))        # False
```

## Unit Tests
```python
import unittest
from main import is_pet

class TestIsPet(unittest.TestCase):
    def test_dog(self):
        self.assertTrue(is_pet("Dog"))

    def test_cat(self):
        self.assertTrue(is_pet("Cat"))

    def test_hamster(self):
        self.assertTrue(is_pet("Hamster"))

    def test_rabbit(self):
        self.assertTrue(is_pet("Rabbit"))

    def test_parrot(self):
        self.assertTrue(is_pet("Parrot"))

    def test_elephant(self):
        self.assertFalse(is_pet("Elephant"))

    def test_none(self):
        self.assertFalse(is_pet(None))

    def test_empty_string(self):
        self.assertFalse(is_pet(""))

    def test_unknown_animal(self):
        self.assertFalse(is_pet("Tiger"))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 515
