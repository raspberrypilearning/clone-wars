## Chauve-souris de l'espace

Pour rendre votre jeu un peu plus difficile, tu vas créer une chauve-souris qui jette des oranges sur le vaisseau spatial.

![une chauve-souris jetant une orange sur le vaisseau spatial](images/bat-oranges.png)

\--- task \---

Ajoute une image-objet `Bat` et définis son style de rotation sur **gauche-droite**.

\--- /task \---

\--- task \---

Fais `move`{: class = "block3motion"} le sprite`Bat` de gauche à droite en haut de la scène `pour toujours`{: class = "block3control"}.

![sprite de chauve-souris](images/bat-sprite.png)

```blocks3
lorsque le drapeau est cliqué sur
définissez la taille sur (50)%
pour toujours
    déplacer (10) étapes
    si sur le bord, rebondissez
fin
```

N'oublie pas de tester ton code.

\--- /task \---

Si tu regardes les costumes de la chauve-souris, tu peux voir qu'il en a quatre différents:

![capture d'écran](images/invaders-bat-costume.png)

\--- task \---

Utilisez le `suivant costume`{: class = « block3looks »} bloc pour faire le rabat bat ses ailes en mouvement.

\--- hints \---

\--- hint \---

Une fois que la chauve-souris a été déplacée, le costume suivant `devrait apparaître:`{: class = "block3looks"}, puis `attendez`{: class = "block3control"} pendant un court instant.

\--- /hint \---

\--- hint \---

Tu dois ajouter ces blocs à ton code:

```blocks3
attendre (0.3) secondes

costume suivant
```

\--- /hint \---

\--- Indice \--- Votre code devrait ressembler à ceci:

```blocks3
quand le drapeau cliqué sur
taille définie à (50) %
pour toujours
déplacer (10) pas
si sur le bord, rebondissez

+ prochain costume
+ attendre (0.3) secondes
fin
```

\--- /hint \---

\--- /astuces \---

\--- /task \---

Maintenant, fais en sorte que la chauve-souris jette des oranges !

\--- task \---

Ajouter un sprite `Orange`de la bibliothèque Scratch.

![capture d'écran](images/invaders-orange.png)

\--- /task \---

\--- task \---

Ajoute du code à ta chauve-souris pour que ` quand le drapeau est cliqué ` {: class = "block3events"}, le `sprite de la ` chauve-souris ` attend ` {: class = "block3control"} ` pour toujours ` {: class = "block3control"} pour une ` durée aléatoire ` {: class = "block3operators"} entre ` 5 et 10 ` {: class = "block3operators"} secondes puis ` crée un clone ` {: class = "block3control"} du sprite de ` l´orange `.

![sprite de chauve-souris](images/bat-sprite.png)

```blocks3
quand le drapeau vert est cliqué
répéter indéfiniment
   attendre (choisir aléatoirement entre (5) et (10)) secondes
   créer un clone de (Orange v)
terminer
```

\--- /task \---

\--- task \---

Ajoute du code a au sprite `d’orange` pour faire tomber chacun de ses clones, à partir du sprite de `chauve-souris` et descendre vers le bas de la scène.

![sprite d´orange](images/orange-sprite.png)

```blocks3
    quand le drapeau cliqué
    cacher

    quand je commence comme clone
    aller à (Chauve-souris v)
    montrer
    répéter jusqu'à <toucher (bord v)?
        changer y par (-4)
    fin
    supprimer ce clone
```

\--- /task \---

\--- task \---

Ajoute plus de code au sprite `d´orange` afin que lorsque un clone `d´orange` touche le sprite `vaisseau spatial`, le clone disparaît également pour donner au joueur une chance de réinitialiser :

![sprite d´orange](images/orange-sprite.png)

```blocks3
    quand je reçois [touché v]
    effacer ce clone
```

\--- /task \---

\--- task \---

Modifie le code de ton sprite `vaisseau spatial` afin que le sprite soit « touché » lorsqu’il touche un sprite `hippo` ou un sprite `orange` :

![sprite de roquette](images/rocket-sprite.png)

```blocks3
    patienter jusqu'à < <touching (Hippo1 v)?> or <touching (Orange v)?>>
```

\--- /task \---

\--- task \---

Teste ton jeu. Que se passe-t-il si le vaisseau spatial se fait frapper par une orange qui tombe ?

\--- /task \---