## Créer un vaisseau spatial

Créons un vaisseau spatial qui défendra la Terre!

+ Démarrez un nouveau projet Scratch et supprimez le lutin de chat.

[[[generic-scratch-new-project]]]

+ Ajouter les ` étoiles ` en arrière plan et le lutin ` vaisseau spatial ` à votre projet.
    
    ![screenshot](images/invaders-sprites.png)

[[[generic-scratch-backdrop-from-library]]]

[[[generic-scratch-sprite-from-library]]]

+ Utilisez l'outil pour** rétrécir ** outil pour rendre votre ` vaisseau spatial ` un peu plus petit, et placez-le près du bas de l'écran.

+ Quand la** flèche de gauche ** est enfoncée, le vaisseau spatial devrait se déplacer vers la gauche. Ajoutez ce code pour que votre vaisseau spatial se déplace vers la gauche lorsque la** touche ** est pressée:

```blocks
    quand le drapeau est cliqué
    répéter indéfiniment
    si <key [left arrow v] pressed?> alors changer par x (-4)
    stop tout
```

L'axe des x va de gauche à droite sur la scène, donc si vous réduisez la position x de la navette spatiale , elle se déplacera plus vers la gauche. Ce code est la partie qui fait bouger votre vaisseau spatial vers la gauche:

```blocks
changer x par (-4)
```

+ Ajoutez un peu plus de code dans le {: class = "blockcontrol"} ` répéter indéfiniment ` pour que votre vaisseau spatial se déplace vers la droite lorsque le ** la flèche droite ** est enfoncée.

\--- astuces \--- \--- indice \--- En soustrayant ` 4 ` de la position du vaisseau spatial, il bouge a gauche, comment pourriez-vous le faire a la place bouger de ` 4 ` à droite ? \--- / hint \--- \--- indice \--- Vous devrez utiliser le même bloc, mais avec un nombre différent:

```blocks
changer x par (4)
```

\--- / hint \--- \--- indice \--- Voici le code que vous devrez ajouter sous l'autre code à l'intérieur de votre bloc {: class = "blockcontrol"}` répéter indéfiniment ` :

```blocks
si <flèche de droite v> pressé
alors changer x par (4)
stop tout 
```

\--- /hint \--- \--- /hints \---

+ Testez votre projet en cliquant sur le drapeau vert. Pouvez-vous déplacer votre vaisseau spatial à gauche et à droite avec les touches directionnelles?