## Ippopotami spaziali

Ora aggiungerai un sacco di ippopotami volanti che cercano di distruggere la tua astronave.

\--- task \---

Crea un nuovo sprite con l'immagine 'Hippo1' nella collezione di Scratch. Usa lo strumento di **riduzione** per rendere l'`ippopotamo` di dimensioni simili alla `Navicella`.

![The Scratch stage with a starry background. A rocket sits in the middle at the bottom of the stage and a hippo sprite with wings is at the top.](images/invaders-hippo.png)

\--- /task \---

\--- task \---

Imposta la rotazione dello sprite dell'`ippopotamo` a **sinistra-destra**.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

Aggiungi del codice per nascondere lo sprite`ippopotamo` quando inizia il gioco.

![sprite ippopotamo](images/hippo-sprite.png)

```blocks3
quando si fa clic sulla bandiera verde
nascondi
```

\--- /task \---

\--- task \---

Aggiungi del codice alla scena per creare un nuovo clone di un `ippopotamo` ogni volta che passa qualche secondo.

\--- hint \---

\--- hint \---

Quando si fa clic sulla `bandiera verde`{:class="block3events"}, `ripetutamente` `aspetta`{:class="block3control"} `tra 2 e 4 secondi`{:class="block3operators"} e poi `crea un clone dello sprite dell'ippopotamo`{:class="block3control"}.

\--- /hint \---

\--- hint \---

Qui ci sono i blocchi di codice che ti serviranno:

```blocks3
per sempre
fine

crea clone di (Ippopotamo1 v)

(numero a caso tra (2) e (4))

quando si fa clic sulla bandiera
attendi () secondi
```

\--- /hint \---

\--- hint \---

Ecco come dovrebbe apparire il risultato:

![scena sprite](images/stage-sprite.png)

```blocks3
quando si fa clic sulla bandiera
per sempre
    attendi (scegli numero a caso tra (2) e (4)) secondi
    crea clone di (Ippopotamo1 v)
fine
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Ogni nuovo clone di ippopotamo dovrebbe apparire in modo casuale in una posizione ` x `, ed ogni clone dovrebbe avere una velocità casuale.

\--- task \---

Crea una nuova variabile chiamata `velocità`{: class = "block3variables"} che verrà usata solo dallo sprite dell'`ippopotamo`.

[[[generic-scratch3-add-variable]]]

Quando lo hai fatto correttamente, la variabile ha il nome dello sprite accanto ad esso, in questo modo:

![The variable sprite that reads "Hippo1: speed 0"](images/invaders-var-test.png)

\--- /task \---

\--- task \---

Quando ogni `Ippopotamo` inizia a clonarsi, scegli una velocità casuale e il suo punto di partenza. Quindi fai apparire il clone sullo schermo.

```blocks3
quando inizio come clone
imposta [velocità v] a (seleziona numero a caso tra (2) e (4))
vai a x: (seleziona numero a caso (-220) a (220)) y: (150)
mostra
```

\--- /task \---

\--- task \---

Prova il codice. Appare un nuovo ippopotamo ogni volta che passa qualche secondo?

\--- /task \---

Al momento gli ippopotami non si muovono.

\--- task \---

Ogni ippopotamo dovrebbe muoversi in modo casuale finché non verrà colpito da un fulmine. Per far si che questo accada, collega questo codice sotto ai blocchi già esistenti che si trovano già nello script di codice dello sprite dell'`ippopotamo`:

```blocks3
ripetere fino a <touching (lightning v) ?>
    spostare (velocità :: variabili) passi
    girare a destra (selezionare casuale (da -10) a (10)) gradi
    se sul bordo, rimbalzare
fine
eliminare questo clone
```

\--- /task \---

\--- task \---

Riprova il codice. Adesso dovresti vedere un nuovo clone di ippopotamo che appare ogni pochi secondi, e ogni clone dovrebbe muoversi con una velocità diversa.

\--- no-print \---

![Animation of the Hippo sprite flying around, two clones are created and move independently.](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Adesso proviamo i cannoni laser dell'astronave. Se un fulmine colpisce un ippopotamo, lui scompare?

\--- /task \---