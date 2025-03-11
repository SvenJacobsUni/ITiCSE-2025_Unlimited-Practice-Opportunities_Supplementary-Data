# Input
- Programming Concept: Tuples;Integer;Logical operators (==, !=, <, >, <=, >=, or, and, not)
- Context: Pets

# Generated Task Components
## Task Description
### Exercise: Pet Check

Write a function named `pet_check(pet)`, which checks if the given pet is included in a predefined list of allowed pets. The list of allowed pets is a tuple and includes the following animals: "Dog", "Cat", "Hamster", "Rabbit", "Parrot".

The function should:
1. Check if the given pet is included in the list of allowed pets.
2. If the pet is allowed, the function should return `True`.
3. If the pet is not allowed, the function should return `False`.

Example calls:
- `pet_check("Dog")` returns `True`.
- `pet_check("Snake")` returns `False`.

## Code Framework
```python
def pet_check(pet):
    ## Insert code here

```

## Model Solution
```python
def pet_check(pet):
    return pet in ("Dog", "Cat", "Hamster", "Rabbit", "Parrot")

# Example calls
print(pet_check("Dog"))  # True
print(pet_check("Snake"))  # False

```

## Unit Tests
```python
import unittest

from main import pet_check

class TestPetCheck(unittest.TestCase):
    def test_allowed_pet_dog(self):
        self.assertTrue(pet_check("Dog"))

    def test_allowed_pet_cat(self):
        self.assertTrue(pet_check("Cat"))

    def test_not_allowed_pet_snake(self):
        self.assertFalse(pet_check("Snake"))

    def test_not_allowed_pet_horse(self):
        self.assertFalse(pet_check("Horse"))

    def test_allowed_pet_hamster(self):
        self.assertTrue(pet_check("Hamster"))

    def test_allowed_pet_rabbit(self):
        self.assertTrue(pet_check("Rabbit"))

    def test_allowed_pet_parrot(self):
        self.assertTrue(pet_check("Parrot"))

    def test_empty_string(self):
        self.assertFalse(pet_check(""))

    def test_none(self):
        self.assertFalse(pet_check(None))

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 615
