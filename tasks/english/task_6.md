# Input
- Programming Concept: If-Else statements
- Context: Animals

# Generated Task Components
## Task Description
### Exercise: Animal Classification

Write a function named `animal_classification(animal)` that returns a message based on the passed animal. The function should recognize the following animals and return appropriate messages:

- For "Dog", it should return "That is a loyal companion!"
- For "Cat", it should return "That is an independent friend!"
- For "Bird", it should return "That is a feathered friend!"
- For all other animals, it should return "That is an interesting animal!"

Example calls:

```python
print(animal_classification("Dog"))  # Output: That is a loyal companion!
print(animal_classification("Cat"))  # Output: That is an independent friend!
print(animal_classification("Bird"))  # Output: That is a feathered friend!
print(animal_classification("Fish"))  # Output: That is an interesting animal!
```

## Code Framework
```python
def animal_classification(animal):
    ## Insert code here
```

## Model Solution
```python
def animal_classification(animal):
    if animal == "Dog":
        return "That is a loyal companion!"
    elif animal == "Cat":
        return "That is an independent friend!"
    elif animal == "Bird":
        return "That is a feathered friend!"
    else:
        return "That is an interesting animal!"

print(animal_classification("Dog"))
print(animal_classification("Cat"))
print(animal_classification("Bird"))
print(animal_classification("Fish"))
```

## Unit Tests
```python
import unittest
from main import animal_classification

class TestAnimalClassification(unittest.TestCase):
    def test_dog(self):
        self.assertEqual(animal_classification("Dog"), "That is a loyal companion!")

    def test_cat(self):
        self.assertEqual(animal_classification("Cat"), "That is an independent friend!")

    def test_bird(self):
        self.assertEqual(animal_classification("Bird"), "That is a feathered friend!")

    def test_unknown_animal(self):
        self.assertEqual(animal_classification("Fish"), "That is an interesting animal!")

    def test_empty_string(self):
        self.assertEqual(animal_classification(""), "That is an interesting animal!")

    def test_none(self):
        self.assertEqual(animal_classification(None), "That is an interesting animal!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 424
