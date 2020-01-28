## Pipistrelli spaziali

Per rendere il tuo gioco un po' più difficile, creerai un pipistrello che lancia arance sulla navicella.

![un pipistrello che lancia un'arancia all'astronave](images/bat-oranges.png)

\--- task \---

Aggiungi uno sprite `Pipistrello` e imposta la sua rotazione su **sinistra-destra**.

\--- /task \---

\--- task \---

Rendi lo sprite `Pipistrello` `movimentato`{:class="block3motion"} da sinistra a destra nella parte superiore dello Stage `per sempre`{:class="block3control"}.

![sprite pipistrello](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

Ricorda di provare il tuo codice.

\--- /task \---

Se guardi i costumi del pipistrello, puoi vedere che ne ha quattro diversi:

![screenshot](images/invaders-bat-costume.png)

\--- task \---

Usa il blocco `prossimo costumee`{:class="block3looks"} per far si che batti le ali quando si muove.

\--- hint \---

\--- hint \---

Dopo che il pipistrello è stato spostato, dovrebbe mostrare il `costume successivo`{:class="block3look"} e poi `attendere`{:class="block3control"} per un breve periodo.

\--- /hint \---

\--- hint \---

Devi aggiungere questi blocchi al tuo codice:

```blocks3
wait (0.3) seconds

next costume
```

\--- /hint \---

\--- hint \---

Il tuo codice dovrebbe assomigliare a questo:

```blocks3
when flag clicked
set size to (50) %
forever
move (10) steps
if on edge, bounce

+ next costume
+ wait (0.3) seconds
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Ora fai sì che il pipistrello lanci arance!

\--- task \---

Aggiungere lo sprite `Arancia` dalla libreria di Scratch.

![schermata](images/invaders-orange.png)

\--- /task \---

\--- task \---

Aggiungi del codice al tuo pipistrello in modo che `quando si fa clic sulla bandierina`{:class = "block3events"}, lo sprite del `Pipistrello` `attenda`{: class = "block3control"} ` per sempre `{: class = "block3control"} per un `casuale` {: class = "block3operators"} intervallo di tempo `da 5 a 10` {: class = "block3operators"} secondi e poi ` crea un clone ` {: class = "block3control"} dello sprite dell'`Arancia`.

![sprite pipistrello](images/bat-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (5) to (10)) secs
    create clone of (Orange v)
end
```

\--- /task \---

\--- task \---

Aggiungi codice all'`Arancia` per far cadere ogni clone, partendo dallo sprite del `Pipistrello` e fallo cadere verso il fondo dello Stage.

![sprite arancia](images/orange-sprite.png)

```blocks3
    when flag clicked
    hide

    when I start as a clone
    go to (Bat v)
    show
    repeat until <touching (edge v)?
        change y by (-4)
    end
    delete this clone
```

\--- /task \---

\--- task \---

Aggiungi altro codice allo sprite dell'`arancia` in modo che quando un suo clone colpisca lo sprite della `navicella`, anche il clone scompaia così da dare al giocatore la possibilità di ricominciare:

![sprite arancia](images/orange-sprite.png)

```blocks3
    when I receive [hit v]
    delete this clone
```

\--- /task \---

\--- task \---

Modifica il codice dello sprite della `navicella` in modo che sia "colpito" quando tocca lo sprite di un `Ippopotamo` o uno sprite dell'`Arancia`:

![sprite razzo](images/rocket-sprite.png)

```blocks3
    wait until < <touching (Hippo1 v)?> or <touching (Orange v)?>>
```

\--- /task \---

\--- task \---

Prova il tuo gioco. Cosa succede se l'astronave viene colpita da un arancia in caduta?

\--- /task \---