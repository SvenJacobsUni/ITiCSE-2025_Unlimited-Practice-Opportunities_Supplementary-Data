# Input
- Programming Concept: Lists;String
- Context: Streaming Services

# Generated Task Components
## Task Description
### Exercise: Popular Series on Streaming Services

Write a function called `popular_series(streaming_service)` that returns a list of series available on the specified streaming service. The function should take a list of strings as input, where each string represents the name of a streaming service. The function should return a list of series names available on the specified streaming service.

Use the following data:

- Netflix: ["Stranger Things", "The Crown", "Black Mirror"]
- Amazon Prime: ["The Boys", "The Marvelous Mrs. Maisel", "Fleabag"]
- Disney+: ["The Mandalorian", "WandaVision", "Loki"]

Example call:
```python
popular_series("Netflix")
```
should return the list `["Stranger Things", "The Crown", "Black Mirror"]`.

## Code Framework
```python
def popular_series(streaming_service):
    ## Insert code here
```

## Model Solution
```python
def popular_series(streaming_service):
    series = {
        "Netflix": ["Stranger Things", "The Crown", "Black Mirror"],
        "Amazon Prime": ["The Boys", "The Marvelous Mrs. Maisel", "Fleabag"],
        "Disney+": ["The Mandalorian", "WandaVision", "Loki"]
    }
    return series.get(streaming_service, [])

# Example call
print(popular_series("Netflix"))
```

## Unit Tests
```python
import unittest
from main import popular_series

class TestPopularSeries(unittest.TestCase):
    def test_netflix(self):
        self.assertEqual(popular_series("Netflix"), ["Stranger Things", "The Crown", "Black Mirror"])

    def test_amazon_prime(self):
        self.assertEqual(popular_series("Amazon Prime"), ["The Boys", "The Marvelous Mrs. Maisel", "Fleabag"])

    def test_disney_plus(self):
        self.assertEqual(popular_series("Disney+"), ["The Mandalorian", "WandaVision", "Loki"])

    def test_unknown_service(self):
        self.assertEqual(popular_series("Hulu"), [])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 567
