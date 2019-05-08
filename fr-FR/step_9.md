## Chauve-souris de l'espace

To make your game a bit harder, you are going to create a bat that throws oranges at the spaceship.

![a bat throwing an orange at the spaceship](images/bat-oranges.png)

\--- task \---

Add a `Bat` sprite and set its rotation style to **left–right**.

\--- /task \---

\--- task \---

Make the `Bat` sprite `move`{:class="block3motion"} from left to right at the top of the Stage `forever`{:class="block3control"}.

![bat sprite](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

Remember to test your code.

\--- /task \---

If you look at the bat's costumes, you can see that it has four different ones:

![screenshot](images/invaders-bat-costume.png)

\--- task \---

Use the `next costume`{:class="block3looks"} block to make the bat flap its wings as it moves.

\--- astuces \---

\--- hint \---

After the bat has moved, it should show the `next costume`{:class="block3looks"} and then `wait`{:class="block3control"} for a short time.

\--- /indice \---

\--- hint \---

You need to add these blocks to you code:

```blocks3
wait (0.3) seconds

next costume
```

\--- /indice \---

\--- hint \--- You code should look like this:

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

\--- /indice \---

\--- /astuces \---

\--- /task \---

Maintenant, fait en sorte que la chauve-souris jette des oranges !

\--- task \---

Ajouter un lutin `Orange`de la bibliothèque Scratch.

![capture d'écran](images/invaders-orange.png)

\--- /task \---

\--- task \---

Ajoutez du code à ta chauve-souris pour que ` quand le drapeau est cliqué ` {: class = "block3events"}, le `lutin de la ` chauve-souris ` attend ` {: class = "block3control"} ` pour toujours ` {: class = "block3control"} pour une ` durée aléatoire ` {: class = "block3operators"} entre ` 5 et 10 ` {: class = "block3operators"} secondes puis ` crée un clone ` {: class = "block3control"} du lutin de ` l´orange `.

![lutin de chauve-souris](images/bat-sprite.png)

```blocks3
quand le drapeau vert est cliqué
répéter indéfiniment
   attendre (choisir aléatoirement entre (5) et (10)) secondes
   créer un clone de (Orange v)
terminer
```

\--- /task \---

\--- task \---

Ajoutez du code a au lutin `d’orange` pour faire chacun de ses clones, à partir du lutin de `chauve-souris` et descendre vers le bas de la scène.

![lutin d´orange](images/orange-sprite.png)

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

Ajoutez plus de code au lutin `d´orange` afin que lorsque un clone `d´orange` touche le lutin de `vaisseau spatial`, le clone disparaît également pour donner au joueur une chance de réinitialiser :

![lutin d´orange](images/orange-sprite.png)

```blocks3
    quand je reçois [touché v]
    effacer ce clone
```

\--- /task \---

\--- task \---

Modifier le code de votre lutin de `vaisseau spatial` afin que le lutin soit « touché » lorsqu’il touche un lutin `hippo` ou un lutin `orange` :

![lutin de roquette](images/rocket-sprite.png)

```blocks3
    patienter jusqu'à < <touching (Hippo1 v)?> or <touching (Orange v)?>>
```

\--- /task \---

\--- task \---

Testez ton jeu. Que se passe-t-il si le vaisseau spatial se fait frapper par une orange qui tombe ?

\--- /task \---