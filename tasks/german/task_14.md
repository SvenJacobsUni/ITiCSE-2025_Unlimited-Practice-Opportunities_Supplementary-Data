# Input
- Programmierkonzept: Funktionen höherer Ordnung
- Kontext: Psychische Gesundheit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen höherer Ordnung im Kontext psychischer Gesundheit

Schreibe eine Funktion `filter_positive_affirmations(affirmations, filter_function)`, die eine Liste von Affirmationen (positive Aussagen) und eine Filterfunktion als Argumente erhält. Die Funktion soll die Affirmationen basierend auf der übergebenen Filterfunktion filtern und die gefilterte Liste zurückgeben.

Beispielaufruf:
```python
affirmations = [
    "Ich bin stark.",
    "Ich bin wertvoll.",
    "Ich kann alles schaffen.",
    "Ich bin geliebt.",
    "Ich bin genug."
]

def contains_word_ich(affirmation):
    return "Ich" in affirmation

positive_affirmations = filter_positive_affirmations(affirmations, contains_word_ich)
print(positive_affirmations)
```

Erwartete Ausgabe:
```
["Ich bin stark.", "Ich bin wertvoll.", "Ich kann alles schaffen.", "Ich bin geliebt.", "Ich bin genug."]
```

Implementiere die Funktion `filter_positive_affirmations` und teste sie mit verschiedenen Filterfunktionen.

## Codegerüst
```python
def filter_positive_affirmations(affirmations, filter_function):
    ## Hier Code einfügen
```

## Musterlösung
```python
def filter_positive_affirmations(affirmations, filter_function):
    return list(filter(filter_function, affirmations))

affirmations = [
    "Ich bin stark.",
    "Ich bin wertvoll.",
    "Ich kann alles schaffen.",
    "Ich bin geliebt.",
    "Ich bin genug."
]

def contains_word_ich(affirmation):
    return "Ich" in affirmation

positive_affirmations = filter_positive_affirmations(affirmations, contains_word_ich)
print(positive_affirmations)
```

## Unit Tests
```python
import unittest
from main import filter_positive_affirmations

class TestFilterPositiveAffirmations(unittest.TestCase):
    def test_contains_word_ich(self):
        affirmations = [
            "Ich bin stark.",
            "Ich bin wertvoll.",
            "Ich kann alles schaffen.",
            "Ich bin geliebt.",
            "Ich bin genug."
        ]
        def contains_word_ich(affirmation):
            return "Ich" in affirmation
        expected = [
            "Ich bin stark.",
            "Ich bin wertvoll.",
            "Ich kann alles schaffen.",
            "Ich bin geliebt.",
            "Ich bin genug."
        ]
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_ich), expected)

    def test_contains_word_bin(self):
        affirmations = [
            "Ich bin stark.",
            "Ich bin wertvoll.",
            "Ich kann alles schaffen.",
            "Ich bin geliebt.",
            "Ich bin genug."
        ]
        def contains_word_bin(affirmation):
            return "bin" in affirmation
        expected = [
            "Ich bin stark.",
            "Ich bin wertvoll.",
            "Ich bin geliebt.",
            "Ich bin genug."
        ]
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_bin), expected)

    def test_no_match(self):
        affirmations = [
            "Ich bin stark.",
            "Ich bin wertvoll.",
            "Ich kann alles schaffen.",
            "Ich bin geliebt.",
            "Ich bin genug."
        ]
        def contains_word_xyz(affirmation):
            return "xyz" in affirmation
        expected = []
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_xyz), expected)

    def test_empty_list(self):
        affirmations = []
        def contains_word_ich(affirmation):
            return "Ich" in affirmation
        expected = []
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_ich), expected)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 432
