# Input
- Programming Concept: Higher-order functions
- Context: Mental Health

# Generated Task Components
## Task Description
### Exercise: Higher-order functions in the context of mental health

Write a function `filter_positive_affirmations(affirmations, filter_function)` that receives a list of affirmations (positive statements) and a filter function as arguments. The function should filter the affirmations based on the given filter function and return the filtered list.

Example call:
```python
affirmations = [
    "I am strong.",
    "I am valuable.",
    "I can achieve anything.",
    "I am loved.",
    "I am enough."
]

def contains_word_i(affirmation):
    return "I" in affirmation

positive_affirmations = filter_positive_affirmations(affirmations, contains_word_i)
print(positive_affirmations)
```

Expected output:
```
["I am strong.", "I am valuable.", "I can achieve anything.", "I am loved.", "I am enough."]
```

Implement the function `filter_positive_affirmations` and test it with different filter functions.

## Code Framework
```python
def filter_positive_affirmations(affirmations, filter_function):
    ## Insert code here
```

## Model Solution
```python
def filter_positive_affirmations(affirmations, filter_function):
    return list(filter(filter_function, affirmations))

affirmations = [
    "I am strong.",
    "I am valuable.",
    "I can achieve anything.",
    "I am loved.",
    "I am enough."
]

def contains_word_i(affirmation):
    return "I" in affirmation

positive_affirmations = filter_positive_affirmations(affirmations, contains_word_i)
print(positive_affirmations)
```

## Unit Tests
```python
import unittest

class TestFilterPositiveAffirmations(unittest.TestCase):
    def test_contains_word_i(self):
        affirmations = [
            "I am strong.",
            "I am valuable.",
            "I can achieve anything.",
            "I am loved.",
            "I am enough."
        ]
        def contains_word_i(affirmation):
            return "I" in affirmation
        expected = [
            "I am strong.",
            "I am valuable.",
            "I can achieve anything.",
            "I am loved.",
            "I am enough."
        ]
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_i), expected)

    def test_contains_word_am(self):
        affirmations = [
            "I am strong.",
            "I am valuable.",
            "I can achieve anything.",
            "I am loved.",
            "I am enough."
        ]
        def contains_word_am(affirmation):
            return "am" in affirmation
        expected = [
            "I am strong.",
            "I am valuable.",
            "I am loved.",
            "I am enough."
        ]
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_am), expected)

    def test_no_match(self):
        affirmations = [
            "I am strong.",
            "I am valuable.",
            "I can achieve anything.",
            "I am loved.",
            "I am enough."
        ]
        def contains_word_xyz(affirmation):
            return "xyz" in affirmation
        expected = []
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_xyz), expected)

    def test_empty_list(self):
        affirmations = []
        def contains_word_i(affirmation):
            return "I" in affirmation
        expected = []
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_i), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 432
