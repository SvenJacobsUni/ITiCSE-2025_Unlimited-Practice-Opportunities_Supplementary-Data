# Input
- Programming Concept: Higher-order functions
- Context: Streaming Services

# Generated Task Components
## Task Description
### Exercise: Higher-order Functions in the Context of Streaming Services

Write a function `filter_movies(movies, criterion)`, which takes a list of movies and a function as a criterion. The function should return a new list that contains only the movies that meet the criterion.

A movie is represented by a dictionary that contains at least the keys `title` and `rating`. The function `criterion` takes a movie dictionary as an argument and returns a Boolean value.

Example call:
```python
movies = [
    {"title": "Film A", "rating": 8.5},
    {"title": "Film B", "rating": 7.0},
    {"title": "Film C", "rating": 9.0}
]

def high_rating(movie):
    return movie["rating"] > 8.0

filtered_movies = filter_movies(movies, high_rating)
# filtered_movies should contain [{"title": "Film A", "rating": 8.5}, {"title": "Film C", "rating": 9.0}]
```

Implement the function `filter_movies(movies, criterion)`.

## Code Framework
```python
def filter_movies(movies, criterion):
    ## Insert code here
```

## Model Solution
```python
def filter_movies(movies, criterion):
    return [movie for movie in movies if criterion(movie)]

movies = [
    {"title": "Film A", "rating": 8.5},
    {"title": "Film B", "rating": 7.0},
    {"title": "Film C", "rating": 9.0}
]

def high_rating(movie):
    return movie["rating"] > 8.0

filtered_movies = filter_movies(movies, high_rating)
print(filtered_movies)
```

## Unit Tests
```python
import unittest

class TestFilterMovies(unittest.TestCase):
    def test_high_rating(self):
        movies = [
            {"title": "Film A", "rating": 8.5},
            {"title": "Film B", "rating": 7.0},
            {"title": "Film C", "rating": 9.0}
        ]
        def high_rating(movie):
            return movie["rating"] > 8.0
        self.assertEqual(filter_movies(movies, high_rating), [
            {"title": "Film A", "rating": 8.5},
            {"title": "Film C", "rating": 9.0}
        ])

    def test_low_rating(self):
        movies = [
            {"title": "Film A", "rating": 8.5},
            {"title": "Film B", "rating": 7.0},
            {"title": "Film C", "rating": 9.0}
        ]
        def low_rating(movie):
            return movie["rating"] < 8.0
        self.assertEqual(filter_movies(movies, low_rating), [
            {"title": "Film B", "rating": 7.0}
        ])

    def test_empty_list(self):
        movies = []
        def high_rating(movie):
            return movie["rating"] > 8.0
        self.assertEqual(filter_movies(movies, high_rating), [])

    def test_all_movies(self):
        movies = [
            {"title": "Film A", "rating": 8.5},
            {"title": "Film B", "rating": 7.0},
            {"title": "Film C", "rating": 9.0}
        ]
        def all_movies(movie):
            return True
        self.assertEqual(filter_movies(movies, all_movies), movies)

    def test_no_movies(self):
        movies = [
            {"title": "Film A", "rating": 8.5},
            {"title": "Film B", "rating": 7.0},
            {"title": "Film C", "rating": 9.0}
        ]
        def no_movies(movie):
            return False
        self.assertEqual(filter_movies(movies, no_movies), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 427
