# FAQ: Schwerkraft (Jump'n'Run)

## Schritt 1: Die Erdanziehungskraft
In einem Jump'n'Run (wie Super Mario) fallen Figuren immer nach unten, wenn sie nicht auf einem Block stehen. In der Physik (und in MakeCode) nennt man das **Beschleunigung** (engl. Acceleration).

* Gehe zur Kategorie **Sprites**.
* Scrolle nach unten zu "Geschwindigkeit" und hole den Block `setze mySprite Geschwindigkeit vx auf 0`.
* Klicke auf das `vx` und ändere es zu `ay` (Acceleration Y = Beschleunigung nach unten).
* Trage als Zahl `500` ein und lege den Block in deinen Start-Block.

```blocks
let mySprite: Sprite = null
mySprite.ay = 500
```

## Schritt 2: Springen!
Jetzt fällt deine Figur wie ein Stein. Wir müssen ihr das Springen beibringen! Ein Sprung ist eine kurze, starke Bewegung nach oben (negative y-Richtung).

* Gehe zu **Controller** und hole `wenn Taste A gedrückt`.
* Hole nochmal den `setze mySprite Geschwindigkeit`-Block aus **Sprites**.
* Ändere diesmal das `vx` zu `vy` (Velocity Y = Geschwindigkeit nach oben/unten).
* Trage eine Minus-Zahl ein (z. B. `-200`), damit die Figur nach oben springt!

## Schritt 3: Der Doppel-Sprung-Bug
Vielleicht merkst du, dass deine Figur fliegen kann, wenn du ganz oft A drückst. Um das zu verhindern, müssen wir den Computer prüfen lassen, ob die Figur den Boden berührt!

* Gehe zu **Logik** und hole eine `wenn wahr dann`-Bedingung.
* Gehe zu **Szene** (Kollisionen) und hole `mySprite trifft Wand unten`. Setze das in das `wahr` ein.
* Schiebe deinen vy-Sprungblock in die Wenn-Dann-Bedingung. Jetzt kann man nur springen, wenn man auf dem Boden (einer Tilemap-Wand) steht!

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    if (mySprite.isHittingTile(CollisionDirection.Bottom)) {
        mySprite.vy = -200
    }
})
```