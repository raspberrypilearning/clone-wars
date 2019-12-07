## Éclairs

Maintenant, tu vas donner au vaisseau spatial la capacité de tirer des éclairs!

\--- task \---

Ajouter le sprite `Lightning`de la bibliothèque Scratch.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Lorsque le jeu commence, le sprite `Lightning` doit être caché jusqu'à ce que le vaisseau spatial tire ses canons laser.

Ajoute ce code au sprite `Lightning`:

![sprite éclair](images/lightning-sprite.png)

```blocks3
Quand le drapeau vert est cliqué
cacher

```

\--- /task \---

Pour le moment, l'éclair est vraiment gros comparé au vaisseau spatial !

\--- task \---

Sous le code que le sprite `Lightning` a déjà, ajoute des blocs pour le réduire et le retourner.

![sprite éclair](images/lightning-sprite.png)

```blocks3
mettre la taille à (25)% de la taille initiale
s'orienter à (-90)
```

Maintenant, on dirait qu'il tire la fin pointue - d'abord hors du vaisseau spatial.

\--- /task \---

\--- task \---

Ajoute un nouveau code au sprite `Spaceship` pour créer un nouveau clone de l'éclair si tu appuies sur la touche <kbd>espace</kbd>.

\--- hints \---

\--- hint \---

`Lorsque le drapeau vert est cliqué`{:class="block3events"}, continue à vérifier `répéter indéfiniment`{:class="block3control"} `si`{:class="block3control"} ` la touche d'espacement est enfoncée`{:class="block3sensing"}, et dans ce cas , `créer un clone du sprite de l'éclair `{:class="block3control"}.

\--- /hint \---

\--- hint \---

Voici les blocs que tu as besoin:

```blocks3
si <> alors
fin

répéter indéfiniment
fin

créer un clone de (Lightning v)

<key (space v) pressed?>

quand le drapeau est cliqué
```

\--- /hint \---

\--- hint \---

Voici à quoi devrait ressembler ton nouveau code:

![sprite de roquette](images/rocket-sprite.png)

```blocks3
quand le drapeau est cliqué
    répéter indéfiniment
    si <key (space v) pressed?> alors
      créer un clone de (Lightning v)
    fin 
fin
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

À chaque fois que le jeu crée un clone de sprite `Lightning`, le clone devrait apparaître et se déplacer vers le haut jusqu'à ce qu'il atteigne le sommet de la scène. Le clone devrait alors disparaître.

Ajoute ce code au sprite `Lightning` pour que ses clones se déplacent vers le haut jusqu'à ce qu'ils touchent le bord de la scène, puis ils sont supprimés.

![sprite éclair](images/lightning-sprite.png)

```blocks3
    quand je commence comme un clone
    aller à (Spaceship v)
    montrer
    répéter jusqu'à ce que <touching (edge v) ?>
        ajouter (10) à y
    fin
    supprimer ce clone
```

\--- /task \---

\--- task \---

Appuie sur la touche <kbd>espace</kbd> pour vérifier si l'éclair se déplace correctement.

\--- /task \---