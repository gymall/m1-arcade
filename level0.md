# Level 0: Das Bootcamp

## Schritt 1: Deine erste Figur (Sprite)
👋 **Willkommen im Code-Editor!** 

Um ein Spiel zu machen, brauchen wir eine Spielfigur. In der Informatik nennt man das einen **Sprite**.

* Ziehe den Block `setze mySprite auf` aus der Kategorie **Sprites** in den grünen Start-Block.

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
🎨 **Werde kreativ!**

* Klicke auf das graue Quadrat in deinem neuen Block. 
* Es öffnet sich der Zeichen-Editor. Zeichne deine eigene Figur (z.B. ein kleines Monster) und klicke auf "Fertig". 

Schau links auf den Bildschirm: Deine Figur ist im Spiel!

## Schritt 3: Bewegung!
Eine Figur, die nur herumsteht, ist langweilig. 

* Gehe in die Kategorie **Controller** (rot).
* Ziehe den Block `bewege mySprite mit Tasten` unter deinen ersten Block. 

🕹️ **Teste es:** Klicke links in den Simulator. Du kannst deine Figur jetzt steuern!

```blocks
let mySprite: Sprite = null
mySprite = sprites.create(img`
. . . . . . . . . . . . . . . .
`, SpriteKind.Player)
controller.moveSprite(mySprite)
```

## Schritt 4: Nicht aus dem Bildschirm fallen
Vielleicht ist deine Figur gerade aus dem Bildschirm verschwunden. Das wollen wir verhindern.

* Gehe nochmal zu **Sprites** und scrolle nach unten zu **Effekte**.
* Suche den Block `setze mySprite bleibt im Bildschirm auf AN`. 
* Hänge ihn ganz unten an deinen Code an.

```blocks
let mySprite: Sprite = null
mySprite = sprites.create(img`
. . . . . . . . . . . . . . . .
`, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setStayInScreen(true)
```

## Schritt 5: 📝 Dein Logbuch-Auftrag
**Herzlichen Glückwunsch, du hast das Bootcamp bestanden!**

Gehe nun zurück ins LMS in die Aufgabe "Das digitale Logbuch". 

1. Mache einen Screenshot von deinem fertigen Code und lade ihn dort hoch.
2. Beantworte dort diese Frage in 1-2 Sätzen: 

*"Du hast gerade deinen ersten **Algorithmus** programmiert! Ein Algorithmus ist eine genaue Schritt-für-Schritt-Anleitung für den Computer. Schau dir deine Blöcke an: In welcher Reihenfolge führt der Computer deine Befehle aus? (Tipp: Liest er von oben nach unten oder von unten nach oben?)"*
