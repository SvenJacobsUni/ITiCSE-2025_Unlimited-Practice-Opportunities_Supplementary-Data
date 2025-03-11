# Input
- Programming Concept: If-Else statements; Recursion; Boolean and None
- Context: Rugby

# Generated Task Components
## Task Description
### Exercise: Rugby Player Classification

Write a function `classify_player(weight, height)` that classifies a rugby player based on their weight (in kilograms) and height (in centimeters). The classification is according to the following rules:

- A player is classified as "Lightweight" if their weight is less than 75 kg.
- A player is classified as "Heavyweight" if their weight is 75 kg or more.
- A player is classified as "Tall" if their height is 185 cm or more.
- A player is classified as "Short" if their height is less than 185 cm.

The function should return a message describing the player's classification. Example:

- `classify_player(70, 190)` returns "Lightweight and Tall".
- `classify_player(80, 180)` returns "Heavyweight and Short".

Additionally, a recursive function `is_tall(weight, height)` should be implemented to check if a player is classified as "Tall". This function should return `True` if the player's height is 185 cm or more, and `False` otherwise.

Example calls:
- `classify_player(70, 190)`
- `classify_player(80, 180)`
- `is_tall(70, 190)`
- `is_tall(80, 180)`

## Code Framework
```python
def classify_player(weight, height):
    ## Insert code here

def is_tall(weight, height):
    ## Insert code here
```

## Model Solution
```python
def classify_player(weight, height):
    weight_classification = "Lightweight" if weight < 75 else "Heavyweight"
    height_classification = "Tall" if height >= 185 else "Short"
    return f"{weight_classification} and {height_classification}"

def is_tall(weight, height):
    if height >= 185:
        return True
    return False

print(classify_player(70, 190))
print(classify_player(80, 180))
print(is_tall(70, 190))
print(is_tall(80, 180))
```

## Unit Tests
```python
import unittest

class TestClassifyPlayer(unittest.TestCase):
    def test_lightweight_tall(self):
        self.assertEqual(classify_player(70, 190), "Lightweight and Tall")

    def test_heavyweight_short(self):
        self.assertEqual(classify_player(80, 180), "Heavyweight and Short")

    def test_lightweight_short(self):
        self.assertEqual(classify_player(70, 180), "Lightweight and Short")

    def test_heavyweight_tall(self):
        self.assertEqual(classify_player(80, 190), "Heavyweight and Tall")

class TestIsTall(unittest.TestCase):
    def test_tall(self):
        self.assertTrue(is_tall(70, 190))

    def test_not_tall(self):
        self.assertFalse(is_tall(80, 180))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 623
