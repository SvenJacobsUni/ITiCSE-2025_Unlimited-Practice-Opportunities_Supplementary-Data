# Input
- Programming Concept: While loops
- Context: Film

# Generated Task Components
## Task Description
### Exercise Task: Film Watchlist

Write a function called `film_watchlist(movies)`, which takes a list of movies as an argument. The function should use a while loop to iterate through the list and print each movie. If the list is empty, the function should print "No movies in the watchlist.".

## Code Framework
```python
def film_watchlist(movies):
    ## Insert code here
```

## Model Solution
```python
def film_watchlist(movies):
    if not movies:
        print("No movies in the watchlist.")
    while movies:
        print(movies.pop(0))

film_watchlist(["Inception", "The Matrix", "Interstellar"])
film_watchlist([])
```

## Unit Tests
```python
import unittest
from io import StringIO
import sys
from main import film_watchlist

class TestFilmWatchlist(unittest.TestCase):
    def test_watchlist_with_movies(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        film_watchlist(["Inception", "The Matrix", "Interstellar"])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "Inception\nThe Matrix\nInterstellar")

    def test_empty_watchlist(self):
        captured_output = StringIO()
        sys.stdout = captured_output
        film_watchlist([])
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue().strip(), "No movies in the watchlist.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 420
