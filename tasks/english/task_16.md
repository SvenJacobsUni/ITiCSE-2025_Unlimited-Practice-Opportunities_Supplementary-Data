# Input
- Programming Concept: If-Else statements
- Context: Animals

# Generated Task Components
## Task Description
### Exercise: Animal Classification

Write a function named `animal_classification(animal)` that classifies the type of an animal based on the passed string. The function should return a corresponding message with `return`.

- If the animal is a "Dog", the message "This is a mammal." should be returned.
- If the animal is an "Eagle", the message "This is a bird." should be returned.
- If the animal is a "Shark", the message "This is a fish." should be returned.
- For all other animals, the message "Unknown animal class." should be returned.

Example calls:
- `animal_classification("Dog")` returns "This is a mammal."
- `animal_classification("Eagle")` returns "This is a bird."
- `animal_classification("Shark")` returns "This is a fish."
- `animal_classification("Crocodile")` returns "Unknown animal class."


## Code Framework
```python
def animal_classification(animal):
    ## Insert code here

```

## Model Solution
```python
def animal_classification(animal):
    if animal == "Dog":
        return "This is a mammal."
    elif animal == "Eagle":
        return "This is a bird."
    elif animal == "Shark":
        return "This is a fish."
    else:
        return "Unknown animal class."

# Example calls
print(animal_classification("Dog"))
print(animal_classification("Eagle"))
print(animal_classification("Shark"))
print(animal_classification("Crocodile"))

```

## Unit Tests
```python
import unittest

from main import animal_classification

class TestAnimalClassification(unittest.TestCase):
    def test_dog(self):
        self.assertEqual(animal_classification("Dog"), "This is a mammal.")

    def test_eagle(self):
        self.assertEqual(animal_classification("Eagle"), "This is a bird.")

    def test_shark(self):
        self.assertEqual(animal_classification("Shark"), "This is a fish.")

    def test_unknown_animal(self):
        self.assertEqual(animal_classification("Crocodile"), "Unknown animal class.")

    def test_empty_string(self):
        self.assertEqual(animal_classification(""), "Unknown animal class.")

    def test_none(self):
        self.assertEqual(animal_classification(None), "Unknown animal class.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 434
