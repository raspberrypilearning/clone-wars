## Fulmini

Ora permetterai all'astronave di sparare fulmini!

--- task ---

Aggiungere lo sprite `Lightning` (Fulmine) dalla raccolta Scratch.

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

All'avvio del gioco, lo sprite `Fulmine` dovrebbe essere nascosto fino a quando l'astronave non li spara dai cannoni laser.

Aggiungi questo codice allo sprite `Fulmine`:

![sprite fulmine](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

Al momento, il fulmine è davvero grande rispetto alla navicella!

--- task ---

Sotto il codice che lo sprite `Fulmine` ha già, aggiungi alcuni blocchi per renderlo più piccolo e per farlo anche capovolgere.

![sprite fulmine](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

Ora sembra che spari prima la punta della navicella spaziale.

--- /task ---

--- task ---

Aggiungi un po' di codice nuovo allo sprite dell'`Astronave` per creare un nuovo clone del fulmine se si preme la <kbd>barra spaziatrice</kbd>.

--- hint ---

--- hint ---

`Quando si fa clic sulla bandiera verde`{:class="block3events"}, continua a guardare `per sempre`{:class="block3control"} `se`{:class="block3control"} la `barra spaziatrice viene premuta`{:class="block3sensing"}, ed in quel caso `crea un clone dello sprite Fulmine`{:class="block3control"}.

--- /hint ---

--- hint ---

Qui ci sono i blocchi di codice che ti serviranno:

```blocks3
if <> then
end

forever
end

create clone of (Fulmine v)

<key (space v) pressed?>

when flag clicked
```

--- /hint ---

--- hint ---

Ecco come dovrebbe apparire il tuo nuovo codice:

![sprite razzo](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
	if <key (space v) pressed?> then
		create clone of (Fulmine v)
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Ogni volta che il gioco crea un clone dello sprite `Fulmine`, lo dovrebbe far apparire e quindi muovere verso l'alto fino a raggiungere la parte alta della scena. Infine il clone dovrebbe scomparire.

Aggiungi questo codice allo sprite del `Fulmine` in modo che i suoi cloni si spostino verso l'alto fino a che non toccano il bordo della scena, e poi vengono eliminati.

![sprite fulmine](images/lightning-sprite.png)

```blocks3
    when I start as a clone
	go to (Astronave v)
    show
	repeat until <touching (edge v) ?>
		change y by (10)
	end
	delete this clone
```

--- /task ---

--- task ---

Premi la <kbd>barra spaziatrice</kbd> per verificare se il fulmine si muove correttamente.

--- /task ---