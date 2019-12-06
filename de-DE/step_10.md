## Game over

Als Nächstes fügst Du am Ende des Spiels eine "Game Over"-Nachricht hinzu.

\--- task \---

Wenn Du es noch nicht getan hast, erstelle jetzt eine neue Variable mit dem Namen `Leben`{:class="block3variables"}.

Dein Raumschiff sollte mit drei Leben beginnen und ein Leben verlieren, wenn es ein Flusspferd oder eine Orange berührt. Dein Spiel sollte aufhören, wenn die `Leben`{:class="block3variables"} ausgehen.

\--- /task \---

\--- task \---

Male mit dem **Text**-Werkzeug eine neue Figur mit dem Namen `Game Over`.

![Screenshot](images/invaders-game-over.png)

\--- /task \---

\--- task \---

Senden Sie auf der Bühne eine `Spiel-über-`Nachricht ({: class = "block3events"}), bevor das Spiel endet.

![Gameover-Figur](images/stage-sprite.png)

```blocks3
sende (game over v) an alle und warte
```

\--- /task \---

\--- task \---

Füge diesen Code zu deiner `Game-Over-`-Figur hinzu, sodass sie am Ende des Spiels angezeigt wird:

![Gameover-Figur](images/gameover-sprite.png)

```blocks3
Wenn die grüne Flagge angeklickt
verstecke dich

Wenn ich [game over v] empfange
zeige dich
```

Da du einen `sende (game over) an alle und warte`{:class="block3events"} Block auf deiner Bühne verwendet hast, wartet die Bühne, bis die `Game-Over-`-Figur angezeigt wird, bevor sie das Spiel beendet.

\--- /task \---

\--- task \---

Teste dein Spiel. Wie viele Punkte kannst Du erzielen? Wenn das Spiel zu einfach oder zu schwer ist, kannst Du Möglichkeiten finden, es zu verbessern?

\--- /task \---