# Input
- Programmierkonzept: Operationen mit Zahlen;For-Schleifen
- Kontext: Sport

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Durchschnittliche Laufzeit berechnen

Schreibe eine Funktion namens `durchschnittliche_laufzeit(zeiten)`, die eine Liste von Laufzeiten (in Minuten) als Argument erhält und die durchschnittliche Laufzeit berechnet und zurückgibt. Die Berechnung soll unter Verwendung einer For-Schleife erfolgen.

Beispielaufruf:
```python
zeiten = [30, 45, 50, 40, 35]
print(durchschnittliche_laufzeit(zeiten))  # Ausgabe: 40.0
```

In diesem Beispiel sind die Laufzeiten von fünf Läufern in Minuten angegeben. Die Funktion soll die durchschnittliche Laufzeit berechnen und zurückgeben.

## Codegerüst
```python
def durchschnittliche_laufzeit(zeiten):
    ## Hier Code einfügen
```

## Musterlösung
```python
def durchschnittliche_laufzeit(zeiten):
    summe = 0
    for zeit in zeiten:
        summe += zeit
    return summe / len(zeiten)

zeiten = [30, 45, 50, 40, 35]
print(durchschnittliche_laufzeit(zeiten))
```

## Unit Tests
```python
import unittest
from main import durchschnittliche_laufzeit

class TestDurchschnittlicheLaufzeit(unittest.TestCase):
    def test_einfache_liste(self):
        self.assertEqual(durchschnittliche_laufzeit([30, 45, 50, 40, 35]), 40.0)

    def test_leere_liste(self):
        with self.assertRaises(ZeroDivisionError):
            durchschnittliche_laufzeit([])

    def test_ein_element(self):
        self.assertEqual(durchschnittliche_laufzeit([25]), 25.0)

    def test_gemischte_werte(self):
        self.assertEqual(durchschnittliche_laufzeit([10, 20, 30, 40, 50]), 30.0)

    def test_gleiche_werte(self):
        self.assertEqual(durchschnittliche_laufzeit([20, 20, 20, 20, 20]), 20.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 534
