# Input
- Programming Concept: String; Functions as variables; Lists
- Context: Streaming Services

# Generated Task Components
## Task Description
### Exercise Task: Streaming Services

Write a function named `filter_genres(movies, genre)`, which takes a list of movies and a genre as parameters. Each movie is a dictionary with the keys "title" and "genre". The function should return a new list containing only the movies that match the specified genre.

Example call:
```python
movies = [
    {"title": "Film A", "genre": "Action"},
    {"title": "Film B", "genre": "Drama"},
    {"title": "Film C", "genre": "Action"},
    {"title": "Film D", "genre": "Comedy"}
]

result = filter_genres(movies, "Action")
# result should be [{"title": "Film A", "genre": "Action"}, {"title": "Film C", "genre": "Action"}]
```

Implement the `filter_genres(movies, genre)` function to fulfill the functionality as described above.

## Code Framework
```python
def filter_genres(movies, genre):
    ## Insert code here

```

## Model Solution
```python
def filter_genres(movies, genre):
    return [movie for movie in movies if movie['genre'] == genre]

movies = [
    {"title": "Film A", "genre": "Action"},
    {"title": "Film B", "genre": "Drama"},
    {"title": "Film C", "genre": "Action"},
    {"title": "Film D", "genre": "Comedy"}
]

result = filter_genres(movies, "Action")
print(result)

```

## Unit Tests
```python
import unittest
from main import filter_genres

class TestFilterGenres(unittest.TestCase):
    def test_action_genre(self):
        movies = [
            {"title": "Film A", "genre": "Action"},
            {"title": "Film B", "genre": "Drama"},
            {"title": "Film C", "genre": "Action"},
            {"title": "Film D", "genre": "Comedy"}
        ]
        self.assertEqual(filter_genres(movies, "Action"), [
            {"title": "Film A", "genre": "Action"},
            {"title": "Film C", "genre": "Action"}
        ])

    def test_drama_genre(self):
        movies = [
            {"title": "Film A", "genre": "Action"},
            {"title": "Film B", "genre": "Drama"},
            {"title": "Film C", "genre": "Action"},
            {"title": "Film D", "genre": "Comedy"}
        ]
        self.assertEqual(filter_genres(movies, "Drama"), [
            {"title": "Film B", "genre": "Drama"}
        ])

    def test_comedy_genre(self):
        movies = [
            {"title": "Film A", "genre": "Action"},
            {"title": "Film B", "genre": "Drama"},
            {"title": "Film C", "genre": "Action"},
            {"title": "Film D", "genre": "Comedy"}
        ]
        self.assertEqual(filter_genres(movies, "Comedy"), [
            {"title": "Film D", "genre": "Comedy"}
        ])

    def test_empty_result(self):
        movies = [
            {"title": "Film A", "genre": "Action"},
            {"title": "Film B", "genre": "Drama"},
            {"title": "Film C", "genre": "Action"},
            {"title": "Film D", "genre": "Comedy"}
        ]
        self.assertEqual(filter_genres(movies, "Horror"), [])

    def test_empty_movie_list(self):
        movies = []
        self.assertEqual(filter_genres(movies, "Action"), [])

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 609
