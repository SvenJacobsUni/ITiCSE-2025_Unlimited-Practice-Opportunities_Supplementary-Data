# Input
- Programming Concept: Higher-order functions; String
- Context: Virtual Reality

# Generated Task Components
## Task Description
### Exercise: Higher-order Functions and Strings in Virtual Reality

In virtual reality (VR), it's essential that objects and environments are correctly named and categorized. Write a function `filter_vr_objects(objects, criteria)` that receives a list of VR objects and a filter function as parameters. The function should return a new list containing only the objects that meet the criteria of the filter function.

The VR objects are stored as strings in the list `objects`. The `criteria` function is a higher-order function that takes a string as an argument and returns a boolean value.

Example call:
```python
def is_environment(obj):
 return "Environment" in obj

vr_objects = ["Environment_Forest", "Object_Tree", "Environment_Desert", "Object_Rock"]
filtered_objects = filter_vr_objects(vr_objects, is_environment)
print(filtered_objects)  # Output: ["Environment_Forest", "Environment_Desert"]
```

Implement the function `filter_vr_objects(objects, criteria)`.

## Code Framework
```python
def filter_vr_objects(objects, criteria):
    ## Insert code here
```

## Model Solution
```python
def filter_vr_objects(objects, criteria):
    return [obj for obj in objects if criteria(obj)]

def is_environment(obj):
    return "Environment" in obj

vr_objects = ["Environment_Forest", "Object_Tree", "Environment_Desert", "Object_Rock"]
filtered_objects = filter_vr_objects(vr_objects, is_environment)
print(filtered_objects)  # Output: ["Environment_Forest", "Environment_Desert"]
```

## Unit Tests
```python
import unittest

from main import filter_vr_objects

class TestFilterVrObjects(unittest.TestCase):
    def test_filter_environments(self):
        def is_environment(obj):
            return "Environment" in obj
        vr_objects = ["Environment_Forest", "Object_Tree", "Environment_Desert", "Object_Rock"]
        self.assertEqual(filter_vr_objects(vr_objects, is_environment), ["Environment_Forest", "Environment_Desert"])

    def test_filter_objects(self):
        def is_object(obj):
            return "Object" in obj
        vr_objects = ["Environment_Forest", "Object_Tree", "Environment_Desert", "Object_Rock"]
        self.assertEqual(filter_vr_objects(vr_objects, is_object), ["Object_Tree", "Object_Rock"])

    def test_empty_list(self):
        def is_environment(obj):
            return "Environment" in obj
        vr_objects = []
        self.assertEqual(filter_vr_objects(vr_objects, is_environment), [])

    def test_no_match(self):
        def is_water(obj):
            return "Water" in obj
        vr_objects = ["Environment_Forest", "Object_Tree", "Environment_Desert", "Object_Rock"]
        self.assertEqual(filter_vr_objects(vr_objects, is_water), [])

    def test_all_match(self):
        def is_any(obj):
            return True
        vr_objects = ["Environment_Forest", "Object_Tree", "Environment_Desert", "Object_Rock"]
        self.assertEqual(filter_vr_objects(vr_objects, is_any), vr_objects)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 572
