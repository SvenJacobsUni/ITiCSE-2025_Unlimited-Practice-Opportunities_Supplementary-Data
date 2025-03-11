# Input
- Programming Concept: Float
- Context: Music

# Generated Task Components
## Task Description
### Practice Task: Music Streaming Duration

Write a function named `calculate_play_duration(songs)` that receives a list of songs. Each song is represented by its play duration in minutes as a float value. The function should calculate and return the total play duration of the songs in hours.

Example call:
```python
songs = [3.5, 4.2, 5.0, 2.8]
print(calculate_play_duration(songs))  # Output: 0.25
```

Note: The output should be returned in hours as a float value.

## Code Framework
```python
def calculate_play_duration(songs):
    ## Insert code here

```

## Model Solution
```python
def calculate_play_duration(songs):
    return sum(songs) / 60

songs = [3.5, 4.2, 5.0, 2.8]
print(calculate_play_duration(songs))
```

## Unit Tests
```python
import unittest
from main import calculate_play_duration

class TestCalculatePlayDuration(unittest.TestCase):
    def test_simple_list(self):
        self.assertAlmostEqual(calculate_play_duration([3.5, 4.2, 5.0, 2.8]), 0.25)

    def test_empty_list(self):
        self.assertAlmostEqual(calculate_play_duration([]), 0.0)

    def test_single_song(self):
        self.assertAlmostEqual(calculate_play_duration([60.0]), 1.0)

    def test_mixed_values(self):
        self.assertAlmostEqual(calculate_play_duration([30.0, 45.0, 15.0]), 1.5)

    def test_large_values(self):
        self.assertAlmostEqual(calculate_play_duration([120.0, 180.0, 240.0]), 9.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 487
