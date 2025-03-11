# Input
- Programming Concept: String
- Context: Fishing

# Generated Task Components
## Task Description
### Exercise: Fishing and Fish

Write a function named `count_fish(text)` that takes a string input and returns the number of times the word "fish" appears in that text. The function should not distinguish between uppercase and lowercase letters.

Example call:
```python
count_fish("I caught three fish today. Fish is my favorite food.")
```

Expected output:
```
2
```

## Code Framework
```python
def count_fish(text):
    ## Insert code here
```

## Model Solution
```python
def count_fish(text):
    print(text.lower().count("fish"))

count_fish("I caught three fish today. Fish is my favorite food.")
```

## Unit Tests
```python
import unittest

from main import count_fish

class TestCountFish(unittest.TestCase):
    def test_simple_text(self):
        self.assertEqual(count_fish("I caught three fish today. Fish is my favorite food."), 2)

    def test_no_fish(self):
        self.assertEqual(count_fish("I caught no fish today."), 1)

    def test_multiple_fish(self):
        self.assertEqual(count_fish("fish fish fish"), 3)

    def test_mixed_case(self):
        self.assertEqual(count_fish("fish Fish FISH"), 3)

    def test_empty_text(self):
        self.assertEqual(count_fish(""), 0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 465
