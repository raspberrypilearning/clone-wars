## Ippopotami spaziali

Ora aggiungerai un sacco di ippopotami volanti che cercano di distruggere la tua astronave.

\--- task \---

Crea un nuovo sprite con l'immagine 'Hippo1' nella collezione di Scratch. Usa lo strumento di **riduzione** per rendere l'`ippopotamo` di dimensioni simili alla `Navicella`.

![schermata](images/invaders-hippo.png)

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
when flag clicked
forever
    wait (pick random (2) to (4)) secs
    create clone of (Hippo1 v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Each new hippo clone should appear at a random `x` position, and every clone should have a random speed.

\--- task \---

Create a new variable called `speed`{:class="block3variables"} that is for the `Hippo` sprite only.

[[[generic-scratch3-add-variable]]]

When you've done this correctly, the variable has the name of the sprite next to it, like this:

![screenshot](images/invaders-var-test.png)

\--- /task \---

\--- task \---

When each `Hippo` clone starts, pick a random speed and starting place for it. Then show the clone on the screen.

```blocks3
when I start as a clone
set [speed v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

\--- /task \---

\--- task \---

Test your code. Does a new hippo appear every few seconds?

\--- /task \---

At the moment the hippos don't move.

\--- task \---

Each hippo should move around randomly until it gets hit by a lightning bolt. To make that happen, attach this code below the blocks that are already in the `Hippo` sprite's code script:

```blocks3
repeat until <touching (lightning v) ?>
    move (speed :: variables) steps
    turn right (pick random (-10) to (10)) degrees
    if on edge, bounce
end
delete this clone
```

\--- /task \---

\--- task \---

Test your code again. You should see a new hippo clone appear every few seconds, and each clone should move at a different speed.

\--- no-print \---

![screenshot](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Now test the spaceship's laser cannon. If a lightning bolt hits a hippo, does the hippo vanish?

\--- /task \---