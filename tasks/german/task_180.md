# Input
- Programmierkonzept: Tupel;Operationen mit Zahlen;Kontrollstrukturen (==, !=, <, >, <=, >=, or, and, not)
- Kontext: Musik

# Generierte Aufgabenkomponenten
## Aufgabenstellung
### Übungsaufgabe: Musik-Playlist-Analyse

Schreibe eine Funktion namens `analyse_playlist(playlist)`, die eine Liste von Tupeln als Argument erhält. Jedes Tupel repräsentiert einen Song und enthält zwei Elemente: den Namen des Songs (String) und die Dauer des Songs in Sekunden (Integer).

Die Funktion soll die folgenden Aufgaben erfüllen:
1. Überprüfen, ob die Playlist mindestens 5 Songs enthält. Wenn nicht, soll die Funktion "Zu wenige Songs in der Playlist" zurückgeben.
2. Den längsten Song in der Playlist finden und seinen Namen zurückgeben.
3. Den kürzesten Song in der Playlist finden und seinen Namen zurückgeben.
4. Die durchschnittliche Dauer der Songs in der Playlist berechnen und zurückgeben.

Beispielaufruf:
```python
playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200)]
analyse_playlist(playlist)
```

Erwartete Rückgabe:
```python
("Längster Song: Song C", "Kürzester Song: Song D", "Durchschnittliche Dauer: 196.0 Sekunden")
```

## Codegerüst
```python
def analyse_playlist(playlist):
    ## Hier Code einfügen
```

## Musterlösung
```python
def analyse_playlist(playlist):
    if len(playlist) < 5:
        return "Zu wenige Songs in der Playlist"
    longest = max(playlist, key=lambda x: x[1])
    shortest = min(playlist, key=lambda x: x[1])
    avg_duration = sum(song[1] for song in playlist) / len(playlist)
    return (f"Längster Song: {longest[0]}", f"Kürzester Song: {shortest[0]}", f"Durchschnittliche Dauer: {avg_duration:.1f} Sekunden")

playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200)]
print(analyse_playlist(playlist))
```

## Unit Tests
```python
import unittest
from main import analyse_playlist

class TestAnalysePlaylist(unittest.TestCase):
    def test_zu_wenige_songs(self):
        playlist = [("Song A", 210), ("Song B", 180)]
        self.assertEqual(analyse_playlist(playlist), "Zu wenige Songs in der Playlist")

    def test_längster_song(self):
        playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200)]
        result = analyse_playlist(playlist)
        self.assertIn("Längster Song: Song C", result)

    def test_kürzester_song(self):
        playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200)]
        result = analyse_playlist(playlist)
        self.assertIn("Kürzester Song: Song D", result)

    def test_durchschnittliche_dauer(self):
        playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200)]
        result = analyse_playlist(playlist)
        self.assertIn("Durchschnittliche Dauer: 196.0 Sekunden", result)

    def test_genau_fünf_songs(self):
        playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200)]
        result = analyse_playlist(playlist)
        self.assertEqual(result, ("Längster Song: Song C", "Kürzester Song: Song D", "Durchschnittliche Dauer: 196.0 Sekunden"))

    def test_mehr_als_fünf_songs(self):
        playlist = [("Song A", 210), ("Song B", 180), ("Song C", 240), ("Song D", 150), ("Song E", 200), ("Song F", 300)]
        result = analyse_playlist(playlist)
        self.assertEqual(result, ("Längster Song: Song F", "Kürzester Song: Song D", "Durchschnittliche Dauer: 213.3 Sekunden"))

if __name__ == '__main__':
    unittest.main()
```
___
# Metadata
Database ID: 612
