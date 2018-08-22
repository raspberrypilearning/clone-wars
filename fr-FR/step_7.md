## Hippopotames disparus

Lorsque le vaisseau spatial est touché, tous les hippopotames doivent disparaître pour permettre au joueur de récupérer.

+ Ajouter un bloc à votre code pour `diffuser` le message «touché » lorsque le vaisseau spatial entre en contact avec un hippopotame.

[[[generic-scratch-broadcast-message]]]

\--- hints \--- \--- hint \--- Créer une diffusion ` ` "touché" en faisant glisser le bloc des ** événements ** puis en cliquant sur le menu déroulant et en sélectionnant ** nouveau message ** . \---/hint\--- \---hint\--- Voici a quoi devrait ressembler votre bloc

```blocks
diffuser [touché v]
```

\---/hint\--- \---hint\--- Voici a quoi devrait ressembler votre bloc

```blocks
lorsque le drapeau vert est cliqué 
changez de costume pour [normal v]
attendez jusqu'à <touché par [Hippo]>?
changer de costume pour [touché v]
diffuser [touché v]
```

\--- /hint \--- \--- /hints \---

Tous les clones ` Hippo ` entendront ce message, vous pouvez donc leur demander de disparaître lorsque le vaisseau spatial est touché.

+ Ajoutez ce code au lutin ` Hippo ` :

```blocks
quand je reçois [touché v]
effacer ce clone
```

+ Testez ce code en commençant un nouveau jeu et en entrant en collision avec un hippopotame.

![capture d'écran](images/invaders-hippo-collide.png)

Après avoir été touché, les hippopotames commencent à réapparaître mais le vaisseau spatial a encore explosé! Permettons au vaisseau spatial de se réinitialiser après avoir été touché.

+ Ajouter une boucle ` indéfiniment ` {: class = "blockcontrol"} autour de tout votre code pour que le processus se répète, et un `attendre` {: class = "blockcontrol"} à la fin pour ajouter une petite pause avant que les hippopotames ne réapparaissent.

```blocks
lorsque le drapeau vert est cliqué
répéter indéfiniment  
   changez de costume pour [normal v]
   attendez jusqu'à <touché par [Hippo]>?
   changer de costume pour [touché v]
   diffuser [touché v]
   attendre (1) secondes
terminer
```

\--- challenge \---

### Défi: vie et score

Pour le moment, le joueur a des vies illimitées. Pouvez-vous ajouter des variables ` vies ` {: class = "blockdata"}, ` score ` {: class = "blockdata"}, ou même ` meilleur score ` {: class = "blockdata"} à votre jeu?

[[[generic-scratch-high-score]]] \--- / challenge \---