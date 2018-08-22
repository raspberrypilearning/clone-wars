## Game Over

Ajoutons un message 'game over' à la fin du jeu.

+ Si vous ne l'avez pas déjà fait, créez une nouvelle variable appelée ` vies ` {: class = "blockdata"}.

Votre vaisseau spatial devrait commencer avec trois vies et perdre une vie chaque fois qu'il touche un hippopotame ou une orange. Votre jeu devrait également s'arrêter lorsque vous n'avez plus de vie. Si vous avez besoin d'aide, vous pouvez utiliser le projet [ Catch the dots ](https://codeclubprojects.org/en-GB/scratch/catch-the-dots/) pour vous aider.

+ Dessine un nouveau sprite appelé ` Game Over ` en utilisant le texte ** ** outil.

![capture d'écran](images/invaders-game-over.png)

+ Sur votre scène, diffuser un message ` game over ` {: class = "blockevents"} juste avant la fin de la partie.

```blocks
diffusion [game over v] et attendez
```

+ Ajoutez ce code à votre lutin `Game Over`, jusqu'à ce que le message indique à la fin du jeu :

```blocks
quand le drapeau cliqué
cacher

quand je reçois [game over v]
montrer
```

Parce que vous avez utilisé un bloc `diffuser [game over] et attendre` { : class = « blockevents »} sur votre scène, le lutin `Game Over` attendra après avoir été afficher avant de terminer le jeu.

+ Testez votre jeu. Combien de points pouvez-vous marquer? Si c'est trop facile ou trop difficile, pouvez-vous trouver des moyens d'améliorer votre jeu?