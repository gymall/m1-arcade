# FAQ: Nächstes Level laden

## Schritt 1: Das Ziel erreichen
Wenn der Spieler eine Tür, eine Treppe oder eine Schatztruhe in deiner Tilemap erreicht, soll das nächste Level starten. 

## Schritt 2: Kollision mit der Tilemap
Wir brauchen eine besondere Wenn-Dann-Bedingung, die prüft, ob die Figur eine bestimmte *Kachel* (Tile) berührt.

* Gehe zur Kategorie **Szene** (dunkelgrün).
* Scrolle nach unten zu "Überschneidungen".
* Hole den großen Block `wenn sprite von Art Player überschneidet [Kachel] an location`.
* Klicke auf das Kachel-Bild im Block und wähle dein Ziel (z. B. die Tür) aus.

```blocks
scene.onOverlapTile(SpriteKind.Player, assets.tile`transparency16`, function (sprite, location) {
    
})
```

## Schritt 3: Das neue Level laden
* Gehe in die Bedingung, die du gerade erstellt hast.
* Ziehe aus der Kategorie **Szene** einen neuen Block `setze Kachelkarte auf` hinein.
* Klicke auf das graue Quadrat und zeichne dein 2. Level!

```blocks
scene.onOverlapTile(SpriteKind.Player, assets.tile`transparency16`, function (sprite, location) {
    tiles.setCurrentTilemap(tilemap`level2`)
})
```