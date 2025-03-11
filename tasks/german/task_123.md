# Input
- Programmierkonzept: While-Schleifen;If-Else-Anweisungen
- Kontext: Musik

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Musik-Playlist

Schreibe eine Funktion namens `spiele_playlist(lieder)`, die eine Liste von Liedern als Argument erhält. Die Funktion soll jedes Lied in der Liste abspielen, bis ein bestimmtes Lied namens "Stop" gefunden wird. Wenn das Lied "Stop" gefunden wird, soll die Wiedergabe beendet werden. Wenn das Lied "Stop" nicht in der Liste enthalten ist, soll die gesamte Liste abgespielt werden.

Beispielaufruf:
```python
spiele_playlist(["Song1", "Song2", "Stop", "Song3"])
```

Erwartetes Verhalten:
- "Song1" wird abgespielt.
- "Song2" wird abgespielt.
- Wiedergabe wird gestoppt, da "Stop" gefunden wurde.

## Codegerüst
```python
def spiele_playlist(lieder):
    ## Hier Code einfügen
```

## Musterlösung
```python
def spiele_playlist(lieder):
    for lied in lieder:
        if lied == "Stop":
            break
        print(f"Spiele {lied}")

spiele_playlist(["Song1", "Song2", "Stop", "Song3"])
```

## Unit Tests
```python
import unittest
from main import spiele_playlist
from io import StringIO
import sys

class TestSpielePlaylist(unittest.TestCase):
    def test_playlist_mit_stop(self):
        lieder = ["Song1", "Song2", "Stop", "Song3"]
        expected_output = "Spiele Song1\nSpiele Song2\n"
        captured_output = StringIO()
        sys.stdout = captured_output
        spiele_playlist(lieder)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue(), expected_output)

    def test_playlist_ohne_stop(self):
        lieder = ["Song1", "Song2", "Song3"]
        expected_output = "Spiele Song1\nSpiele Song2\nSpiele Song3\n"
        captured_output = StringIO()
        sys.stdout = captured_output
        spiele_playlist(lieder)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue(), expected_output)

    def test_leere_playlist(self):
        lieder = []
        expected_output = ""
        captured_output = StringIO()
        sys.stdout = captured_output
        spiele_playlist(lieder)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue(), expected_output)

    def test_playlist_nur_stop(self):
        lieder = ["Stop"]
        expected_output = ""
        captured_output = StringIO()
        sys.stdout = captured_output
        spiele_playlist(lieder)
        sys.stdout = sys.__stdout__
        self.assertEqual(captured_output.getvalue(), expected_output)

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 555
