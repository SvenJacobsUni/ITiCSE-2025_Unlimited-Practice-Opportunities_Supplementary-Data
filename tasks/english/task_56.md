# Input
- Programming Concept: Higher-order functions
- Context: Mental Health

# Generated Task Components
## Task Description
### Exercise Task: Higher-order functions in the context of mental health

Write a function `filter_positive_thoughts(thoughts, filter_function)` that takes a list of thoughts (`thoughts`) and a filter function (`filter_function`) as arguments. The function should apply the `filter_function` to each thought and return only the positive thoughts.

A thought is considered positive if the `filter_function` returns `True` for that thought.

Example call:
```python
def is_positive(thought):
    positive_keywords = ["happy", "content", "successful", "loved"]
    return any(keyword in thought for keyword in positive_keywords)

thoughts = ["I feel happy", "Today was a tough day", "I am content with my work", "I feel loved"]
positive_thoughts = filter_positive_thoughts(thoughts, is_positive)
print(positive_thoughts)
```

Expected output:
```
["I feel happy", "I am content with my work", "I feel loved"]
```

Implement the function `filter_positive_thoughts(thoughts, filter_function)`.

## Code Framework
```python
def filter_positive_thoughts(thoughts, filter_function):
    ## Insert code here

```

## Model Solution
```python
def filter_positive_thoughts(thoughts, filter_function):
    return [thought for thought in thoughts if filter_function(thought)]

def is_positive(thought):
    positive_keywords = ["happy", "content", "successful", "loved"]
    return any(keyword in thought for keyword in positive_keywords)

thoughts = ["I feel happy", "Today was a tough day", "I am content with my work", "I feel loved"]
positive_thoughts = filter_positive_thoughts(thoughts, is_positive)
print(positive_thoughts)

```

## Unit Tests
```python
import unittest

from main import filter_positive_thoughts

def is_positive(thought):
    positive_keywords = ["happy", "content", "successful", "loved"]
    return any(keyword in thought for keyword in positive_keywords)

class TestFilterPositiveThoughts(unittest.TestCase):
    def test_all_positive(self):
        thoughts = ["I feel happy", "I am content", "I feel loved"]
        self.assertEqual(filter_positive_thoughts(thoughts, is_positive), thoughts)

    def test_no_positive(self):
        thoughts = ["Today was a tough day", "I am tired", "It was a bad day"]
        self.assertEqual(filter_positive_thoughts(thoughts, is_positive), [])

    def test_mixed_thoughts(self):
        thoughts = ["I feel happy", "Today was a tough day", "I am content with my work", "I feel loved"]
        expected = ["I feel happy", "I am content with my work", "I feel loved"]
        self.assertEqual(filter_positive_thoughts(thoughts, is_positive), expected)

    def test_empty_list(self):
        self.assertEqual(filter_positive_thoughts([], is_positive), [])

    def test_no_keywords(self):
        thoughts = ["I feel okay", "It was a day", "Nothing special"]
        self.assertEqual(filter_positive_thoughts(thoughts, is_positive), [])

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 474
