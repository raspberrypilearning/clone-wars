## Créer un vaisseau spatial

Commence par créer un vaisseau spatial capable de défendre la Terre!

\--- task \---

Ouvrez le projet de démarrage Scratch 'Clone wars'.

**En ligne:** ouvre le projet de démarrage à [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target="_ blank"}.

Si tu as un compte Scratch, tu peux en créer une copie en cliquant sur **Remix**.

**Hors ligne:** téléchargez le projet de démarrage à partir de [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go), puis ouvrez-le à l'aide de l'éditeur hors ligne.

Si tu dois télécharger et installer l'éditeur hors ligne Scratch, tu peux le trouver à [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

![projet de démarrage](images/starter-project.png)

\--- task \---

Ajoutez ce code à l’image-objet du vaisseau spatial pour le déplacer vers la gauche si vous appuyez sur la flèche <kbd>gauche</kbd>:

![lutin de roquette](images/rocket-sprite.png)

```blocks3
    quand le drapeau est cliqué
    répéter indéfiniment
    si <key (left arrow v) pressed?> alors changer par x (-4)
    stop tout
```

L'axe des x va du côté gauche de la scène au côté droit. Cela signifie que le vaisseau spatial se déplace vers la gauche lorsque vous soustrayez de la valeur de la position `x` du sprite du vaisseau spatial. Donc, ce bloc de code est la partie qui fait bouger votre vaisseau spatial vers la gauche:

```blocks3
changer x par (-4)
```

\--- /task \---

\--- task \---

Ajoutez du code supplémentaire dans le bloc `forever`{: class = "block3control"} pour que votre vaisseau spatial se déplace vers la droite si vous appuyez sur la touche <kbd>droite</kbd> flèche.

\--- hints \---

\--- hint \---

En soustrayant `4` de la position `x` du vaisseau spatial, il se déplaçait à gauche, alors comment pourriez-vous faire bouger le vaisseau spatial de `4` place?

\--- /hint \---

\--- hint \---

Vous avez besoin du même bloc de code, mais avec un numéro différent:

```blocks3
changer x par (4)
```

\--- /hint \---

\--- hint \---

Voici le code que vous devez ajouter ci-dessous l’autre code du bloc `forever`{: class = "block3control"}:

![lutin de roquette](images/rocket-sprite.png)

```blocks3
si <key (right arrow v) pressed?> alors
    change x de (4)
fin
```

\--- /hint \---

\--- /astuces \---

\--- /task \---

\--- task \---

Testez votre projet en cliquant sur le drapeau vert. Pouvez-vous appuyer sur les touches fléchées pour faire bouger votre vaisseau spatial à gauche et à droite?

\--- /task \---