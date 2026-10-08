# Skill: Tilemaps (Level bauen)

## Schritt 1: Das Spielfeld
Ein leerer schwarzer Bildschirm ist auf Dauer langweilig. Mit einer **Tilemap** (Kachelkarte) kannst du richtige Welten bauen. Ein "Tile" ist eine kleine quadratische Kachel (16x16 Pixel). Aus vielen Kacheln setzt du dein Level wie ein Mosaik zusammen.

* Gehe zur Kategorie **Szene** (dunkelgrün).
* Ziehe den Block `setze Kachelkarte auf` in deinen grünen Start-Block.

```blocks
tiles.setCurrentTilemap(tilemap`level1`)
```

## Schritt 2: Zeichne deine Welt
Klicke auf das graue Quadrat in deinem neuen Block. Der Tilemap-Editor öffnet sich!
* Wähle links deine Kacheln aus (z.B. Gras, Wege, Wände) und zeichne dein Level.
* **WICHTIG:** Wenn deine Figur nicht durch bestimmte Kacheln laufen soll (z.B. durch Wände), musst du das **Wand-Werkzeug** (das rote Quadrat mit den Steinen in der Mitte) auswählen und diese Kacheln rot markieren!

## Schritt 3: Die Kamera
Wenn dein Level größer gezeichnet ist als der kleine Gameboy-Bildschirm, muss die Kamera deiner Spielfigur folgen, sonst verschwindet sie aus dem Bild.
* Gehe zu **Szene**.
* Scrolle nach unten zum Bereich "Kamera".
* Ziehe den Block `Kamera folgt Sprite mySprite` ganz unten an deinen Start-Code (unter deine Figur).

```blocks
let mySprite: Sprite = null
tiles.setCurrentTilemap(tilemap`level1`)
scene.cameraFollowSprite(mySprite)
```

## Schritt 4: 📝 Dein Logbuch-Auftrag
Gehe nun in dein Logbuch im LMS.
Lade als Erstes einen Screenshot hoch, auf dem man sieht, wie du die Tilemap oder Kamera eingebaut hast.

Beantworte danach diese Aufgaben in eigenen Sätzen:

1. **Der Fachbegriff:** Was genau ist eine "Tilemap" (Kachelkarte) und wie baut der Computer daraus eine Welt zusammen?
2. **Die Lebenswelt / Gamedesign:** Warum ist es so wichtig, dass wir dem Computer mit dem roten Wand-Werkzeug sagen müssen, was eine feste Wand ist? Was würde im Spiel passieren, wenn wir diesen Algorithmus vergessen?
