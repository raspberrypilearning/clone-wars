## Fin de la partie

Ensuite, tu va rajouter un message 'fin de la partie' à la fin du jeu.

\--- task \---

Si tu ne l'a pas déjà fait, crée une nouvelle variable appelée `vies`{:class="block3variables"}.

Ton vaisseau spatial devrait commencer avec trois vies et perdre une vie à chaque fois qu’il touche un hippopotame ou une orange. Ton jeu devrait s'arrêter lorsque les `vies`{:class="block3variables"} sont épuisées.

\--- /task \---

\--- task \---

Dessine un nouveau sprite appelé `Fin de la partie` en utilisant l'outil **texte**.

![capture d'écran](images/invaders-game-over.png)

\--- /task \---

\--- task \---

Sur la scène, diffuser un message `fin de la partie` {:class="blockevents"} juste avant la fin de la partie.

![sprite de gameover](images/stage-sprite.png)

```blocks3
envoyer à tous (game over v) et attendre
```

\--- /task \---

\--- task \---

Ajoutez ce code à ton sprite `Game Over` pour qu’il apparaisse à la fin du jeu :

![sprite de gameover](images/gameover-sprite.png)

```blocks3
quand le drapeau est cliqué
cacher

quand je reçois [game over v]
montrer
```

Parce que tu as utilisé un bloc `envoyer à tous (game over) et attendre` {:class="blockevents"} sur ta scène, le sprite `Game Over` attendra après avoir été affiché, avant de terminer le jeu.

\--- /task \---

\--- task \---

Teste ton jeu. Combien de points peux-tu marquer? Si le jeu est trop facile ou trop difficile, peux-tu penser à des moyens de l’améliorer ?

\--- /task \---