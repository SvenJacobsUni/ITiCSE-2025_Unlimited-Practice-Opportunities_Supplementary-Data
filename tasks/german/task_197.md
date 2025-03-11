# Input
- Programmierkonzept: Float;If-Else-Anweisungen;Funktionen höherer Ordnung
- Kontext: Soziale Medien

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Soziale Medien - Engagement Rate Berechnung

Schreibe eine Funktion namens `berechne_engagement_rate(likes, kommentare, follower)`, die die Engagement Rate eines Social Media Posts berechnet. Die Engagement Rate wird als Prozentsatz der Interaktionen (Likes und Kommentare) im Verhältnis zur Anzahl der Follower berechnet.

Die Funktion soll die folgenden Schritte ausführen:
1. Die Gesamtanzahl der Interaktionen berechnen (Likes + Kommentare).
2. Die Engagement Rate als Prozentsatz der Interaktionen im Verhältnis zur Anzahl der Follower berechnen.
3. Die Engagement Rate zurückgeben.

Zusätzlich soll die Funktion eine Nachricht ausgeben, die die Engagement Rate bewertet:
- Wenn die Engagement Rate größer oder gleich 10% ist, soll die Nachricht "Hohe Engagement Rate!" ausgegeben werden.
- Wenn die Engagement Rate zwischen 5% und 10% liegt, soll die Nachricht "Durchschnittliche Engagement Rate" ausgegeben werden.
- Wenn die Engagement Rate unter 5% liegt, soll die Nachricht "Niedrige Engagement Rate" ausgegeben werden.

Beispielaufruf:
```python
berechne_engagement_rate(150, 30, 2000)
```

Erwartete Ausgabe:
```
Durchschnittliche Engagement Rate
```

Erwarteter Rückgabewert:
```python
9.0
```

## Codegerüst
```python
def berechne_engagement_rate(likes, kommentare, follower):
    ## Hier Code einfügen
```

## Musterlösung
```python
def berechne_engagement_rate(likes, kommentare, follower):
    interaktionen = likes + kommentare
    engagement_rate = (interaktionen / follower) * 100
    if engagement_rate >= 10:
        print("Hohe Engagement Rate!")
    elif engagement_rate >= 5:
        print("Durchschnittliche Engagement Rate")
    else:
        print("Niedrige Engagement Rate")
    return engagement_rate

# Beispielaufruf
print(berechne_engagement_rate(150, 30, 2000))
```

## Unit Tests
```python
import unittest
from main import berechne_engagement_rate

class TestBerechneEngagementRate(unittest.TestCase):
    def test_hohe_engagement_rate(self):
        self.assertEqual(berechne_engagement_rate(200, 100, 2000), 15.0)

    def test_durchschnittliche_engagement_rate(self):
        self.assertEqual(berechne_engagement_rate(150, 30, 2000), 9.0)

    def test_niedrige_engagement_rate(self):
        self.assertEqual(berechne_engagement_rate(50, 20, 2000), 3.5)

    def test_null_follower(self):
        with self.assertRaises(ZeroDivisionError):
            berechne_engagement_rate(100, 50, 0)

    def test_keine_interaktionen(self):
        self.assertEqual(berechne_engagement_rate(0, 0, 2000), 0.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 629
