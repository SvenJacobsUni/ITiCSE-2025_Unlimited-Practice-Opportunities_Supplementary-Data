# Input
- Programming Concept: Higher-order functions
- Context: Mental Health

# Generated Task Components
## Task Description
### Exercise: Higher-order functions in the context of mental health

Write a function `filter_positive_affirmations(affirmations, filter_function)` that takes a list of positive affirmations and a filter function as arguments. The function should filter the affirmations based on the provided filter function and return the filtered list.

A positive affirmation is a short, positive sentence aimed at boosting self-esteem and mental health. Examples of affirmations are: "I am strong", "I am valuable", "I can achieve anything".

Example call:
```python
affirmations = ["I am strong", "I am valuable", "I can achieve anything", "I am enough"]
def contains_word_i(affirmation):
    return "I" in affirmation

filtered_affirmations = filter_positive_affirmations(affirmations, contains_word_i)
print(filtered_affirmations)  # Output: ["I am strong", "I am valuable", "I can achieve anything", "I am enough"]
```

Implement the function `filter_positive_affirmations` such that it correctly filters and returns the list of affirmations based on the provided filter function.

## Code Framework
```python
def filter_positive_affirmations(affirmations, filter_function):
    ## Insert code here
```

## Model Solution
```python
def filter_positive_affirmations(affirmations, filter_function):
    return list(filter(filter_function, affirmations))

affirmations = ["I am strong", "I am valuable", "I can achieve anything", "I am enough"]
def contains_word_i(affirmation):
    return "I" in affirmation

filtered_affirmations = filter_positive_affirmations(affirmations, contains_word_i)
print(filtered_affirmations)
```

## Unit Tests
```python
import unittest

class TestFilterPositiveAffirmations(unittest.TestCase):
    def test_contains_word_i(self):
        affirmations = ["I am strong", "I am valuable", "I can achieve anything", "I am enough"]
        def contains_word_i(affirmation):
            return "I" in affirmation
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_i), affirmations)

    def test_empty_list(self):
        affirmations = []
        def contains_word_i(affirmation):
            return "I" in affirmation
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_i), [])

    def test_no_match(self):
        affirmations = ["You are strong", "You are valuable", "You can achieve anything", "You are enough"]
        def contains_word_i(affirmation):
            return "I" in affirmation
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_i), [])

    def test_partial_match(self):
        affirmations = ["I am strong", "You are valuable", "I can achieve anything", "You are enough"]
        def contains_word_i(affirmation):
            return "I" in affirmation
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_i), ["I am strong", "I can achieve anything"])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 497
