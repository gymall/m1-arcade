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
Gehe nun ins LMS in die Aufgabe "Das digitale Logbuch". 
Lade dort als Erstes einen Screenshot von deinem fertigen Code hoch. 

Beantworte danach diese Fragen in eigenen Sätzen:

1. **Der Fachbegriff:** Du hast heute deinen ersten **Algorithmus** gebaut. Ein Algorithmus ist eine genaue, schrittweise Abfolge von Befehlen. Womit aus deinem Alltag (z.B. beim Kochen oder beim Aufbau von Möbeln) kann man so einen Algorithmus am besten vergleichen? 
2. **Die Reihenfolge:** Was würde bei deinem Alltags-Beispiel passieren, wenn man die Reihenfolge der Anleitung einfach vertauscht?
3. **Dein Code:** Ein Computer liest Algorithmen streng von oben nach unten. Was würde wohl passieren, wenn du in MakeCode den roten `bewege mySprite`-Block nach ganz oben schiebst, noch *bevor* die Figur überhaupt erstellt wird?
