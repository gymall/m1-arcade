# FAQ: Highscore speichern

## Schritt 1: Den Rekord festhalten
Es ist ärgerlich, wenn man einen neuen Rekord aufstellt und das Spiel ihn nach dem Game Over sofort wieder vergisst. Wir wollen den Highscore (die höchste Punktzahl) dauerhaft im Browser speichern!

## Schritt 2: Der Highscore-Block
Du brauchst dafür nur einen einzigen Block!

* Überlege, wann das Spiel vorbei ist (z. B. wenn der Timer abläuft, Leben auf 0 fallen, oder der Spieler das Ziel erreicht).
* Gehe zur Kategorie **Info**.
* Ziehe den Block `sichere Höchstpunktestand` genau dorthin, wo der Spieler gewinnt oder verliert. Wichtig: Mache das noch *vor* einem eventuellen Game Over Block.

🕹️ **Teste es:** Sammle ein paar Punkte und beende das Spiel. Wenn du es neu startest, siehst du deinen alten Rekord nun als Pokal neben deinem aktuellen Punktestand!

```blocks
scene.onOverlapTile(SpriteKind.Player, assets.tile`transparency16`, function (sprite, location) {
    info.saveHighScore()
    game.gameOver(true)
})
```