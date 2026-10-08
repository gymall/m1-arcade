# Skill: Schleifen (Gegner erschaffen)

## Schritt 1: Ständige Wiederholungen
Manche Dinge in einem Spiel passieren immer wieder. Anstatt einen Befehl hundertmal untereinander zu schreiben, nutzen Programmierer eine **Schleife** (engl. Loop). 

Eine Schleife wiederholt Befehle automatisch. Wir nutzen jetzt eine zeitgesteuerte Schleife, um endlos neue Gegner erscheinen zu lassen.

* Gehe in die Kategorie **Spiel** (dunkelblau).
* Suche den Block `bei Spiel-Update alle 500 ms` und ziehe ihn auf die freie Arbeitsfläche.

```blocks
game.onUpdateInterval(500, function () {
	
})
```

## Schritt 2: Den Gegner spawnen
Alles, was wir jetzt in diesen Block packen, wird alle 500 Millisekunden (also zweimal pro Sekunde) ausgeführt. Das ist unsere Endlosschleife.

* Gehe zu **Sprites** und hole den Block `setze mySprite auf`. Ziehe ihn in deine Schleife.
* Ändere den Namen der Variablen von `mySprite` zu `Gegner`.
* Ändere die Art (rechts im Block) von `Player` zu `Enemy`.
* Klicke auf das graue Quadrat und zeichne deinen Gegner.

```blocks
let Gegner: Sprite = null
game.onUpdateInterval(500, function () {
    Gegner = sprites.create(img`
. . . . . . . . . . . . . . . .
`, SpriteKind.Enemy)
})
```

## Schritt 3: Zufällige Positionen
Wenn alle Gegner an der gleichen Stelle auftauchen, ist das Spiel langweilig.

* Gehe zu **Sprites** und hole `setze mySprite x auf 0`. Ziehe ihn unter deinen Gegner und ändere `mySprite` auf `Gegner`.
* Gehe zur Kategorie **Mathematik** (lila).
* Hole den Block `wähle eine zufällige Zahl von 0 bis 10`. Ziehe ihn in die `0` deines X-Blocks.
* Ändere die Zahlen auf `0` bis `160` (so breit ist der Bildschirm).
* *Tipp: Damit die Gegner sich auch bewegen, gib ihnen danach eine Geschwindigkeit (vy) nach unten!*

```blocks
let Gegner: Sprite = null
game.onUpdateInterval(500, function () {
    Gegner = sprites.create(img`
. . . . . . . . . . . . . . . .
`, SpriteKind.Enemy)
    Gegner.x = randint(0, 160)
})
```

## Schritt 4: 📝 Dein Logbuch-Auftrag
Gehe nun in dein Logbuch im LMS.
Lade als Erstes einen Screenshot hoch, auf dem man sieht, wo du in deinem eigenen Spiel eine **Schleife** nutzt.

Beantworte danach diese Aufgaben in eigenen Sätzen:

1. **Der Fachbegriff:** Erkläre kurz, was eine **Schleife** in einem Programm macht und warum Programmierer sie benutzen (statt den Code ganz oft untereinander zu schreiben).
2. **Die Lebenswelt:** Schleifen gibt es nicht nur im Computer, sondern überall dort, wo Maschinen arbeiten. Nenne ein Beispiel aus dem echten Leben (z. B. in einer Fabrik, bei einer Ampel oder bei einem Haushaltsgerät), bei dem eine Aktion in einer "Endlosschleife" immer und immer wieder ausgeführt wird.
