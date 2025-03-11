# Input
- Programming Concept: While loops;String;Tuple
- Context: Film

# Generated Task Components
## Task Description
### Exercise: Counting Film Quotes

Write a function named `count_quotes(movie_quotes)` that receives a list of movie quotes as tuples. Each tuple contains the name of the movie and the quote. The function should count the number of quotes for each movie and return the result as a dictionary. Use a While loop to iterate through the list of film quotes.

#### Example:
```python
movie_quotes = [
    ("The Godfather", "I'm going to make him an offer he can't refuse."),
    ("Star Wars", "May the Force be with you."),
    ("The Godfather", "Leave the gun. Take the cannoli."),
    ("Star Wars", "I am your father."),
    ("The Godfather", "It was Barzini all along."),
]

result = count_quotes(movie_quotes)
print(result)  # Output: {'The Godfather': 3, 'Star Wars': 2}
```

Implement the function `count_quotes(movie_quotes)` that behaves as described above.

## Code Framework
```python
def count_quotes(movie_quotes):
    ## Insert code here
```

## Model Solution
```python
def count_quotes(movie_quotes):
    result = {}
    i = 0
    while i < len(movie_quotes):
        movie, _ = movie_quotes[i]
        if movie in result:
            result[movie] += 1
        else:
            result[movie] = 1
        i += 1
    return result

movie_quotes = [
    ("The Godfather", "I'm going to make him an offer he can't refuse."),
    ("Star Wars", "May the Force be with you."),
    ("The Godfather", "Leave the gun. Take the cannoli."),
    ("Star Wars", "I am your father."),
    ("The Godfather", "It was Barzini all along."),
]

result = count_quotes(movie_quotes)
print(result)  # Output: {'The Godfather': 3, 'Star Wars': 2}
```

## Unit Tests
```python
import unittest

from main import count_quotes

class TestCountQuotes(unittest.TestCase):
    def test_multiple_movies(self):
        movie_quotes = [
            ("The Godfather", "I'm going to make him an offer he can't refuse."),
            ("Star Wars", "May the Force be with you."),
            ("The Godfather", "Leave the gun. Take the cannoli."),
            ("Star Wars", "I am your father."),
            ("The Godfather", "It was Barzini all along."),
        ]
        self.assertEqual(count_quotes(movie_quotes), {'The Godfather': 3, 'Star Wars': 2})

    def test_one_movie(self):
        movie_quotes = [
            ("Inception", "You have to go deeper."),
            ("Inception", "An idea is like a virus."),
        ]
        self.assertEqual(count_quotes(movie_quotes), {'Inception': 2})

    def test_no_quotes(self):
        movie_quotes = []
        self.assertEqual(count_quotes(movie_quotes), {})

    def test_one_quote(self):
        movie_quotes = [("Matrix", "There is no spoon.")]
        self.assertEqual(count_quotes(movie_quotes), {'Matrix': 1})

    def test_various_movies(self):
        movie_quotes = [
            ("Matrix", "There is no spoon."),
            ("Inception", "You have to go deeper."),
            ("Star Wars", "May the Force be with you."),
        ]
        self.assertEqual(count_quotes(movie_quotes), {'Matrix': 1, 'Inception': 1, 'Star Wars': 1})

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 631
