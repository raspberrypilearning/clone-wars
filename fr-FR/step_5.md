## Une chauve-souris !

Tu vas maintenant ajouter de nombreux hippopotames volants qui tentent de détruire ton vaisseau spatial.

\--- task \---

Créez une nouvelle image-objet avec l'image 'Hippo1' dans la bibliothèque Scratch. Utilisez l’outil **shrink** pour donner à l’image-objet `Hippo` une taille similaire à celle de l’image-objet `Spaceship`.

![capture d'écran](images/invaders-hippo.png)

\--- /task \---

\--- task \---

Définissez le style de rotation de l’image-objet `Hippo` sur **gauche-droite**.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

Ajoutez du code pour cacher le lutin `Hippo` quand le jeu commence.

![hippo sprite](images/hippo-sprite.png)

```blocks3
Quand le drapeau vert est cliqué
cacher

```

\--- /task \---

\--- task \---

Ajoutez du code sur la scène pour créer un nouveau clone `Hippo` toutes les quelques secondes.

\--- hints \---

\--- hint \---

Lorsque le drapeau vert `est cliqué`{: class = "block3events"}, `plusieurs reprises`{: class = "block3control"} `wait`{: class = "block3control"} `entre 2 et 4 secondes`{: class = "block3operators"} puis `créez un clone de l'image-objet Hippo`{: class = "block3control"}.

\--- /indice \---

\--- hint \---

Voici les blocs que tu as besoin:

```blocks3
pour toujours
fin

créer le clone de (Hippo1 v)

(choisir aléatoire (2) à (4))

lorsque le drapeau cliqué

attendre () secs
```

\--- /hint \---

\--- hint \---

Voici à quoi ton code devrait ressembler:

![lutin de scène](images/stage-sprite.png)

```blocks3
quand le drapeau vert est cliqué
répéter indéfiniment
   attendre (choisir aléatoirement entre (2) et (4)) secondes
   créer un clone de (Hippo1 v)
terminer
```

\--- /hint \---

\--- /astuces \---

\--- /task \---

Chaque nouvel clone d´hippopotame doit apparaître à une position `x` aléatoire et chaque clone doit avoir une vitesse aléatoire.

\--- task \---

Créer une nouvelle variable appelée ` vitesse `{:class="block3variables"} pour le lutin ` hippo` uniquement.

[[[generic-scratch3-add-variable]]]

Une fois que tu auras fait cela correctement, la variable porte le nom du lutin à côté de lui, comme ceci :

![capture d'écran](images/invaders-var-test.png)

\--- /task \---

\--- task \---

Au démarrage de chaque clone de `Hippo`, choisis une vitesse aléatoire et le lieu de départ pour le clone. Puis affiche le clone a l’écran.

```blocks3
quand je commence comme un ensemble de
clone [vitesse v] (choisir au hasard 2 à 4)
aller à x: (sélection aléatoirement entre -(220) et (220)) y: (150)
montrer
```

\--- /task \---

\--- task \---

Testez ton code. Un nouveau hippo apparaît-il toutes les quelques secondes ?

\--- /task \---

Pour le moment, les hippos ne bougent pas.

\--- task \---

Chaque hippopotame doit se déplacer de manière aléatoire jusqu’à ce qu’il soit frappé par un éclair. Pour ce faire, attachez ce code sous les blocs déjà présents dans le script de code du sprite `Hippo`:

```blocks3
répéter jusqu'à <touching (lightning v) ?>
    mouvement (vitesse :: variables) étapes
    tourner à droite (choisir au hasard (-10) à (10)) degrés
    si sur le bord, rebond
fin
supprimer ce clone
```

\--- /task \---

\--- task \---

Testez votre code à nouveau. Vous devriez voir apparaître un nouveau clone hippo toutes les quelques secondes et chaque clone devrait se déplacer à une vitesse différente.

\--- no-print \---

![capture d'écran](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Maintenant, testez le canon laser du vaisseau spatial. Si un éclair frappe un hippopotame, l'hippopotame disparaît-il?

\--- /task \---