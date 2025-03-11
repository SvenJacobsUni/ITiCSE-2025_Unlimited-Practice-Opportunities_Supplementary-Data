# Input
- Programming Concept: Float;Tuple
- Context: Pets

# Generated Task Components
## Task Description
### Exercise: Pet Weight

Write a function named `pet_weight(pets)` that takes a tuple of pets and their weights (in kilograms) as input. The function should calculate and return the average weight of the pets.

Example call:
```python
pets = (("Dog", 20.5), ("Cat", 4.3), ("Hamster", 0.1))
average = pet_weight(pets)
print(average)  # Expected output: 8.3
```

Implement the function so that it correctly calculates and returns the average weight of the pets.

## Code Framework
```python
def pet_weight(pets):
    ## Insert code here
```

## Model Solution
```python
def pet_weight(pets):
    return sum(weight for _, weight in pets) / len(pets)

pets = (("Dog", 20.5), ("Cat", 4.3), ("Hamster", 0.1))
average = pet_weight(pets)
print(average)  # Expected output: 8.3
```

## Unit Tests
```python
import unittest

class TestPetWeight(unittest.TestCase):
    def test_average_weight(self):
        pets = (("Dog", 20.5), ("Cat", 4.3), ("Hamster", 0.1))
        self.assertAlmostEqual(pet_weight(pets), 8.3, places=1)

    def test_empty_list(self):
        pets = ()
        with self.assertRaises(ZeroDivisionError):
            pet_weight(pets)

    def test_single_pet(self):
        pets = (("Dog", 20.5),)
        self.assertEqual(pet_weight(pets), 20.5)

    def test_mixed_weights(self):
        pets = (("Dog", 20.5), ("Cat", 4.3), ("Hamster", 0.1), ("Parrot", 1.2))
        self.assertAlmostEqual(pet_weight(pets), 6.525, places=3)

    def test_negative_weights(self):
        pets = (("Dog", -20.5), ("Cat", -4.3), ("Hamster", -0.1))
        self.assertAlmostEqual(pet_weight(pets), -8.3, places=1)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 538
