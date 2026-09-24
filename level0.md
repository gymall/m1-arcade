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

Gehe nun zurück ins LMS in die Aufgabe "Das digitale Logbuch". Lade dort als Erstes einen Screenshot von deinem fertigen Code hoch. Beantworte danach diese drei Fragen in eigenen Sätzen:

1. **Der Fachbegriff:** Du hast heute deinen ersten **Algorithmus** gebaut. Überlege oder recherchiere kurz: Womit aus deinem Alltag kann man einen Algorithmus am besten vergleichen? (Tipp: Denk ans Kochen oder an den Aufbau von Möbeln).
2. **Die Reihenfolge:** Was würde bei deinem Alltags-Beispiel passieren, wenn man die Reihenfolge der Anleitung einfach wild vertauscht?
3. **Dein Code:** Ein Computer liest Algorithmen streng von oben nach unten. Was würde wohl passieren, wenn du in MakeCode den roten `bewege mySprite`-Block nach ganz oben schiebst, noch *bevor* die Figur überhaupt erstellt wird?
