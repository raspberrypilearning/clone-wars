## Game Over

Successivamente, aggiungerai un messaggio di "game over" alla fine del gioco.

\--- task \---

Se non lo hai già fatto, crea una nuova variabile chiamata `vite`{:class="block3variables"}.

La tua astronave dovrebbe iniziare con tre vite e perdere una vita ogni volta che tocca un ippopotamo o un'arancia. Il tuo gioco dovrebbe finire quando le `vite` {: class = "block3variables"} si esauriscono.

\--- /task \---

\--- task \---

Disegna un nuovo sprite chiamato `Game Over` utilizzando lo strumento **text**.

![schermata](images/invaders-game-over.png)

\--- /task \---

\--- task \---

Sullo schermo, fai apparire un broadcast con `game over`{:class="block3events"} subito prima che il gioco finisca.

![sprite gameover](images/stage-sprite.png)

```blocks3
trasmetti (game over v) e aspetta
```

\--- /task \---

\--- task \---

Aggiungi questo codice al tuo sprite `Game Over` così che lo faccia apparire alla fine del gioco:

![sprite gameover](images/gameover-sprite.png)

```blocks3
quando si fa clic sulla bandiera verde
nascondere

quando ricevo [game over v]
mostrare
```

Visto che hai usato un blocco `trasmettere(game over) e aspettare`{:class="block3events"} nel tuo scenario, lo scenario aspetterà lo sprite `Game Over` per essere mostrato prima della fine del gioco.

\--- /task \---

\--- task \---

Prova il tuo gioco. Quanti puinti puoi fare? Se il gioco è troppo facile o troppo difficile, puoi trovare qualche modo per migliorarlo?

\--- /task \---