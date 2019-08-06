## Fin du jeu

Quand un hippopotame touche votre vaisseau spatial, le vaisseau spatial devrait exploser!

\--- task \---

Sélectionnez le sprite `Spaceship` et renommez son costume 'normal'.

\--- /task \---

\--- task \---

Dessinez un autre costume de vaisseau spatial en explosion et appelez le nouveau costume «hit».

![capture d'écran](images/invaders-spaceship-costumes.png)

Si vous ne voulez pas dessiner l'explosion, vous pouvez sélectionner le costume 'Soleil' dans la bibliothèque Scratch, puis utiliser l'outil **Couleur** forme </strong> pour changer la couleur et le visage du costume.

![capture d'écran](images/invaders-sun.png)

\--- /task \---

\--- task \---

Ajoutez du code à votre sprite `Spaceship` pour qu'il affiche le costume "normal" au début du jeu et qu'il passe au costume "hit" lorsqu'il touche un hippopotame:

![lutin de roquette](images/rocket-sprite.png)

```blocks3
lorsque le drapeau a cliqué sur
passez de costume à (normal v)
attendez jusqu'à <touching (Hippo1 v)>?
costume de commutation à (hit v)
```

\--- /task \---

\--- task \---

Testez votre code. Faites en sorte que le vaisseau spatial entre en collision avec un hippopotame. Est-ce que le vaisseau spatial change en costume de hit?

\--- /task \---