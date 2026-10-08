# Skill: Bedingungen (Kollision)

## Schritt 1: Die Wenn-Dann-Regel
In Spielen passieren Dinge oft nur, **WENN** eine bestimmte Bedingung erfüllt ist. **DANN** wird eine Aktion ausgeführt. In der Informatik nennt man das eine **Bedingung** oder **Verzweigung**.

Die häufigste Bedingung in Retro-Spielen ist die Kollision (Überschneidung): *WENN der Spieler das Monster berührt, DANN verliert er ein Leben.*

## Schritt 2: Die Kollision abfragen
Lass uns so eine Verzweigung bauen! Wir gehen davon aus, dass du bereits einen Spieler und z. B. ein Stück Essen (Food) erstellt hast.

* Gehe zur Kategorie **Sprites**.
* Scrolle nach unten zum Bereich "Überschneidungen".
* Ziehe den großen Block `wenn sprite von Art Player anderesSprite von Art Player überlappt` auf deine Arbeitsfläche.
* Ändere das zweite Dropdown-Menü von `Player` auf `Food`.

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
	
})
```

## Schritt 3: Die DANN-Aktion festlegen
Jetzt müssen wir dem Computer sagen, was passieren soll, wenn die Bedingung erfüllt ist. 

* Gehe zu **Sprites** und hole den Block `zerstöre mySprite`. Ziehe ihn in deine Bedingung.
* **WICHTIG:** Ziehe das rote Wort `otherSprite` (anderes Sprite) von oben aus der Klammer des großen Blocks direkt in das Feld `mySprite` deines Zerstören-Blocks. So weiß der Computer, dass das Essen verschwinden soll und nicht der Spieler.
* Gehe zu **Info** und füge `ändere Punktzahl um 1` hinzu.

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    otherSprite.destroy()
    info.changeScoreBy(1)
})
```

## Schritt 4: 📝 Dein Logbuch-Auftrag
Gehe nun in dein Logbuch im LMS.
Lade als Erstes einen Screenshot hoch, auf dem man sieht, wo du in deinem Spiel eine eigene Wenn-Dann-Bedingung (Verzweigung) eingebaut hast.

Beantworte danach diese Aufgaben in eigenen Sätzen:

1. **Der Fachbegriff:** Erkläre in deinen eigenen Worten, was eine **Bedingung** (oder Verzweigung) in einem Programmkreis macht. Warum ist das Wort "Wenn-Dann" dabei so wichtig?
2. **Die Lebenswelt:** Eine Bedingung trifft Entscheidungen. Stelle dir vor, du programmierst einen **Smart-Home-Roboter** für dein Haus. Nenne zwei Beispiele für "Wenn-Dann"-Regeln (Bedingungen), auf die der Roboter im Alltag reagieren muss (z. B. wenn es dunkel wird, oder wenn es anfängt zu regnen).
