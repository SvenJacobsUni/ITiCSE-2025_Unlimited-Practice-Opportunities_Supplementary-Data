# Input
- Programming Concept: Integer;For loops;Higher-order functions
- Context: Music

# Generated Task Components
## Task Description
### Exercise: Counting Musical Notes

Write a function named `count_notes(musical_piece)` that accepts a list of integers as an argument. Each integer in the list represents a note in a musical piece. The function should count the occurrences of each note and return the result as a dictionary, with the keys being the notes and the values being the count of occurrences.

Example call:
```python
musical_piece = [60, 62, 64, 60, 62, 60, 65, 67, 60]
print(count_notes(musical_piece))
```

Expected output:
```python
{60: 4, 62: 2, 64: 1, 65: 1, 67: 1}
```

Implement the function `count_notes(musical_piece)` so that it correctly counts the occurrences of each note in the list and returns the result as a dictionary.

## Code Framework
```python
def count_notes(musical_piece):
    ## Insert code here
```

## Model Solution
```python
def count_notes(musical_piece):
    return {note: musical_piece.count(note) for note in set(musical_piece)}

musical_piece = [60, 62, 64, 60, 62, 60, 65, 67, 60]
print(count_notes(musical_piece))
```

## Unit Tests
```python
import unittest

from main import count_notes

class TestCountNotes(unittest.TestCase):
    def test_simple_piece(self):
        self.assertEqual(count_notes([60, 62, 64, 60, 62, 60, 65, 67, 60]), {60: 4, 62: 2, 64: 1, 65: 1, 67: 1})

    def test_empty_piece(self):
        self.assertEqual(count_notes([]), {})

    def test_single_note(self):
        self.assertEqual(count_notes([60]), {60: 1})

    def test_all_notes_once(self):
        self.assertEqual(count_notes([60, 61, 62, 63, 64, 65, 66, 67]), {60: 1, 61: 1, 62: 1, 63: 1, 64: 1, 65: 1, 66: 1, 67: 1})

    def test_all_notes_multiple_times(self):
        self.assertEqual(count_notes([60, 60, 61, 61, 62, 62, 63, 63, 64, 64, 65, 65, 66, 66, 67, 67]), {60: 2, 61: 2, 62: 2, 63: 2, 64: 2, 65: 2, 66: 2, 67: 2})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 601
