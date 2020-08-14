## Crea una navicella spaziale

Creiamo una navicella spaziale che difenderà la Terra!

--- task ---

Apri il progetto per principianti 'Guerre dei Cloni'.

**Online:** apri il progetto iniziale su [scratch.mit.edu/projects/417839351](https://scratch.mit.edu/projects/417839351){:target="_blank"}.

Se hai un account su Scratch, puoi farne una copia cliccando su **Remix**.

**Offline:** scarica il progetto per principianti da [rpf.io/p/it-IT/clone-wars-go](http://rpf.io/p/it-IT/clone-wars-go), e poi aprilo con l'editor offline.

Se hai bisogno di scaricare ed installare l'editor Scratch offline, puoi trovarlo su [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

![progetto per principianti](images/starter-project.png)

--- task ---

Aggiuhngi questo codice allo sprite della navicella per far si che si muova verso sinistra quando la freccetta <kbd>sinistra</kbd> viene premuta:

![sprite razzo](images/rocket-sprite.png)

```blocks3
    when flag clicked
	forever
		if <key (left arrow v) pressed?> then
			change x by (-4)
		end
	end
```

L'asse x va da sinistra verso destra nella scena. Questo significa che la navicella si muoverà a sinistra quando si sottrarrà dal valore dello sprite della navicella il valore della posizione `x`. Quindi questo blocco di codice è la parte che permetterà alla navicella di spostarsi verso sinistra:

```blocks3
change x by (-4)
```

--- /task ---

--- task ---

Aggiungi ancora altro codice nel blocco `per sempre`{:class="block3control"} per far si che la navicella si muova a destra quando la freccetta <kbd>destra</kbd> verrà premuta.

--- hint ---

--- hint ---

Sottraendo `4` dalla posizione `x` della navicella questa si muoverà verso sinistra, invece come puoi far si che si muova a destra di `4`?

--- /hint ---

--- hint ---

Hai bisogno dello stesso blocco di codice, solo che dovrai cambiare numero:

```blocks3
change x by ( )
```

--- /hint ---

--- hint ---

Qui c'è il codice che dovrai inserire sotto l'altro codice nel blocco `per sempre`{:class="block3control"}:

![sprite razzo](images/rocket-sprite.png)

```blocks3
if <key (right arrow v) pressed?> then
	change x by (4)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Prova il tuo progetto facendo clic sulla bandierina verde. Riesci a muovere la navicella prememndo le frecce a sinistra e a destra?

--- /task ---