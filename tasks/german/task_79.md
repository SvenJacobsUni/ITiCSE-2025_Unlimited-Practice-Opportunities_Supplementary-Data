# Input
- Programmierkonzept: Funktionen höherer Ordnung
- Kontext: Psychische Gesundheit

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen höherer Ordnung im Kontext psychischer Gesundheit

Schreibe eine Funktion `filter_positive_affirmations(affirmations, filter_function)`, die eine Liste von positiven Affirmationen und eine Filterfunktion als Argumente erhält. Die Funktion soll die Affirmationen basierend auf der übergebenen Filterfunktion filtern und die gefilterte Liste zurückgeben.

Eine positive Affirmation ist ein kurzer, positiver Satz, der das Selbstwertgefühl und die psychische Gesundheit stärken soll. Beispiele für Affirmationen sind: "Ich bin stark", "Ich bin wertvoll", "Ich kann alles erreichen".

Beispielaufruf:
```python
affirmations = ["Ich bin stark", "Ich bin wertvoll", "Ich kann alles erreichen", "Ich bin genug"]
def contains_word_ich(affirmation):
    return "Ich" in affirmation

gefilterte_affirmationen = filter_positive_affirmations(affirmations, contains_word_ich)
print(gefilterte_affirmationen)  # Ausgabe: ["Ich bin stark", "Ich bin wertvoll", "Ich kann alles erreichen", "Ich bin genug"]
```

Implementiere die Funktion `filter_positive_affirmations` so, dass sie die Liste der Affirmationen basierend auf der übergebenen Filterfunktion korrekt filtert und zurückgibt.

## Codegerüst
```python
def filter_positive_affirmations(affirmations, filter_function):
    ## Hier Code einfügen
```

## Musterlösung
```python
def filter_positive_affirmations(affirmations, filter_function):
    return list(filter(filter_function, affirmations))

affirmations = ["Ich bin stark", "Ich bin wertvoll", "Ich kann alles erreichen", "Ich bin genug"]
def contains_word_ich(affirmation):
    return "Ich" in affirmation

gefilterte_affirmationen = filter_positive_affirmations(affirmations, contains_word_ich)
print(gefilterte_affirmationen)
```

## Unit Tests
```python
import unittest
from main import filter_positive_affirmations

class TestFilterPositiveAffirmations(unittest.TestCase):
    def test_contains_word_ich(self):
        affirmations = ["Ich bin stark", "Ich bin wertvoll", "Ich kann alles erreichen", "Ich bin genug"]
        def contains_word_ich(affirmation):
            return "Ich" in affirmation
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_ich), affirmations)

    def test_empty_list(self):
        affirmations = []
        def contains_word_ich(affirmation):
            return "Ich" in affirmation
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_ich), [])

    def test_no_match(self):
        affirmations = ["Du bist stark", "Du bist wertvoll", "Du kannst alles erreichen", "Du bist genug"]
        def contains_word_ich(affirmation):
            return "Ich" in affirmation
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_ich), [])

    def test_partial_match(self):
        affirmations = ["Ich bin stark", "Du bist wertvoll", "Ich kann alles erreichen", "Du bist genug"]
        def contains_word_ich(affirmation):
            return "Ich" in affirmation
        self.assertEqual(filter_positive_affirmations(affirmations, contains_word_ich), ["Ich bin stark", "Ich kann alles erreichen"])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 497
