## Créer un vaisseau spatial

Commence par créer un vaisseau spatial capable de défendre la Terre !

\--- task \---

Ouvre le projet de démarrage Scratch 'Clone wars'.

**En ligne:** ouvre le projet de démarrage à [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target="_ blank"}.

Si tu as un compte Scratch, tu peux en créer une copie en cliquant sur **Remix**.

**Hors ligne:** télécharge le projet de démarrage à partir de [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go), puis ouvre-le à l'aide de l'éditeur hors ligne.

Si tu dois télécharger et installer l'éditeur hors ligne Scratch, tu peux le trouver à [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

![projet de démarrage](images/starter-project.png)

\--- task \---

Ajoute ce code au sprite du vaisseau spatial pour le déplacer vers la gauche si tu appuies sur la flèche <kbd>gauche</kbd> :

![sprite de roquette](images/rocket-sprite.png)

```blocks3
    quand le drapeau est cliqué
    répéter indéfiniment
        si <key (left arrow v) pressed?> alors
            ajouter (-4) à x
        fin
    fin
```

L'axe des x va du côté gauche de la scène au côté droit. Cela signifie que le vaisseau spatial se déplace vers la gauche lorsque tu soustrais de la valeur de la position `x` du sprite du vaisseau spatial. Donc, ce bloc de code est la partie qui fait bouger ton vaisseau spatial vers la gauche :

```blocks3
ajouter (-4) à x
```

\--- /task \---

\--- task \---

Ajoute du code supplémentaire dans le bloc `répéter indéfiniment`{:class="block3control"} pour que ton vaisseau spatial se déplace vers la droite si tu appuies sur la touche fléchée <kbd>droite</kbd>.

\--- hints \---

\--- hint \---

En soustrayant `4` de la position `x` du vaisseau spatial, il se déplaçait à gauche, alors comment pourrais-tu faire bouger le vaisseau spatial de `4` à la place ?

\--- /hint \---

\--- hint \---

Tu as besoin du même bloc de code, mais avec un numéro différent:

```blocks3
ajouter ( ) à x
```

\--- /hint \---

\--- hint \---

Voici le code que tu dois ajouter sous l’autre code du bloc `répéter indéfiniment`{:class="block3control"}:

![sprite de roquette](images/rocket-sprite.png)

```blocks3
si <key (right arrow v) pressed?> alors
    ajouter (4) à x
fin
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Teste ton projet en cliquant sur le drapeau vert. Peux-tu appuyer sur les touches fléchées pour faire bouger ton vaisseau spatial à gauche et à droite ?

\--- /task \---