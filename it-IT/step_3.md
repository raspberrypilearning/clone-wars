## Fulmini

Diamo all'astronave la possibilità di sparare fulmini!

+ Aggiungi lo sprite 'Fulmine' dalla libreria Scratch.  Quando la partita è iniziata, il fulmine sarà nascosto finché l'astronave spara i suoi cannoni laser. Lo spire deve essere molto più piccolo e a testa in giù. Aggiungi il seguente codice allo sprite 'Fulmine'.

	```blocks
		quando si clicca sulla bandiera verde
		nascondi
		porta dimensione al (25) %
		punta in direzione (-90 v)
	```


+ Aggiungi il seguente codice **all'Astronave** per creare un nuovo fulmine ogni volta che la barra spaziatrice è premuta.


	```blocks
		quando si clicca sulla bandiera verde
		per sempre
  			se <tasto [spazio v] premuto> allora
    			crea clone di [Fulmine v]
  			end
		end
	```

+ Ogni volta che viene creato un nuovo clone, dovrebbe iniziare nello stesso posto dell'astronave, e poi muoversi in alto dello schermo finché tocca il bordo. Aggiungi il seguente codice allo **sprite Fulmine**:

	```blocks
		quando vengo clonato
		raggiungi [Astronave v]
		mostra
		ripeti fino a quando <sta toccando [bordo v]>
  			cambia y di (10)
		end
		elimina questo clone
	```

Nota: Muoviamo il nuovo clone verso l'astronave mentre è ancora nascosto, dunque prima di mostrarlo. Così va meglio.

+ Prova il tuo fulmine, premendo la barra spaziatrice.

--- challenge ---

## Sfida: Aggiustare il fulmine 
Cosa succede se tieni la barra spaziatrice premuta? Puoi usare un blocco `attendi`{:class="blockcontrol"} per risolverlo?

--- /challenge ---