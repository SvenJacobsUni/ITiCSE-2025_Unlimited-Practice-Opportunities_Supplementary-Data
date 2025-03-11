# Input
- Programming Concept: Recursion
- Context: Music

# Generated Task Components
## Task Description
### Exercise Task: Recursive Music Notes

Write a function named `play_note_sequence(notes)` that recursively iterates over a list of musical notes (as strings) and prints each note to the console. The function should print the notes in the order they appear in the list.

Example call:
```python
play_note_sequence(["C", "D", "E", "F", "G"])
```

Output:
```
C
D
E
F
G
```

Implement the function so that it works recursively.

## Code Framework
```python
def play_note_sequence(notes):
    ## Insert code here
```

## Model Solution
```python
def play_note_sequence(notes):
    if not notes:
        return
    print(notes[0])
    play_note_sequence(notes[1:])

play_note_sequence(["C", "D", "E", "F", "G"])
```

## Unit Tests
```python
import unittest
from unittest.mock import patch
from main import play_note_sequence

class TestPlayNoteSequence(unittest.TestCase):
    @patch('builtins.print')
    def test_simple_note_sequence(self, mock_print):
        play_note_sequence(["C", "D", "E", "F", "G"])
        mock_print.assert_has_calls([unittest.mock.call("C"), unittest.mock.call("D"), unittest.mock.call("E"), unittest.mock.call("F"), unittest.mock.call("G")])

    @patch('builtins.print')
    def test_empty_note_sequence(self, mock_print):
        play_note_sequence([])
        mock_print.assert_not_called()

    @patch('builtins.print')
    def test_single_note(self, mock_print):
        play_note_sequence(["A"])
        mock_print.assert_called_once_with("A")

    @patch('builtins.print')
    def test_nested_note_sequence(self, mock_print):
        play_note_sequence(["A", "B", "C", "D", "E"])
        mock_print.assert_has_calls([unittest.mock.call("A"), unittest.mock.call("B"), unittest.mock.call("C"), unittest.mock.call("D"), unittest.mock.call("E")])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 486
