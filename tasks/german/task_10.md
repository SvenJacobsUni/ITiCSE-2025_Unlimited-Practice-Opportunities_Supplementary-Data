# Input
- Programmierkonzept: Funktionen als Variablen
- Kontext: Virtuelle Realität

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Funktionen als Variablen in der Virtuellen Realität

In der virtuellen Realität (VR) können verschiedene Aktionen durch Funktionen repräsentiert werden. Schreibe eine Funktion `ausfuehren_aktion(aktion)`, die eine Aktion als Parameter entgegennimmt und diese Aktion ausführt. Die Aktion wird durch eine Funktion repräsentiert, die keine Parameter hat und eine Nachricht zurückgibt.

Definiere zwei Beispielaktionen:
1. `start_vr()`: Gibt die Nachricht "VR gestartet!" zurück.
2. `beenden_vr()`: Gibt die Nachricht "VR beendet!" zurück.

Die Funktion `ausfuehren_aktion(aktion)` soll die übergebene Aktion ausführen und die entsprechende Nachricht zurückgeben.

Beispielaufrufe:
```python
print(ausfuehren_aktion(start_vr))  # Ausgabe: "VR gestartet!"
print(ausfuehren_aktion(beenden_vr))  # Ausgabe: "VR beendet!"
```

## Codegerüst
```python
def ausfuehren_aktion(aktion):
    ## Hier Code einfügen

def start_vr():
    ## Hier Code einfügen

def beenden_vr():
    ## Hier Code einfügen
```

## Musterlösung
```python
def ausfuehren_aktion(aktion):
    return aktion()

def start_vr():
    return "VR gestartet!"

def beenden_vr():
    return "VR beendet!"

print(ausfuehren_aktion(start_vr))
print(ausfuehren_aktion(beenden_vr))
```

## Unit Tests
```python
import unittest
from main import ausfuehren_aktion, start_vr, beenden_vr

class TestAusfuehrenAktion(unittest.TestCase):
    def test_start_vr(self):
        self.assertEqual(ausfuehren_aktion(start_vr), "VR gestartet!")

    def test_beenden_vr(self):
        self.assertEqual(ausfuehren_aktion(beenden_vr), "VR beendet!")

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 428
