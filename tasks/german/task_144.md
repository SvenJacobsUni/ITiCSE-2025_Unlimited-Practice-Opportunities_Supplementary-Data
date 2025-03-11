# Input
- Programmierkonzept: Float;While-Schleifen
- Kontext: Musik

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Musik-Playlist

Schreibe eine Funktion namens `playlist_dauer(lieder)`, die eine Liste von Liedern als Eingabe erhält. Jedes Lied ist durch seine Dauer in Minuten als Float-Wert dargestellt. Die Funktion soll die Gesamtdauer der Playlist berechnen und zurückgeben. Verwende eine `while`-Schleife, um die Gesamtdauer zu berechnen.

Beispielaufruf:
```python
lieder = [3.5, 4.0, 2.75, 5.25]
print(playlist_dauer(lieder))  # Ausgabe: 15.5
```

### Anforderungen:
- Die Funktion soll eine `while`-Schleife verwenden.
- Die Funktion soll die Gesamtdauer der Playlist als Float-Wert zurückgeben.

## Codegerüst
```python
def playlist_dauer(lieder):
    ## Hier Code einfügen
```

## Musterlösung
```python
def playlist_dauer(lieder):
    i, gesamt = 0, 0.0
    while i < len(lieder):
        gesamt += lieder[i]
        i += 1
    return gesamt

lieder = [3.5, 4.0, 2.75, 5.25]
print(playlist_dauer(lieder))
```

## Unit Tests
```python
import unittest
from main import playlist_dauer

class TestPlaylistDauer(unittest.TestCase):
    def test_einfache_playlist(self):
        self.assertEqual(playlist_dauer([3.5, 4.0, 2.75, 5.25]), 15.5)

    def test_leere_playlist(self):
        self.assertEqual(playlist_dauer([]), 0.0)

    def test_ein_lied(self):
        self.assertEqual(playlist_dauer([4.5]), 4.5)

    def test_gemischte_dauern(self):
        self.assertEqual(playlist_dauer([1.0, 2.5, 3.75, 4.25]), 11.5)

    def test_grosse_playlist(self):
        self.assertEqual(playlist_dauer([1.0] * 1000), 1000.0)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 576
