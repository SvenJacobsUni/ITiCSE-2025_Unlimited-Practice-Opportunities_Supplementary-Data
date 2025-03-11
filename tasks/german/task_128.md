# Input
- Programmierkonzept: Boolean und None;For-Schleifen
- Kontext: Angeln

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Fische zählen

Schreibe eine Funktion namens `zaehle_fische(fische)`, die eine Liste von Fischen als Eingabe erhält. Jeder Eintrag in der Liste ist entweder der Name eines Fisches (als String) oder `None`, wenn kein Fisch gefangen wurde. Die Funktion soll die Anzahl der gefangenen Fische zählen und zurückgeben. 

Beispielaufruf:
```python
fische = ["Hecht", None, "Karpfen", "Forelle", None, "Barsch"]
print(zaehle_fische(fische))  # Ausgabe: 4
```

### Anforderungen:
- Die Funktion soll eine Liste von Fischen als Argument akzeptieren.
- Die Funktion soll die Anzahl der gefangenen Fische (nicht `None` Einträge) zählen und zurückgeben.
- Verwende eine `for`-Schleife, um durch die Liste zu iterieren.
- Nutze Boolean-Werte, um zu überprüfen, ob ein Eintrag `None` ist oder nicht.

## Codegerüst
```python
def zaehle_fische(fische):
    ## Hier Code einfügen
```

## Musterlösung
```python
def zaehle_fische(fische):
    return sum(1 for fisch in fische if fisch)

fische = ["Hecht", None, "Karpfen", "Forelle", None, "Barsch"]
print(zaehle_fische(fische))  # Ausgabe: 4
```

## Unit Tests
```python
import unittest

from main import zaehle_fische

class TestZaehleFische(unittest.TestCase):
    def test_einfache_liste(self):
        self.assertEqual(zaehle_fische(["Hecht", None, "Karpfen", "Forelle", None, "Barsch"]), 4)

    def test_leere_liste(self):
        self.assertEqual(zaehle_fische([]), 0)

    def test_alle_none(self):
        self.assertEqual(zaehle_fische([None, None, None]), 0)

    def test_alle_fische(self):
        self.assertEqual(zaehle_fische(["Hecht", "Karpfen", "Forelle", "Barsch"]), 4)

    def test_gemischte_liste(self):
        self.assertEqual(zaehle_fische([None, "Hecht", None, "Karpfen", "Forelle", None, "Barsch", None]), 4)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 560
