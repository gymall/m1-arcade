# Skill: Variablen (Punkte & Leben)

## Schritt 1: Startwerte festlegen
In einem Spiel brauchst du oft Zahlen, die sich im Laufe der Zeit verändern (wie einen **Punktestand** oder **Leben**). In der Informatik nennt man das eine **Variable**. 

Stell dir eine Variable wie eine leere Umzugskiste vor, auf der mit Edding "Punkte" steht. Am Anfang des Spiels müssen wir dem Computer sagen, was in der Kiste liegt.

* Gehe zur Kategorie **Info** (dunkelrot).
* Ziehe die Blöcke `setze Punktzahl auf 0` und `setze Leben auf 3` in deinen grünen Start-Block.

```blocks
info.setScore(0)
info.setLife(3)
```

## Schritt 2: Punkte sammeln!
Wenn der Spieler in deinem Spiel etwas Gutes tut, muss sich die Zahl in unserer "Punkte-Kiste" ändern. 

Lass uns das isoliert testen: Wir geben uns einfach einen Punkt, jedes Mal wenn wir die Taste A drücken.
* Gehe zu **Controller** und hole den Block `wenn Taste A gedrückt`.
* Gehe zu **Info** und ziehe `ändere Punktzahl um 1` hinein.

🕹️ **Teste es:** Drücke im Simulator links oft auf die Taste A (oder die Leertaste auf deiner Tastatur). Oben rechts steigt dein Punktestand!

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    info.changeScoreBy(1)
})
```

## Schritt 3: In dein Spiel einbauen
Du weißt jetzt, wie die Blöcke funktionieren. Lösche den `wenn Taste A gedrückt`-Block wieder. 
Baue die Info-Blöcke nun in *dein eigenes* Spiel ein (z. B. wenn sich zwei Sprites berühren). 

## Schritt 4: 📝 Dein Logbuch-Auftrag
Gehe nun in dein Logbuch im LMS und bearbeite diese Aufgabe:

1. **Dein Code:** Lade einen Screenshot hoch, auf dem man sieht, wo du in deinem eigenen Spiel eine Variable veränderst (z. B. Punkte plus 1 oder Leben minus 1).
2. **Die Lebenswelt:** Eine Variable ist wie eine beschriftete Kiste, in der sich der Computer Zahlen oder Wörter merkt. Stelle dir vor, du programmierst einen **Online-Shop** (wie Amazon) statt eines Spiels. Nenne zwei Beispiele für solche "Kisten" (Variablen), die der Computer in einem Online-Shop zwingend speichern und verändern muss, wenn ein Kunde etwas einkauft.
