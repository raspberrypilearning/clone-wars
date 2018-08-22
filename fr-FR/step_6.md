## L'explosion du vaisseau

Quand un hippopotame touche votre vaisseau spatial, il devrait exploser !

+ Sélectionnez le lutin `vaisseau spatial` et renommez le costume « normal ».

+ Dessinez un autre costume pour le vaisseau spatial qui explose et appelez-le «touché».

![capture d'écran](images/invaders-spaceship-costumes.png)

Ou, si vous ne voulez pas attirer l’explosion, vous pourriez choisir le costume du « Sun » de la bibliothèque de Scratch et utiliser ** l’outil de couleur** pour changer sa couleur et enlever le visage.

![capture d'écran](images/invaders-sun.png)

+ Ajoutez du code à votre ` Spaceship ` sprite pour qu'il commence par afficher le costume normal, mais quand il touche un hippopotame volant, il passe au costume "touché":

```blocks
lorsque le drapeau vert est cliqué 
changez de costume pour [normal v]
attendez jusqu'à <touching [Hippo1 v]>?
changer de costume pour [touché v]
```

+ Testez votre code en jouant le jeu et entrer en collision avec un hippopotame. Est-ce que le vaisseau spatial change pour le costume « frappé » ?