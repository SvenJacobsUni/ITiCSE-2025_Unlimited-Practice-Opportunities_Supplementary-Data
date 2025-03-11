# Input
- Programming Concept: If-Else statements
- Context: Music

# Generated Task Components
## Task Description
### Practice Task: Music Genre Recommendation

Write a function named `music_recommendation(genre)` that returns a corresponding message based on the provided music genre. The function should consider the following genres:

- For "Rock", the message "You like it loud and energetic!" should be returned.
- For "Pop", the message "You love catchy melodies and rhythms!" should be returned.
- For "Jazz", the message "You appreciate complex harmonies and improvisation!" should be returned.
- For "Classical", the message "You enjoy timeless masterpieces and orchestral sounds!" should be returned.

If another genre is provided, the message "Genre not recognized. Try Rock, Pop, Jazz, or Classical." should be returned.

Example calls:
- `music_recommendation("Rock")` returns "You like it loud and energetic!".
- `music_recommendation("Hip-Hop")` returns "Genre not recognized. Try Rock, Pop, Jazz, or Classical.".

## Code Framework
```python
def music_recommendation(genre):
    ## Insert code here
```

## Model Solution
```python
def music_recommendation(genre):
    if genre == "Rock":
        return "You like it loud and energetic!"
    elif genre == "Pop":
        return "You love catchy melodies and rhythms!"
    elif genre == "Jazz":
        return "You appreciate complex harmonies and improvisation!"
    elif genre == "Classical":
        return "You enjoy timeless masterpieces and orchestral sounds!"
    else:
        return "Genre not recognized. Try Rock, Pop, Jazz, or Classical."

# Example calls
print(music_recommendation("Rock"))
print(music_recommendation("Hip-Hop"))
```

## Unit Tests
```python
import unittest
from main import music_recommendation

class TestMusicRecommendation(unittest.TestCase):
    def test_rock(self):
        self.assertEqual(music_recommendation("Rock"), "You like it loud and energetic!")

    def test_pop(self):
        self.assertEqual(music_recommendation("Pop"), "You love catchy melodies and rhythms!")

    def test_jazz(self):
        self.assertEqual(music_recommendation("Jazz"), "You appreciate complex harmonies and improvisation!")

    def test_classical(self):
        self.assertEqual(music_recommendation("Classical"), "You enjoy timeless masterpieces and orchestral sounds!")

    def test_unknown_genre(self):
        self.assertEqual(music_recommendation("Hip-Hop"), "Genre not recognized. Try Rock, Pop, Jazz, or Classical.")

    def test_empty_genre(self):
        self.assertEqual(music_recommendation(""), "Genre not recognized. Try Rock, Pop, Jazz, or Classical.")

    def test_none_genre(self):
        self.assertEqual(music_recommendation(None), "Genre not recognized. Try Rock, Pop, Jazz, or Classical.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 426
