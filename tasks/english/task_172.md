# Input
- Programming Concept: Float;Higher-order functions;Integer
- Context: Animals

# Generated Task Components
## Task Description
### Exercise: Animals and Their Characteristics

Write a function named `animal_info(animal, characteristic)` that returns information about different animals and their characteristics. The function should accept two parameters: `animal` (a string) and `characteristic` (a string). 

The function should support the following animals and characteristics:

- Dog:
  - "weight" (Float): Returns the average weight of a dog in kilograms.
  - "legs" (Integer): Returns the number of legs a dog has.
- Cat:
  - "weight" (Float): Returns the average weight of a cat in kilograms.
  - "legs" (Integer): Returns the number of legs a cat has.
- Bird:
  - "weight" (Float): Returns the average weight of a bird in kilograms.
  - "legs" (Integer): Returns the number of legs a bird has.

Example calls:
- `animal_info("Dog", "weight")` should return the average weight of a dog.
- `animal_info("Cat", "legs")` should return the number of legs a cat has.

Implement the function so that it returns the corresponding values.

## Code Framework
```python
def animal_info(animal, characteristic):
    ## Insert code here
```

## Model Solution
```python
def animal_info(animal, characteristic):
    data = {
        "Dog": {"weight": 30.0, "legs": 4},
        "Cat": {"weight": 4.5, "legs": 4},
        "Bird": {"weight": 0.1, "legs": 2}
    }
    return data[animal][characteristic]

print(animal_info("Dog", "weight"))
print(animal_info("Cat", "legs"))
print(animal_info("Bird", "weight"))
```

## Unit Tests
```python
import unittest
from main import animal_info

class TestAnimalInfo(unittest.TestCase):
    def test_dog_weight(self):
        self.assertEqual(animal_info("Dog", "weight"), 30.0)

    def test_dog_legs(self):
        self.assertEqual(animal_info("Dog", "legs"), 4)

    def test_cat_weight(self):
        self.assertEqual(animal_info("Cat", "weight"), 4.5)

    def test_cat_legs(self):
        self.assertEqual(animal_info("Cat", "legs"), 4)

    def test_bird_weight(self):
        self.assertEqual(animal_info("Bird", "weight"), 0.1)

    def test_bird_legs(self):
        self.assertEqual(animal_info("Bird", "legs"), 2)

    def test_unknown_animal(self):
        with self.assertRaises(KeyError):
            animal_info("Elephant", "weight")

    def test_unknown_characteristic(self):
        with self.assertRaises(KeyError):
            animal_info("Dog", "color")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 604
