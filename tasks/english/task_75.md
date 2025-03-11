# Input
- Programming Concept: Integer
- Context: Pets

# Generated Task Components
## Task Description
### Exercise: Counting Pets

Write a function named `count_pets(dogs, cats)`, which takes two integer parameters: the number of dogs and the number of cats in a household. The function should calculate and return the total number of pets.

Example call:
```python
total = count_pets(3, 2)
print(total)  # Output: 5
```

In this example, there are 3 dogs and 2 cats, resulting in a total of 5 pets.

## Code Framework
```python
def count_pets(dogs, cats):
    ## Insert code here
```

## Model Solution
```python
def count_pets(dogs, cats):
    return dogs + cats

print(count_pets(3, 2))  # Output: 5
```

## Unit Tests
```python
import unittest
from main import count_pets

class TestCountPets(unittest.TestCase):
    def test_no_pets(self):
        self.assertEqual(count_pets(0, 0), 0)

    def test_only_dogs(self):
        self.assertEqual(count_pets(5, 0), 5)

    def test_only_cats(self):
        self.assertEqual(count_pets(0, 3), 3)

    def test_dogs_and_cats(self):
        self.assertEqual(count_pets(2, 4), 6)

    def test_large_numbers(self):
        self.assertEqual(count_pets(1000, 2000), 3000)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 493
