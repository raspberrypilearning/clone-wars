## Défi : Améliorez votre jeu

Lorsque le vaisseau spatial explose, tous les hippopotames devraient disparaître afin que les joueurs puissent se remettre

\--- task \---

Ajoutez du code au sprite du vaisseau spatial pour le rendre `diffusé`{: class = "block3events"} le message "touché" lorsque le vaisseau spatial `touche un hippo`{: class = "block3sensing"}.

![lutin de roquette](images/rocket-sprite.png)

```blocks3
lorsque le drapeau a cliqué sur
passez de costume à (normal v)
attendez jusqu'à <touching (Hippo1 v)>?
costume de commutation pour (hit v)

+ diffusion (hit v)
```

\--- /task \---

\--- task \---

Tous les `clones du sprite` Hippo recevront le message "hit", et vous pouvez leur demander de disparaître quand le vaisseau spatial est touché en ajoutant ce code au sprite `Hippo`:

![hippo sprite](images/hippo-sprite.png)

```blocks3
quand je reçois [touché v]
effacer ce clone
```

\--- /task \---

\--- task \---

Pour vérifier si le nouveau code fonctionne, cliquez sur le drapeau vert et faites entrer le vaisseau spatial en collision avec un hippopotame.

![screenshot](images/invaders-hippo-collide.png)

\--- /task \---

Après l'explosion du vaisseau spatial, de nouveaux clones `Hippo` apparaissent, mais le vaisseau spatial explose encore! Le vaisseau spatial doit se réinitialiser après avoir été touché.

\--- task \---

Ajoutez un bloc `wait`{: class = "block3control"} à la fin du code du sprite `Spaceship` pour créer une petite pause avant la réapparition des hippopotames. Ajoutez ensuite un bloc `pour toujours`{: class = "block3control"} autour de tout votre code pour le faire exécuter à plusieurs reprises.

![lutin de roquette](images/rocket-sprite.png)

```blocks3
quand le drapeau a cliqué sur
pour toujours
changer de costume en (normal v)
attendre jusqu'à <touching (Hippo1 v)>?
costume de commutation pour (hit v)
diffusion (hit v)

+ wait (1) secondes
end
```

\--- /task \---