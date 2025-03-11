# Input
- Programming Concept: Float; While loops
- Context: Music

# Generated Task Components
## Task Description
### Exercise: Music Playlist

Write a function called `playlist_duration(songs)` that receives a list of songs as input. Each song is represented by its duration in minutes as a float value. The function should calculate and return the total duration of the playlist. Use a `while` loop to calculate the total duration.

Example call:
```python
songs = [3.5, 4.0, 2.75, 5.25]
print(playlist_duration(songs))  # Output: 15.5
```

### Requirements:
- The function should use a `while` loop.
- The function should return the total playlist duration as a float value.

## Code Framework
```python
def playlist_duration(songs):
    ## Insert code here
```

## Model Solution
```python
def playlist_duration(songs):
    i, total = 0, 0.0
    while i < len(songs):
        total += songs[i]
        i += 1
    return total

songs = [3.5, 4.0, 2.75, 5.25]
print(playlist_duration(songs))
```

## Unit Tests
```python
import unittest
from main import playlist_duration

class TestPlaylistDuration(unittest.TestCase):
    def test_simple_playlist(self):
        self.assertEqual(playlist_duration([3.5, 4.0, 2.75, 5.25]), 15.5)

    def test_empty_playlist(self):
        self.assertEqual(playlist_duration([]), 0.0)

    def test_single_song(self):
        self.assertEqual(playlist_duration([4.5]), 4.5)

    def test_mixed_lengths(self):
        self.assertEqual(playlist_duration([1.0, 2.5, 3.75, 4.25]), 11.5)

    def test_large_playlist(self):
        self.assertEqual(playlist_duration([1.0] * 1000), 1000.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 576
