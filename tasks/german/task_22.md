# Input
- Programmierkonzept: Rekursion
- Kontext: Virtuelle Realität

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Berechnung der VR-Welten

In der virtuellen Realität (VR) können Welten ineinander verschachtelt sein, ähnlich wie bei einem Fraktal. Jede VR-Welt kann eine bestimmte Anzahl von Unterwelten enthalten, und jede dieser Unterwelten kann wiederum weitere Unterwelten enthalten.

Schreibe eine rekursive Funktion `anzahl_unterwelten(welt)`, die die Gesamtanzahl der Unterwelten in einer gegebenen VR-Welt berechnet. Die VR-Welt wird als ein Dictionary dargestellt, wobei der Schlüssel `"unterwelten"` eine Liste von weiteren VR-Welten (ebenfalls Dictionaries) enthält.

Beispiel:

```python
vr_welt = {
    "name": "Hauptwelt",
    "unterwelten": [
        {
            "name": "Unterwelt 1",
            "unterwelten": []
        },
        {
            "name": "Unterwelt 2",
            "unterwelten": [
                {
                    "name": "Unterwelt 2.1",
                    "unterwelten": []
                }
            ]
        }
    ]
}
```

In diesem Beispiel hat die Hauptwelt zwei direkte Unterwelten und eine weitere Unterwelt in der zweiten Unterwelt, also insgesamt drei Unterwelten.

Implementiere die Funktion `anzahl_unterwelten(welt)`, die die Gesamtanzahl der Unterwelten in der gegebenen VR-Welt berechnet und zurückgibt.

Beispielaufruf:

```python
print(anzahl_unterwelten(vr_welt))  # Ausgabe: 3
```

## Codegerüst
```python
def anzahl_unterwelten(welt):
    ## Hier Code einfügen
```

## Musterlösung
```python
def anzahl_unterwelten(welt):
    return len(welt["unterwelten"]) + sum(anzahl_unterwelten(uw) for uw in welt["unterwelten"])

vr_welt = {
    "name": "Hauptwelt",
    "unterwelten": [
        {
            "name": "Unterwelt 1",
            "unterwelten": []
        },
        {
            "name": "Unterwelt 2",
            "unterwelten": [
                {
                    "name": "Unterwelt 2.1",
                    "unterwelten": []
                }
            ]
        }
    ]
}

print(anzahl_unterwelten(vr_welt))  # Ausgabe: 3
```

## Unit Tests
```python
import unittest
from main import anzahl_unterwelten

class TestAnzahlUnterwelten(unittest.TestCase):
    def test_einfache_welt(self):
        welt = {
            "name": "Hauptwelt",
            "unterwelten": []
        }
        self.assertEqual(anzahl_unterwelten(welt), 0)

    def test_welt_mit_einer_unterwelt(self):
        welt = {
            "name": "Hauptwelt",
            "unterwelten": [
                {
                    "name": "Unterwelt 1",
                    "unterwelten": []
                }
            ]
        }
        self.assertEqual(anzahl_unterwelten(welt), 1)

    def test_welt_mit_mehreren_unterwelten(self):
        welt = {
            "name": "Hauptwelt",
            "unterwelten": [
                {
                    "name": "Unterwelt 1",
                    "unterwelten": []
                },
                {
                    "name": "Unterwelt 2",
                    "unterwelten": [
                        {
                            "name": "Unterwelt 2.1",
                            "unterwelten": []
                        }
                    ]
                }
            ]
        }
        self.assertEqual(anzahl_unterwelten(welt), 3)

    def test_tief_verschachtelte_welt(self):
        welt = {
            "name": "Hauptwelt",
            "unterwelten": [
                {
                    "name": "Unterwelt 1",
                    "unterwelten": [
                        {
                            "name": "Unterwelt 1.1",
                            "unterwelten": [
                                {
                                    "name": "Unterwelt 1.1.1",
                                    "unterwelten": []
                                }
                            ]
                        }
                    ]
                }
            ]
        }
        self.assertEqual(anzahl_unterwelten(welt), 3)

    def test_leere_welt(self):
        welt = {}
        self.assertEqual(anzahl_unterwelten(welt), 0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 440
