# Input
- Programming Concept: String
- Context: Modern Gaming

# Generated Task Components
## Task Description
### Exercise: Modern Gaming - Validate Player Tag

Write a function named `is_valid_player_tag(player_tag)` that checks if a given player tag (String) meets the following criteria:

1. The player tag must be between 3 and 16 characters long.
2. The player tag can only contain alphanumeric characters (letters and numbers).
3. The player tag cannot contain spaces.

The function should return `True` if the player tag is valid, and `False` if it is invalid.

Example calls:
- `is_valid_player_tag("Gamer123")` returns `True`.
- `is_valid_player_tag("G@mer")` returns `False`.
- `is_valid_player_tag("Gamer 123")` returns `False`.
- `is_valid_player_tag("G")` returns `False`.

## Code Framework
```python
def is_valid_player_tag(player_tag):
    ## Insert code here
```

## Model Solution
```python
def is_valid_player_tag(player_tag):
    return 3 <= len(player_tag) <= 16 and player_tag.isalnum()

# Example calls
print(is_valid_player_tag("Gamer123"))  # True
print(is_valid_player_tag("G@mer"))     # False
print(is_valid_player_tag("Gamer 123")) # False
print(is_valid_player_tag("G"))         # False
```

## Unit Tests
```python
import unittest
from main import is_valid_player_tag

class TestIsValidPlayerTag(unittest.TestCase):
    def test_valid_player_tag(self):
        self.assertTrue(is_valid_player_tag("Gamer123"))

    def test_invalid_player_tag_special_characters(self):
        self.assertFalse(is_valid_player_tag("G@mer"))

    def test_invalid_player_tag_spaces(self):
        self.assertFalse(is_valid_player_tag("Gamer 123"))

    def test_invalid_player_tag_too_short(self):
        self.assertFalse(is_valid_player_tag("G"))

    def test_invalid_player_tag_too_long(self):
        self.assertFalse(is_valid_player_tag("Gamer1234567890123"))

    def test_valid_player_tag_minimum_length(self):
        self.assertTrue(is_valid_player_tag("abc"))

    def test_valid_player_tag_maximum_length(self):
        self.assertTrue(is_valid_player_tag("Gamer1234567890"))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 469
