# Level 0: Das Bootcamp

## Schritt 1: Deine erste Figur (Sprite)
Willkommen im Code-Editor! 
Um ein Spiel zu machen, brauchen wir eine Spielfigur. In der Informatik nennt man das einen **Sprite**.
Zieh den Block `setze mySprite auf` aus der Kategorie **Sprites** in den grünen Start-Block.

```blocks
let mySprite: Sprite = null
mySprite = sprites.create(img`
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
. . . . . . . . . . . . . . . .
`, SpriteKind.Player)
```

## Schritt 2: Zeichne deinen Sprite
Klicke auf das graue Quadrat in deinem neuen Block. 
Es öffnet sich der Zeichen-Editor. Zeichne deine eigene Figur (z.B. ein kleines Monster oder ein Raumschiff) und klicke auf "Fertig". Schau links auf den Bildschirm: Deine Figur ist im Spiel!

## Schritt 3: Bewegung!
Eine Figur, die nur herumsteht, ist langweilig. 
Gehe in die Kategorie **Controller** und ziehe den Block `bewege mySprite mit Tasten` unter deinen ersten Block. 
Teste links im Simulator: Du kannst deine Figur jetzt steuern!

```blocks
let mySprite: Sprite = null
mySprite = sprites.create(img`
. . . . . . . . . . . . . . . .
`, SpriteKind.Player)
controller.moveSprite(mySprite)
```

## Schritt 4: Nicht aus dem Bildschirm fallen
Vielleicht hast du gemerkt, dass deine Figur einfach aus dem Bildschirm verschwinden kann. Das wollen wir verhindern.
Gehe nochmal zu **Sprites**, scrolle etwas nach unten zu "Effekte" und suche den Block `setze mySprite bleibt im Bildschirm auf AN`. Hänge ihn ganz unten an.

```blocks
let mySprite: Sprite = null
mySprite = sprites.create(img`
. . . . . . . . . . . . . . . .
`, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setStayInScreen(true)
```

## Schritt 5: 📝 Dein Logbuch-Auftrag
Gehe nun zurück ins LMS in die Aufgabe "Das digitale Logbuch". 
1. Mache einen Screenshot von deinem Code und lade ihn dort hoch.
2. Beantworte dort diese Frage in 1-2 Sätzen: "In der Informatik sprechen wir oft von Daten. Ein Bild (dein Sprite) besteht aus Daten. In welchem der bunten Blöcke werden die Daten für dein Aussehen gespeichert?"