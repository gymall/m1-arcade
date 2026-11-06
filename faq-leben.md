# FAQ: Leben aufladen

## Schritt 1: Der Heiltrank
Wenn dein Spieler Schaden nimmt, braucht er eine Möglichkeit, sich zu heilen. Dafür erstellen wir ein neues Item (z. B. ein Herz oder einen Heiltrank).

## Schritt 2: Die Kollision
Das Einsammeln funktioniert genauso wie beim Münzen sammeln!
* Gehe zu **Sprites** und hole die Bedingung `wenn sprite von Art Player anderesSprite von Art Player überlappt`.
* Ändere das zweite Dropdown von `Player` auf `Food` (oder lege über "Füge neue Art hinzu..." eine neue Art namens `Health` an).

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    
})
```

## Schritt 3: Das Leben heilen
* Gehe zu **Info** und ziehe den Block `ändere Leben um -1` in deine Bedingung.
* **Ganz wichtig:** Entferne das Minus! Schreibe eine normale `1` hinein, sonst verlierst du ein Leben beim Heilen.
* Gehe zu **Sprites** und hole `zerstöre mySprite`. Ändere `mySprite` in `otherSprite` (ziehe den roten Block von oben aus der Klammer hinein), damit das Herz danach verschwindet.

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeLifeBy(1)
    otherSprite.destroy()
})
```