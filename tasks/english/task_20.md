# Input
- Programming Concept: Tuples
- Context: Film

# Generated Task Components
## Task Description
### Practice Task: Film Tuples

Write a function named `film_info(film)` that takes a tuple as an argument. The tuple contains information about a film in the following order: title (String), release year (Integer), director (String), and rating (Float).

The function should return a formatted string that displays the film's information in a readable format.

Example call:
```python
film = ("Inception", 2010, "Christopher Nolan", 8.8)
print(film_info(film))
```

Expected output:
```
Title: Inception
Release Year: 2010
Director: Christopher Nolan
Rating: 8.8
```

## Code Framework
```python
def film_info(film):
    ## Insert code here
```

## Model Solution
```python
def film_info(film):
    return f"Title: {film[0]}\nRelease Year: {film[1]}\nDirector: {film[2]}\nRating: {film[3]}"

film = ("Inception", 2010, "Christopher Nolan", 8.8)
print(film_info(film))
```

## Unit Tests
```python
import unittest
from main import film_info

class TestFilmInfo(unittest.TestCase):
    def test_standard_film(self):
        film = ("Inception", 2010, "Christopher Nolan", 8.8)
        expected = "Title: Inception\nRelease Year: 2010\nDirector: Christopher Nolan\nRating: 8.8"
        self.assertEqual(film_info(film), expected)

    def test_film_with_comma_in_title(self):
        film = ("Spider-Man: No Way Home", 2021, "Jon Watts", 8.4)
        expected = "Title: Spider-Man: No Way Home\nRelease Year: 2021\nDirector: Jon Watts\nRating: 8.4"
        self.assertEqual(film_info(film), expected)

    def test_film_with_low_rating(self):
        film = ("The Room", 2003, "Tommy Wiseau", 3.7)
        expected = "Title: The Room\nRelease Year: 2003\nDirector: Tommy Wiseau\nRating: 3.7"
        self.assertEqual(film_info(film), expected)

    def test_film_with_high_rating(self):
        film = ("The Godfather", 1972, "Francis Ford Coppola", 9.2)
        expected = "Title: The Godfather\nRelease Year: 1972\nDirector: Francis Ford Coppola\nRating: 9.2"
        self.assertEqual(film_info(film), expected)

    def test_film_with_integer_rating(self):
        film = ("A Beautiful Mind", 2001, "Ron Howard", 8.0)
        expected = "Title: A Beautiful Mind\nRelease Year: 2001\nDirector: Ron Howard\nRating: 8.0"
        self.assertEqual(film_info(film), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 438
