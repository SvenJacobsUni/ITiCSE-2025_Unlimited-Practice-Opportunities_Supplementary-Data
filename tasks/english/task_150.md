# Input
- Programming Concept: Boolean and None;Recursion
- Context: Film

# Generated Task Components
## Task Description
### Exercise: Film recommendation based on ratings

Write a recursive function `recommend_film(films, rating)` that receives a list of films and a rating as parameters. Each film in the list is a dictionary with the keys `title` and `rating`. The function should return the first film whose rating is greater or equal to the given rating. If no such film is found, the function should return `None`.

Example calls:
```python
films = [
    {'title': 'Film A', 'rating': 7.5},
    {'title': 'Film B', 'rating': 8.0},
    {'title': 'Film C', 'rating': 6.0}
]
print(recommend_film(films, 7.0))  # Returns {'title': 'Film A', 'rating': 7.5}
print(recommend_film(films, 8.5))  # Returns None
```

Implement the function `recommend_film(films, rating)`.

## Code Framework
```python
def recommend_film(films, rating):
    ## Insert code here
```

## Model Solution
```python
def recommend_film(films, rating):
    if not films:
        return None
    if films[0]['rating'] >= rating:
        return films[0]
    return recommend_film(films[1:], rating)

films = [
    {'title': 'Film A', 'rating': 7.5},
    {'title': 'Film B', 'rating': 8.0},
    {'title': 'Film C', 'rating': 6.0}
]
print(recommend_film(films, 7.0))  # Returns {'title': 'Film A', 'rating': 7.5}
print(recommend_film(films, 8.5))  # Returns None
```

## Unit Tests
```python
import unittest

from main import recommend_film

class TestRecommendFilm(unittest.TestCase):
    def test_film_found(self):
        films = [
            {'title': 'Film A', 'rating': 7.5},
            {'title': 'Film B', 'rating': 8.0},
            {'title': 'Film C', 'rating': 6.0}
        ]
        self.assertEqual(recommend_film(films, 7.0), {'title': 'Film A', 'rating': 7.5})

    def test_no_film_found(self):
        films = [
            {'title': 'Film A', 'rating': 7.5},
            {'title': 'Film B', 'rating': 8.0},
            {'title': 'Film C', 'rating': 6.0}
        ]
        self.assertIsNone(recommend_film(films, 8.5))

    def test_empty_list(self):
        films = []
        self.assertIsNone(recommend_film(films, 7.0))

    def test_all_films_below_rating(self):
        films = [
            {'title': 'Film A', 'rating': 5.5},
            {'title': 'Film B', 'rating': 6.0},
            {'title': 'Film C', 'rating': 4.0}
        ]
        self.assertIsNone(recommend_film(films, 7.0))

    def test_first_film_found(self):
        films = [
            {'title': 'Film A', 'rating': 7.0},
            {'title': 'Film B', 'rating': 8.0},
            {'title': 'Film C', 'rating': 6.0}
        ]
        self.assertEqual(recommend_film(films, 7.0), {'title': 'Film A', 'rating': 7.0})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 582
