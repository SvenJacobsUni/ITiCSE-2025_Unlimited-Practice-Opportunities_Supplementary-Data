# Input
- Programmierkonzept: Funktionen höherer Ordnung;String
- Kontext: Virtuelle Realität

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen höherer Ordnung und Strings in der Virtuellen Realität

In der virtuellen Realität (VR) ist es wichtig, dass Objekte und Umgebungen korrekt benannt und kategorisiert werden. Schreibe eine Funktion `filter_vr_objects(objects, criteria)`, die eine Liste von VR-Objekten und eine Filterfunktion als Parameter erhält. Die Funktion soll eine neue Liste zurückgeben, die nur die Objekte enthält, die den Kriterien der Filterfunktion entsprechen.

Die VR-Objekte sind als Strings in der Liste `objects` gespeichert. Die `criteria`-Funktion ist eine Funktion höherer Ordnung, die einen String als Argument nimmt und einen Boolean-Wert zurückgibt.

Beispielaufruf:
```python
def is_environment(obj):
    return "Environment" in obj

vr_objects = ["Environment_Forest", "Object_Tree", "Environment_Desert", "Object_Rock"]
filtered_objects = filter_vr_objects(vr_objects, is_environment)
print(filtered_objects)  # Ausgabe: ["Environment_Forest", "Environment_Desert"]
```

Implementiere die Funktion `filter_vr_objects(objects, criteria)`.

## Codegerüst
```python
def filter_vr_objects(objects, criteria):
    ## Hier Code einfügen
```

## Musterlösung
```python
def filter_vr_objects(objects, criteria):
    return [obj for obj in objects if criteria(obj)]

def is_environment(obj):
    return "Environment" in obj

vr_objects = ["Environment_Forest", "Object_Tree", "Environment_Desert", "Object_Rock"]
filtered_objects = filter_vr_objects(vr_objects, is_environment)
print(filtered_objects)  # Ausgabe: ["Environment_Forest", "Environment_Desert"]
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
