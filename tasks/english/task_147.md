# Input
- Programming Concept: Tuples;For loops
- Context: Animals

# Generated Task Components
## Task Description
### Exercise Task: Animals and Their Habitats

Write a function called `animal_habitat(animals)`, which receives a list of tuples as an argument. Each tuple contains the name of an animal and its habitat. The function should return a list of animals that live in the forest.

Example call:
```python
tiere = [("Lion", "Savannah"), ("Fox", "Forest"), ("Elephant", "Savannah"), ("Deer", "Forest")]
print(animal_habitat(animals))
```

Expected output:
```
['Fox', 'Deer']
```

## Code Framework
```python
def animal_habitat(animals):
    ## Insert code here
```

## Model Solution
```python
def animal_habitat(animals):
    return [animal for animal, habitat in animals if habitat == "Forest"]

animals = [("Lion", "Savannah"), ("Fox", "Forest"), ("Elephant", "Savannah"), ("Deer", "Forest")]
print(animal_habitat(animals))
```

## Unit Tests
```python
import unittest

from main import animal_habitat

class TestAnimalHabitat(unittest.TestCase):
    def test_habitat_forest(self):
        animals = [("Lion", "Savannah"), ("Fox", "Forest"), ("Elephant", "Savannah"), ("Deer", "Forest")]
        self.assertEqual(animal_habitat(animals), ["Fox", "Deer"])

    def test_no_animals_in_forest(self):
        animals = [("Lion", "Savannah"), ("Elephant", "Savannah")]
        self.assertEqual(animal_habitat(animals), [])

    def test_all_animals_in_forest(self):
        animals = [("Fox", "Forest"), ("Deer", "Forest")]
        self.assertEqual(animal_habitat(animals), ["Fox", "Deer"])

    def test_empty_list(self):
        animals = []
        self.assertEqual(animal_habitat(animals), [])

    def test_various_habitats(self):
        animals = [("Lion", "Savannah"), ("Fox", "Forest"), ("Penguin", "Antarctica"), ("Deer", "Forest"), ("Kangaroo", "Australia")]
        self.assertEqual(animal_habitat(animals), ["Fox", "Deer"])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 579
