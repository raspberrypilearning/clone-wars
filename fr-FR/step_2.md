## Fabrication d'un vaisseau spatial

Créons un vaisseau spatial qui défendra la Terre!

+ Commencez un nouveau projet Scratch et supprimez le lutin de chat pour que votre projet soit vide. Vous pouvez trouver l'éditeur de scratch en ligne à <a href="http://jumpto.cc/scratch-new">jumpto.cc/scratch-new</a>.

+ Ajoutez le fond 'stars' et le lutin 'Spaceship' à votre projet. Faites rétrécir le vaisseau spatial et déplacez-le près du bas de l'écran.

	![screenshot](images/invaders-sprites.png)

+ Ajoutez le code pour déplacer votre vaisseau spatial à gauche lorsque la touche de direction gauche est appuyée. Vous devrez utiliser ces blocs :

	```blocks
		quand le drapeau vert pressé
		répéter indéfiniment
   			si <touche [flèche gauche v] pressée?> alors
      			ajouter (-4) à x
   			fin
		fin
	```

+ Ajoutez le code pour déplacer votre vaisseau spatial à droite quand la touche de direction droite est appuyée.

+ Testez votre projet de voir si vous pouvez contrôler votre vaisseau spatial avec les touches de direction.
