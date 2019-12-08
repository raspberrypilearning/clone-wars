## Explosion du vaisseau spatial

Quand un hippopotame touche ton vaisseau spatial, le vaisseau spatial devrait exploser !

\--- task \---

Sélectionne le sprite `Spaceship` et renomme son costume 'normal'.

\--- /task \---

\--- task \---

Dessine un autre costume de vaisseau spatial en explosion et appelle le nouveau costume "hit".

![capture d'écran](images/invaders-spaceship-costumes.png)

Si tu ne veux pas dessiner l'explosion, tu peux sélectionner le costume "Sun" à partir de la bibliothèque Scratch, puis utiliser **l'outil Couleur** pour changer la couleur et l'apparence du costume.

![capture d'écran](images/invaders-sun.png)

\--- /task \---

\--- task \---

Ajoute du code à ton sprite `Spaceship` pour qu'il affiche le costume "normal" au début du jeu et qu'il passe au costume "hit" lorsqu'il touche un hippopotame :

![sprite de roquette](images/rocket-sprite.png)

```blocks3
quand le drapeau est cliqué
basculer sur le costume (normal v)
attendre jusqu'à ce que <touching (Hippo1 v)>?
basculer sur le costume (hit v)
```

\--- /task \---

\--- task \---

Teste ton code. Fais en sorte que le vaisseau spatial entre en collision avec un hippopotame. Est-ce que le vaisseau spatial change en costume de hit ?

\--- /task \---