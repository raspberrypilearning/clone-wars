## Game Over

Ensuite, tu va rajouter un message 'game over' à la fin du jeu.

\--- task \---

Si tu ne l'a pas déjà fait, crée une nouvelle variable appelée ` vies `{:class="block3variables"}.

Ton vaisseau spatial devrait commencer avec trois vies et perdre une vie à chaque fois qu’il touche un hippopotame ou une orange. Ton jeu devrait s'arrêter lorsque les ` vies `{:class="block3variables"} sont épuisées.

\--- /task \---

\--- task \---

Dessine un nouveau sprite appelé ` Game Over ` en utilisant le texte ** ** outil.

![capture d'écran](images/invaders-game-over.png)

\--- /task \---

\--- task \---

Sur la scène, diffuser un message ` game over ` {: class = "blockevents"} juste avant la fin de la partie.

![lutin de gameover](images/stage-sprite.png)

```blocks3
broadcast (game over v) and wait
```

\--- /task \---

\--- task \---

Add this code to your `Game Over` sprite so that it shows at the end of the game:

![gameover sprite](images/gameover-sprite.png)

```blocks3
quand le drapeau cliqué
cacher

quand je reçois [game over v]
montrer
```

Because you've used a `broadcast (game over) and wait`{:class="block3events"} block on your Stage, the Stage will wait for the `Game Over` sprite to be displayed before ending the game.

\--- /task \---

\--- task \---

Test your game. How many points can you score? If the game is too easy or too hard, can you think of ways to improve it?

\--- /task \---