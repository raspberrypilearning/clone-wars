## Hippopotames qui disparaissent

Lorsque le vaisseau spatial explose, tous les hippopotames devraient disparaître afin que les joueurs du jeu puissent récupérer.

\--- task \---

Ajoute du code au sprite du vaisseau spatial pour le faire `envoyer à tous`{:class="block3events"} le message "hit" lorsque le vaisseau spatial `touche un hippo`{:class="block3sensing"}.

![sprite de roquette](images/rocket-sprite.png)

```blocks3
quand le drapeau est cliqué
basculer sur le costume (normal v)
attendre jusqu'à ce que <touching (Hippo1 v)>?
basculer sur le costume (hit v)

+ envoyer à tous (hit v)
```

\--- /task \---

\--- task \---

Tous les `clones du sprite` Hippo recevront le message "hit", et tu peux leur demander de disparaître quand le vaisseau spatial est touché en ajoutant ce code au sprite `Hippo` :

![sprite hippopotame](images/hippo-sprite.png)

```blocks3
quand je reçois [hit v]
supprimer ce clone
```

\--- /task \---

\--- task \---

Pour vérifier si le nouveau code fonctionne, clique sur le drapeau vert et fais entrer le vaisseau spatial en collision avec un hippopotame.

![capture d'écran](images/invaders-hippo-collide.png)

\--- /task \---

Après l'explosion du vaisseau spatial, de nouveaux clones `Hippo` apparaissent, mais le vaisseau spatial explose encore ! Le vaisseau spatial doit se réinitialiser après avoir été touché.

\--- task \---

Ajoute un bloc `attendre`{:class="block3control"} à la fin du code du sprite `Spaceship` pour créer une petite pause avant la réapparition des hippopotames. Ajoute ensuite un bloc `répéter indéfiniment`{:class="block3control"} englobant tout le code pour le faire exécuter à plusieurs reprises.

![sprite de roquette](images/rocket-sprite.png)

```blocks3
quand le drapeau est cliqué
répéter indéfiniment
basculer sur le costume (normal v)
attendre jusqu'à ce que <touching (Hippo1 v)>?
basculer sur le costume (hit v)
envoyer à tous (hit v)

+ attendre (1) secondes
fin
```

\--- /task \---