# Input
- Programming Concept: Tuples;Operations with numbers;Control structures (==, !=, <, >, <=, >=, or, and, not)
- Context: Music

# Generated Task Components
## Task Description
### Exercise: Music Playlist Analysis 

Write a function named `analyse_playlist(playlist)`, that takes a list of tuples as an argument. Each tuple represents a song and contains two elements: the name of the song (String) and the duration of the song in seconds (Integer).

The function should accomplish the following tasks:
1. Check if the playlist contains at least 5 songs. If not, the function should return "Too few songs in the playlist".
2. Find and return the name of the longest song in the playlist.
3. Find and return the name of the shortest song in the playlist.
4. Calculate and return the average duration of the songs in the playlist.

Example call:
```python
playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200)]
analyse_playlist(playlist)
```

Expected return:
```python
("Longest Song: Song C", "Shortest Song: Song D", "Average Duration: 196.0 Seconds")
```

## Code Framework
```python
def analyse_playlist(playlist):
    ## Insert code here
```

## Model Solution
```python
def analyse_playlist(playlist):
    if len(playlist) < 5:
        return "Too few songs in the playlist"
    longest = max(playlist, key=lambda x: x[1])
    shortest = min(playlist, key=lambda x: x[1])
    avg_duration = sum(song[1] for song in playlist) / len(playlist)
    return (f"Longest Song: {longest[0]}", f"Shortest Song: {shortest[0]}", f"Average Duration: {avg_duration:.1f} Seconds")

playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200)]
print(analyse_playlist(playlist))
```

## Unit Tests
```python
import unittest

class TestAnalysePlaylist(unittest.TestCase):
    def test_too_few_songs(self):
        playlist = [("Song A", 210), ("Song B", 180)]
        self.assertEqual(analyse_playlist(playlist), "Too few songs in the playlist")

    def test_longest_song(self):
        playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200)]
        result = analyse_playlist(playlist)
        self.assertIn("Longest Song: Song C", result)

    def test_shortest_song(self):
        playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200)]
        result = analyse_playlist(playlist)
        self.assertIn("Shortest Song: Song D", result)

    def test_average_duration(self):
        playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200)]
        result = analyse_playlist(playlist)
        self.assertIn("Average Duration: 196.0 Seconds", result)

    def test_exactly_five_songs(self):
        playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200)]
        result = analyse_playlist(playlist)
        self.assertEqual(result, ("Longest Song: Song C", "Shortest Song: Song D", "Average Duration: 196.0 Seconds"))

    def test_more_than_five_songs(self):
        playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200), ("Song F", 300)]
        result = analyse_playlist(playlist)
        self.assertEqual(result, ("Longest Song: Song F", "Shortest Song: Song D", "Average Duration: 213.3 Seconds"))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 612
