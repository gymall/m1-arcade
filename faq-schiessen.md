# FAQ: Projektile schießen

## Schritt 1: Die Waffe laden
Wenn deine Figur schießen soll (z. B. Laser, Feuerbälle oder Pfeile), nutzen wir dafür keine normalen Sprites, sondern spezielle **Projektile**. Ein Projektil fliegt automatisch in eine bestimmte Richtung und wird gelöscht, sobald es den Bildschirm verlässt.

## Schritt 2: Auf Knopfdruck feuern
Lass uns auf Tastendruck einen Feuerball schießen.

* Gehe zu **Controller** und hole den Block `wenn Taste A gedrückt`. (Du kannst A auch auf B ändern).
* Gehe zu **Sprites** und scrolle zu "Projektile".
* Hole den großen Block `setze projectile auf Projektil [Bild] von mySprite mit vx 50 vy 50`.
* Zeichne deinen Laser oder Feuerball in das graue Quadrat.

## Schritt 3: Die Richtung einstellen (vx und vy)
Dein Schuss braucht eine Geschwindigkeit und eine Richtung.
* **vx** ist die Geschwindigkeit nach rechts (positiv) oder links (negativ).
* **vy** ist die Geschwindigkeit nach unten (positiv) oder oben (negativ).
* Wenn du willst, dass dein Laser geradeaus nach rechts fliegt, trage bei `vx 100` und bei `vy 0` ein.

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    let projectile = sprites.createProjectileFromSprite(img`
. . . . . . . . . . . . . . . .
`, mySprite, 100, 0)
})
```