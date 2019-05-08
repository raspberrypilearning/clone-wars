## Une chauve-souris !

Now you're going to add lots of flying hippos that try to destroy your spaceship.

\--- task \---

Create a new sprite with the 'Hippo1' image in the Scratch library. Use the **shrink** tool to make the `Hippo` sprite a similar size to the `Spaceship` sprite.

![capture d'écran](images/invaders-hippo.png)

\--- /task \---

\--- task \---

Set the `Hippo` sprite's rotation style to **left-right**.

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

Add some code to the Stage to create a new `Hippo` clone every few seconds.

\--- astuces \---

\--- hint \---

When the `green flag is clicked`{:class="block3events"}, `repeatedly`{:class="block3control"} `wait`{:class="block3control"} `between 2 and 4 seconds`{:class="block3operators"} and then `create a clone of the Hippo sprite`{:class="block3control"}.

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

\--- /indice \---

\--- hint \---

C’est ce que ton code devrait ressembler :

![lutin de scène](images/stage-sprite.png)

```blocks3
quand le drapeau vert est cliqué
répéter indéfiniment
   attendre (choisir aléatoirement entre (2) et (4)) secondes
   créer un clone de (Hippo1 v)
terminer
```

\--- /indice \---

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

Each hippo should move around randomly until it gets hit by a lightning bolt. To make that happen, attach this code below the blocks that are already in the `Hippo` sprite's code script:

```blocks3
repeat until <touching (lightning v) ?>
    move (speed :: variables) steps
    turn right (pick random (-10) to (10)) degrees
    if on edge, bounce
end
delete this clone
```

\--- /task \---

\--- task \---

Test your code again. You should see a new hippo clone appear every few seconds, and each clone should move at a different speed.

\--- no-print \---

![capture d'écran](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Now test the spaceship's laser cannon. If a lightning bolt hits a hippo, does the hippo vanish?

\--- /task \---