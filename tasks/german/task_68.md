# Input
- Programmierkonzept: Rekursion
- Kontext: Musik

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rekursive Musiknoten

Schreibe eine Funktion namens `spiele_notenfolge(notenfolge)`, die eine Liste von Musiknoten (als Strings) rekursiv durchläuft und jede Note in der Konsole ausgibt. Die Funktion soll die Noten in der Reihenfolge ausgeben, in der sie in der Liste erscheinen.

Beispielaufruf:
```python
spiele_notenfolge(["C", "D", "E", "F", "G"])
```

Ausgabe:
```
C
D
E
F
G
```

Implementiere die Funktion so, dass sie rekursiv arbeitet.

## Codegerüst
```python
def spiele_notenfolge(notenfolge):
    ## Hier Code einfügen
```

## Musterlösung
```python
def spiele_notenfolge(notenfolge):
    if not notenfolge:
        return
    print(notenfolge[0])
    spiele_notenfolge(notenfolge[1:])

spiele_notenfolge(["C", "D", "E", "F", "G"])
```

## Unit Tests
```python
import unittest
from unittest.mock import patch
from main import spiele_notenfolge

class TestSpieleNotenfolge(unittest.TestCase):
    @patch('builtins.print')
    def test_einfache_notenfolge(self, mock_print):
        spiele_notenfolge(["C", "D", "E", "F", "G"])
        mock_print.assert_has_calls([unittest.mock.call("C"), unittest.mock.call("D"), unittest.mock.call("E"), unittest.mock.call("F"), unittest.mock.call("G")])

    @patch('builtins.print')
    def test_leere_notenfolge(self, mock_print):
        spiele_notenfolge([])
        mock_print.assert_not_called()

    @patch('builtins.print')
    def test_eine_note(self, mock_print):
        spiele_notenfolge(["A"])
        mock_print.assert_called_once_with("A")

    @patch('builtins.print')
    def test_verschachtelte_notenfolge(self, mock_print):
        spiele_notenfolge(["A", "B", "C", "D", "E"])
        mock_print.assert_has_calls([unittest.mock.call("A"), unittest.mock.call("B"), unittest.mock.call("C"), unittest.mock.call("D"), unittest.mock.call("E")])

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 486
