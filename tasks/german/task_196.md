# Input
- Programmierkonzept: Operationen mit Zahlen;Rekursion;Float
- Kontext: Rugby

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Rugby-Punktestand berechnen

In einem Rugby-Spiel können Punkte auf verschiedene Arten erzielt werden: 
- Ein Versuch (Try) bringt 5 Punkte.
- Eine Erhöhung (Conversion) bringt 2 Punkte.
- Ein Straftritt (Penalty) oder ein Dropgoal bringt jeweils 3 Punkte.

Schreibe eine Funktion `berechne_punkte(versuche, erhoehungen, straftritte, dropgoals)`, die die Gesamtpunktzahl eines Rugby-Teams berechnet. Die Funktion soll die Anzahl der Versuche, Erhöhungen, Straftritte und Dropgoals als Argumente entgegennehmen und die Gesamtpunktzahl als `float` zurückgeben.

Beispielaufruf:
```python
punkte = berechne_punkte(3, 2, 1, 1)
print(punkte)  # Ausgabe: 22.0
```

### Erweiterung: Rekursive Berechnung

Erweitere die Funktion `berechne_punkte_rekursiv(versuche, erhoehungen, straftritte, dropgoals)`, die die gleiche Funktionalität wie `berechne_punkte` hat, aber die Berechnung der Gesamtpunktzahl rekursiv durchführt.

Beispielaufruf:
```python
punkte = berechne_punkte_rekursiv(3, 2, 1, 1)
print(punkte)  # Ausgabe: 22.0
```

## Codegerüst
```python
def berechne_punkte(versuche, erhoehungen, straftritte, dropgoals):
    ## Hier Code einfügen

def berechne_punkte_rekursiv(versuche, erhoehungen, straftritte, dropgoals):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_punkte(versuche, erhoehungen, straftritte, dropgoals):
    return versuche * 5 + erhoehungen * 2 + straftritte * 3 + dropgoals * 3

def berechne_punkte_rekursiv(versuche, erhoehungen, straftritte, dropgoals):
    if versuche == 0 and erhoehungen == 0 and straftritte == 0 and dropgoals == 0:
        return 0
    if versuche > 0:
        return 5 + berechne_punkte_rekursiv(versuche - 1, erhoehungen, straftritte, dropgoals)
    if erhoehungen > 0:
        return 2 + berechne_punkte_rekursiv(versuche, erhoehungen - 1, straftritte, dropgoals)
    if straftritte > 0:
        return 3 + berechne_punkte_rekursiv(versuche, erhoehungen, straftritte - 1, dropgoals)
    if dropgoals > 0:
        return 3 + berechne_punkte_rekursiv(versuche, erhoehungen, straftritte, dropgoals - 1)

punkte = berechne_punkte(3, 2, 1, 1)
print(punkte)  # Ausgabe: 22.0

punkte_rekursiv = berechne_punkte_rekursiv(3, 2, 1, 1)
print(punkte_rekursiv)  # Ausgabe: 22.0
```

## Unit Tests
```python
import unittest
from main import berechne_punkte, berechne_punkte_rekursiv

class TestBerechnePunkte(unittest.TestCase):
    def test_alle_null(self):
        self.assertEqual(berechne_punkte(0, 0, 0, 0), 0.0)
    
    def test_nur_versuche(self):
        self.assertEqual(berechne_punkte(3, 0, 0, 0), 15.0)
    
    def test_nur_erhoehungen(self):
        self.assertEqual(berechne_punkte(0, 2, 0, 0), 4.0)
    
    def test_nur_straftritte(self):
        self.assertEqual(berechne_punkte(0, 0, 1, 0), 3.0)
    
    def test_nur_dropgoals(self):
        self.assertEqual(berechne_punkte(0, 0, 0, 1), 3.0)
    
    def test_gemischt(self):
        self.assertEqual(berechne_punkte(3, 2, 1, 1), 22.0)

class TestBerechnePunkteRekursiv(unittest.TestCase):
    def test_alle_null(self):
        self.assertEqual(berechne_punkte_rekursiv(0, 0, 0, 0), 0.0)
    
    def test_nur_versuche(self):
        self.assertEqual(berechne_punkte_rekursiv(3, 0, 0, 0), 15.0)
    
    def test_nur_erhoehungen(self):
        self.assertEqual(berechne_punkte_rekursiv(0, 2, 0, 0), 4.0)
    
    def test_nur_straftritte(self):
        self.assertEqual(berechne_punkte_rekursiv(0, 0, 1, 0), 3.0)
    
    def test_nur_dropgoals(self):
        self.assertEqual(berechne_punkte_rekursiv(0, 0, 0, 1), 3.0)
    
    def test_gemischt(self):
        self.assertEqual(berechne_punkte_rekursiv(3, 2, 1, 1), 22.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 628
