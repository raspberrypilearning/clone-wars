## Foudre

Maintenant, vous allez donner au vaisseau spatial la capacité de tirer des éclairs!

\--- task \---

Ajouter le lutin `Lightning `de la bibliothèque Scratch.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Lorsque le jeu commence, le sprite `Lightning` doit être caché jusqu'à ce que le vaisseau spatial tire ses canons laser.

Ajoutez ce code au sprite `Lightning`:

![sprite éclair](images/lightning-sprite.png)

```blocks3
Quand le drapeau vert est cliqué
cacher

```

\--- /task \---

Pour le moment, l'éclair est vraiment gros comparé au vaisseau spatial!

\--- task \---

Sous le code que l’image-objet `Lightning` a déjà, ajoutez des blocs pour la réduire et la retourner.

![sprite éclair](images/lightning-sprite.png)

```blocks3
définir la taille sur (25)%
point dans la direction (-90)
```

On dirait maintenant que ça tire au bout pointu - premier sorti du vaisseau spatial.

\--- /task \---

\--- task \---

Ajoutez un nouveau code au sprite `Spaceship` pour créer un nouveau clone de l'éclair si vous appuyez sur la touche <kbd>espace</kbd>.

\--- hints \---

\--- hint \---

`Lorsque le drapeau vert est cliqué`{: class = "block3events"}, continuez à vérifier `pour toujours`{: class = "block3control"} `si`{: class = "block3control"} la touche d'espacement `est enfoncée`{: class = "block3sensing"}, et dans ce cas , `créer un clone de la foudre`{: class = "block3control"} sprite.

\--- /hint \---

\--- hint \---

Voici les blocs que tu as besoin:

```blocks3
si <> puis


pour toujours


créer un clone de (Lightning v)

<key (space v) pressed?>

lorsque le drapeau est cliqué
```

\--- /hint \---

\--- hint \---

Voici à quoi devrait ressembler votre nouveau code:

![lutin de roquette](images/rocket-sprite.png)

```blocks3
lorsque l' indicateur cliqué
pour toujours
    si <key (space v) pressed?> puis
        créer clone de (foudre v)
    extrémité
extrémité
```

\--- /hint \---

\--- /astuces \---

\--- /task \---

\--- task \---

Chaque fois que le jeu crée un clone de sprite `Lightning` , le clone doit apparaître puis se déplacer vers le haut jusqu'à ce qu'il atteigne le haut de la scène. Ensuite, le clone devrait disparaître.

Ajoutez ce code au sprite `Lightning` pour que ses clones se déplacent vers le haut jusqu'à ce qu'ils touchent le bord de la scène, puis ils sont supprimés.

![sprite éclair](images/lightning-sprite.png)

```blocks3
    quand je commence en tant que clone
    aller à (Spaceship v)
    montrer
    répéter jusqu'à ce que <touching (edge v) ?>
        change y par (10)
    fin
    supprimer ce clone
```

\--- /task \---

\--- task \---

Appuyez sur la touche <kbd>espace</kbd> pour vérifier si l'éclair se déplace correctement.

\--- /task \---