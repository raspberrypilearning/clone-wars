## Les Hippopotames de l'espace

Tu vas maintenant ajouter de nombreux hippopotames volants qui tentent de détruire ton vaisseau spatial.

--- task ---

Crée un nouveau sprite avec l'image 'Hippo1' dans la bibliothèque Scratch. Utilise l’outil **rétrécissement** pour donner au sprite `Hippo` une taille similaire à celle du sprite `Spaceship`.

![capture d'écran](images/invaders-hippo.png)

--- /task ---

--- task ---

Définis le style de rotation du sprite `Hippo` sur **gauche-droite**.

[[[generic-scratch3-sprite-rotation-style]]]

--- /task ---

--- task ---

Ajoute du code pour cacher le sprite `Hippo` quand le jeu commence.

![sprite hippopotame](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

--- task ---

Ajoute du code sur la scène pour créer un nouveau clone `Hippo` toutes les quelques secondes.

--- hints ---

--- hint ---

`Lorsque le drapeau vert est cliqué`{:class="block3events"}, continue à vérifier `répéter indéfiniment`{:class="block3control"} `si`{:class="block3control"} `la touche d'espacement est enfoncée`{:class="block3sensing"}, et dans ce cas , `créer un clone du sprite Hippo`{:class="block3control"}.

--- /hint ---

--- hint ---

Voici les blocs que tu as besoin :

```blocks3
forever
end

create clone of (Hippo1 v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

--- /hint ---

--- hint ---

Voici à quoi ton code devrait ressembler :

![sprite Scène](images/stage-sprite.png)

```blocks3
when flag clicked
forever
	wait (pick random (2) to (4)) secs
	create clone of (Hippo1 v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

Chaque nouveau clone d´hippopotame doit apparaître à une position `x` aléatoire et chaque clone doit avoir une vitesse aléatoire.

--- task ---

Créer une nouvelle variable appelée `vitesse`{:class="block3variables"} pour le sprite `hippo` uniquement.

[[[generic-scratch3-add-variable]]]

Une fois que tu auras fait cela correctement, la variable porte le nom du sprite à côté de lui, comme ceci :

![capture d'écran](images/invaders-var-test.png)

--- /task ---

--- task ---

Au démarrage de chaque clone de `Hippo`, choisis une vitesse aléatoire et le lieu de départ pour le clone. Puis affiche le clone a l’écran.

```blocks3
when I start as a clone
set [vitesse v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

--- /task ---

--- task ---

Teste ton code. Un nouveau hippopotame apparaît-il toutes les quelques secondes ?

--- /task ---

Pour le moment, les hippopotames ne bougent pas.

--- task ---

Chaque hippopotame doit se déplacer de manière aléatoire jusqu’à ce qu’il soit frappé par un éclair. Pour ce faire, attache ce code sous les blocs déjà présents dans le script de code du sprite `Hippo` :

```blocks3
repeat until <touching (lightning v) ?>
	move (vitesse :: variables) steps
	turn right (pick random (-10) to (10)) degrees
	if on edge, bounce
end
delete this clone
```	

--- /task ---

--- task ---

Teste ton code à nouveau. Tu devrais voir apparaître un nouveau clone hippopotame toutes les quelques secondes et chaque clone devrait se déplacer à une vitesse différente.

--- no-print ---

![capture d'écran](images/hippo-clones.gif)

--- /no-print ---

--- /task ---

--- task ---

Maintenant, teste le canon laser du vaisseau spatial. Si un éclair frappe un hippopotame, l'hippopotame disparaît-il ?

--- /task ---