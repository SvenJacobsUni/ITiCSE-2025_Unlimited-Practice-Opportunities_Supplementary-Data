# Input
- Programming Concept: Lists;While loops;Functions as variables
- Context: Streaming Services

# Generated Task Components
## Task Description
### Exercise Task: Streaming Services and Series

Write a function `filter_series(series_list, rating)`, which receives a list of series and a minimum rating as parameters. The function should return all series from the list that have a rating equal to or higher than the specified minimum rating.

The series list is a list of tuples, where each tuple contains the name of the series and its rating. The rating is a number between 1 and 10.

Use a `while` loop to iterate through the list and filter the series.

Example:

```python
series = ["Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9), ("Friends", 8.0)]
print(filter_series(series, 8.5))
```

Expected Output:

```
[('Breaking Bad', 9.5), ('Stranger Things', 8.7), ('The Office', 8.9)]
```


## Code Framework
```python
def filter_series(series_list, rating):
    ## Insert code here

```

## Model Solution
```python
def filter_series(series_list, rating):
    result = []
    i = 0
    while i < len(series_list):
        if series_list[i][1] >= rating:
            result.append(series_list[i])
        i += 1
    return result

series = [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9), ("Friends", 8.0)]
print(filter_series(series, 8.5))

```

## Unit Tests
```python
import unittest
from main import filter_series

class TestFilterSeries(unittest.TestCase):
    def test_all_series(self):
        series = [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9), ("Friends", 8.0)]
        self.assertEqual(filter_series(series, 8.0), series)

    def test_no_series(self):
        series = [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9), ("Friends", 8.0)]
        self.assertEqual(filter_series(series, 10.0), [])

    def test_some_series(self):
        series = [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9), ("Friends", 8.0)]
        self.assertEqual(filter_series(series, 8.5), [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9)])

    def test_empty_list(self):
        series = []
        self.assertEqual(filter_series(series, 8.5), [])

    def test_boundary_rating(self):
        series = [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9), ("Friends", 8.0)]
        self.assertEqual(filter_series(series, 8.7), [("Breaking Bad", 9.5), ("Stranger Things", 8.7), ("The Office", 8.9)])

if __name__ == '__main__':
    unittest.main()

```
___
# Metadata
Database ID: 602
