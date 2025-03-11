# Input
- Programming Concept: Integer;For loops;Higher-order functions
- Context: Streaming Services

# Generated Task Components
## Task Description
### Exercise: Most Popular Movies on Streaming Services

Write a function named `most_popular_movies(movies, ratings)` that receives a list of movies and a list of ratings as arguments. Each movie in the list `movies` has a corresponding rating in the list `ratings` at the same position. The function should return the movies that have a rating of 8 or higher.

Use a for loop to iterate through the lists and a higher-order function to return the filtered movies.

Example call:
```python
movies = ["Movie A", "Movie B", "Movie C", "Movie D"]
ratings = [7, 9, 8, 6]
print(most_popular_movies(movies, ratings))
```

Expected output:
```
["Movie B", "Movie C"]
```

## Code Framework
```python
def most_popular_movies(movies, ratings):
    ## Insert code here
```

## Model Solution
```python
def most_popular_movies(movies, ratings):
    return [movie for movie, rating in zip(movies, ratings) if rating >= 8]

movies = ["Movie A", "Movie B", "Movie C", "Movie D"]
ratings = [7, 9, 8, 6]
print(most_popular_movies(movies, ratings))
```

## Unit Tests
```python
import unittest
from main import most_popular_movies

class TestMostPopularMovies(unittest.TestCase):
    def test_all_movies_popular(self):
        movies = ["Movie A", "Movie B", "Movie C"]
        ratings = [8, 9, 10]
        self.assertEqual(most_popular_movies(movies, ratings), ["Movie A", "Movie B", "Movie C"])

    def test_no_movies_popular(self):
        movies = ["Movie A", "Movie B", "Movie C"]
        ratings = [7, 6, 5]
        self.assertEqual(most_popular_movies(movies, ratings), [])

    def test_mixed_ratings(self):
        movies = ["Movie A", "Movie B", "Movie C", "Movie D"]
        ratings = [7, 9, 8, 6]
        self.assertEqual(most_popular_movies(movies, ratings), ["Movie B", "Movie C"])

    def test_empty_list(self):
        movies = []
        ratings = []
        self.assertEqual(most_popular_movies(movies, ratings), [])

    def test_boundary_rating(self):
        movies = ["Movie A", "Movie B", "Movie C"]
        ratings = [8, 7, 8]
        self.assertEqual(most_popular_movies(movies, ratings), ["Movie A", "Movie C"])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 598
