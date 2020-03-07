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
broadcast (game over v) and wait
```

\--- /task \---

\--- task \---

Add this code to your `Game Over` sprite so that it shows at the end of the game:

![gameover sprite](images/gameover-sprite.png)

```blocks3
when flag clicked
hide

when I receive [game over v]
show
```

Because you've used a `broadcast (game over) and wait`{:class="block3events"} block on your Stage, the Stage will wait for the `Game Over` sprite to be displayed before ending the game.

\--- /task \---

\--- task \---

Test your game. How many points can you score? If the game is too easy or too hard, can you think of ways to improve it?

\--- /task \---