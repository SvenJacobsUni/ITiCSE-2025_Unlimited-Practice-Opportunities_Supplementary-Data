# Input
- Programmierkonzept: String;Operationen mit Zahlen
- Kontext: Olympia

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Olympia-Medaillenspiegel

Schreibe eine Funktion namens `medaillenspiegel(land, gold, silber, bronze)`, die die Anzahl der gewonnenen Medaillen eines Landes bei den Olympischen Spielen berechnet und eine entsprechende Nachricht zurückgibt.

Die Funktion soll folgende Parameter haben:
- `land` (String): Der Name des Landes.
- `gold` (int): Die Anzahl der gewonnenen Goldmedaillen.
- `silber` (int): Die Anzahl der gewonnenen Silbermedaillen.
- `bronze` (int): Die Anzahl der gewonnenen Bronzemedaillen.

Die Funktion soll die Gesamtzahl der Medaillen berechnen und eine Nachricht im folgenden Format zurückgeben:
```
[Land] hat insgesamt [Gesamtzahl] Medaillen gewonnen: [Gold] Gold, [Silber] Silber, [Bronze] Bronze.
```

Beispielaufruf:
```python
print(medaillenspiegel("Deutschland", 10, 5, 7))
```

Beispielausgabe:
```
Deutschland hat insgesamt 22 Medaillen gewonnen: 10 Gold, 5 Silber, 7 Bronze.
```

## Codegerüst
```python
def medaillenspiegel(land, gold, silber, bronze):
    ## Hier Code einfügen
```

## Musterlösung
```python
def medaillenspiegel(land, gold, silber, bronze):
    gesamt = gold + silber + bronze
    return f"{land} hat insgesamt {gesamt} Medaillen gewonnen: {gold} Gold, {silber} Silber, {bronze} Bronze."

print(medaillenspiegel("Deutschland", 10, 5, 7))
```

## Unit Tests
```python
import unittest
from main import medaillenspiegel

class TestMedaillenspiegel(unittest.TestCase):
    def test_deutschland(self):
        self.assertEqual(medaillenspiegel("Deutschland", 10, 5, 7), "Deutschland hat insgesamt 22 Medaillen gewonnen: 10 Gold, 5 Silber, 7 Bronze.")

    def test_usa(self):
        self.assertEqual(medaillenspiegel("USA", 15, 10, 5), "USA hat insgesamt 30 Medaillen gewonnen: 15 Gold, 10 Silber, 5 Bronze.")

    def test_china(self):
        self.assertEqual(medaillenspiegel("China", 8, 12, 6), "China hat insgesamt 26 Medaillen gewonnen: 8 Gold, 12 Silber, 6 Bronze.")

    def test_null_medaillen(self):
        self.assertEqual(medaillenspiegel("Niemandsland", 0, 0, 0), "Niemandsland hat insgesamt 0 Medaillen gewonnen: 0 Gold, 0 Silber, 0 Bronze.")

    def test_randfall(self):
        self.assertEqual(medaillenspiegel("Testland", 1, 0, 0), "Testland hat insgesamt 1 Medaille gewonnen: 1 Gold, 0 Silber, 0 Bronze.")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 581
