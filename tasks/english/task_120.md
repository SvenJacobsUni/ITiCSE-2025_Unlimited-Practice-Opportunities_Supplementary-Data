# Input
- Programming Concept: String; Lists
- Context: Film

# Generated Task Components
## Task Description
### Exercise Task: Film Genres

Write a function named `film_genres(movies)` that takes a list of movie titles as input. Each movie title is a string that contains the title of the movie and the genre in parentheses, e.g., "Inception (Sci-Fi)". The function should return a list of the genres that appear in the input list. The genres should appear only once in the output list, even if they occur multiple times in the input list.

Example call:
```python
movies = ["Inception (Sci-Fi)", "Titanic (Romance)", "The Matrix (Sci-Fi)", "The Notebook (Romance)"]
print(film_genres(movies))
```

Expected Output:
```
['Sci-Fi', 'Romance']
```

## Code Framework
```python
def film_genres(movies):
    ## Insert code here
```

## Model Solution
```python
def film_genres(movies):
    return list({movie.split('(')[-1].strip(')') for movie in movies})

movies = ["Inception (Sci-Fi)", "Titanic (Romance)", "The Matrix (Sci-Fi)", "The Notebook (Romance)"]
print(film_genres(movies))
```

## Unit Tests
```python
import unittest

class TestFilmGenres(unittest.TestCase):
    def test_simple_case(self):
        movies = ["Inception (Sci-Fi)", "Titanic (Romance)", "The Matrix (Sci-Fi)", "The Notebook (Romance)"]
        self.assertEqual(set(film_genres(movies)), {"Sci-Fi", "Romance"})

    def test_empty_list(self):
        movies = []
        self.assertEqual(film_genres(movies), [])

    def test_single_genre(self):
        movies = ["Inception (Sci-Fi)"]
        self.assertEqual(film_genres(movies), ["Sci-Fi"])

    def test_multiple_genres(self):
        movies = ["Inception (Sci-Fi)", "Titanic (Romance)", "Avatar (Action)", "The Notebook (Romance)"]
        self.assertEqual(set(film_genres(movies)), {"Sci-Fi", "Romance", "Action"})

    def test_various_cases(self):
        movies = ["Inception (Sci-Fi)", "Titanic (romance)", "Avatar (Action)", "The Notebook (Romance)"]
        self.assertEqual(set(film_genres(movies)), {"Sci-Fi", "romance", "Action", "Romance"})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 552
