# Input
- Programming Concept: Float
- Context: Virtual Reality

# Generated Task Components
## Task Description
### Exercise: Calculating VR Render Time

In virtual reality (VR), it is important that the render time per frame is as low as possible to ensure smooth and realistic representation. The render time is often measured in milliseconds (ms).

Write a function named `calculate_render_time(frames, total_time)`, which calculates the average render time per frame. The function should take two parameters:
- `frames`: The number of rendered frames (integer value).
- `total_time`: The total render time in milliseconds (float value).

The function should return the average render time per frame as a float value.

Example call:
```python
average = calculate_render_time(240, 5000.0)
print(average)  # Expected output: 20.833333333333332
```

## Code Framework
```python
def calculate_render_time(frames, total_time):
    ## Insert code here
```

## Model Solution
```python
def calculate_render_time(frames, total_time):
    return total_time / frames

average = calculate_render_time(240, 5000.0)
print(average)
```

## Unit Tests
```python
import unittest

from main import calculate_render_time

class TestCalculateRenderTime(unittest.TestCase):
    def test_simple_case(self):
        self.assertAlmostEqual(calculate_render_time(240, 5000.0), 20.833333333333332)

    def test_zero_frames(self):
        with self.assertRaises(ZeroDivisionError):
            calculate_render_time(0, 5000.0)

    def test_zero_total_time(self):
        self.assertEqual(calculate_render_time(240, 0.0), 0.0)

    def test_one_frame(self):
        self.assertEqual(calculate_render_time(1, 5000.0), 5000.0)

    def test_large_values(self):
        self.assertAlmostEqual(calculate_render_time(1000000, 5000000.0), 5.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 461
