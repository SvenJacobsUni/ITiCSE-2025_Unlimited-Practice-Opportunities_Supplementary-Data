# Input
- Programming Concept: Recursion
- Context: Virtual Reality

# Generated Task Components
## Task Description
### Exercise: Recursive Calculation of VR Worlds

In virtual reality (VR), worlds can be nested within each other, similar to a fractal. Each VR world can contain a certain number of subworlds, and each of these subworlds can in turn contain more subworlds.

Write a recursive function `count_subworlds(world)`, which calculates the total number of subworlds in a given VR world. The VR world is represented as a dictionary, where the key "subworlds" contains a list of further VR worlds (also dictionaries).

Example:

```python
vr_world = {
    "name": "Main World",
    "subworlds": [
        {
            "name": "Subworld 1",
            "subworlds": []
        },
        {
            "name": "Subworld 2",
            "subworlds": [
                {
                    "name": "Subworld 2.1",
                    "subworlds": []
                }
            ]
        }
    ]
}
```

In this example, the main world has two direct subworlds and one further subworld in the second subworld, totaling three subworlds.

Implement the function `count_subworlds(world)`, which calculates and returns the total number of subworlds in the given VR world.

Example Call:

```python
print(count_subworlds(vr_world))  # Output: 3
```

## Code Framework
```python
def count_subworlds(world):
    ## Insert code here
```

## Model Solution
```python
def count_subworlds(world):
    return len(world["subworlds"]) + sum(count_subworlds(sw) for sw in world["subworlds"])

vr_world = {
    "name": "Main World",
    "subworlds": [
        {
            "name": "Subworld 1",
            "subworlds": []
        },
        {
            "name": "Subworld 2",
            "subworlds": [
                {
                    "name": "Subworld 2.1",
                    "subworlds": []
                }
            ]
        }
    ]
}

print(count_subworlds(vr_world))  # Output: 3
```

## Unit Tests
```python
import unittest
from main import count_subworlds

class TestCountSubworlds(unittest.TestCase):
    def test_simple_world(self):
        world = {
            "name": "Main World",
            "subworlds": []
        }
        self.assertEqual(count_subworlds(world), 0)

    def test_world_with_one_subworld(self):
        world = {
            "name": "Main World",
            "subworlds": [
                {
                    "name": "Subworld 1",
                    "subworlds": []
                }
            ]
        }
        self.assertEqual(count_subworlds(world), 1)

    def test_world_with_multiple_subworlds(self):
        world = {
            "name": "Main World",
            "subworlds": [
                {
                    "name": "Subworld 1",
                    "subworlds": []
                },
                {
                    "name": "Subworld 2",
                    "subworlds": [
                        {
                            "name": "Subworld 2.1",
                            "subworlds": []
                        }
                    ]
                }
            ]
        }
        self.assertEqual(count_subworlds(world), 3)

    def test_deeply_nested_world(self):
        world = {
            "name": "Main World",
            "subworlds": [
                {
                    "name": "Subworld 1",
                    "subworlds": [
                        {
                            "name": "Subworld 1.1",
                            "subworlds": [
                                {
                                    "name": "Subworld 1.1.1",
                                    "subworlds": []
                                }
                            ]
                        }
                    ]
                }
            ]
        }
        self.assertEqual(count_subworlds(world), 3)

    def test_empty_world(self):
        world = {}
        self.assertEqual(count_subworlds(world), 0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 440
