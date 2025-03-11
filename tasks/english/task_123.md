# Input
- Programming Concept: While loops;If-Else statements
- Context: Music

# Generated Task Components
## Task Description
### Exercise Task: Music Playlist

Write a function named `play_playlist(songs)` that takes a list of songs as an argument. The function should play each song in the list until a specific song named "Stop" is found. If the song "Stop" is found, the playback should stop. If the song "Stop" is not in the list, the entire playlist should be played.

Example call:
```python
play_playlist(["Song1", "Song2", "Stop", "Song3"])
```

Expected behavior:
- "Song1" is played.
- "Song2" is played.
- Playback is stopped because "Stop" was found.

## Code Framework
```python
def play_playlist(songs):
    ## Insert code here
```

## Model Solution
```python
def play_playlist(songs):
    for song in songs:
        if song == "Stop":
            break
        print(f"Playing {song}")

play_playlist(["Song1", "Song2", "Stop", "Song3"])
```

## Unit Tests
```python
import unittest
from main import play_playlist
from io import StringIO
import sys

class TestPlayPlaylist(unittest.TestCase):
    def test_playlist_with_stop(self):
        songs = ["Song1", "Song2", "Stop", "Song3"]
        expected_output = "Playing Song1\nPlaying Song2\n"
        captured_output = StringIO()
        sys.stdout = captured_output
        play_playlist(songs)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue(), expected_output)

    def test_playlist_without_stop(self):
        songs = ["Song1", "Song2", "Song3"]
        expected_output = "Playing Song1\nPlaying Song2\nPlaying Song3\n"
        captured_output = StringIO()
        sys.stdout = captured_output
        play_playlist(songs)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue(), expected_output)

    def test_empty_playlist(self):
        songs = []
        expected_output = ""
        captured_output = StringIO()
        sys.stdout = captured_output
        play_playlist(songs)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue(), expected_output)

    def test_playlist_only_stop(self):
        songs = ["Stop"]
        expected_output = ""
        captured_output = StringIO()
        sys.stdout = captured_output
        play_playlist(songs)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue(), expected_output)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 555
