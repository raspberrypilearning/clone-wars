## Fulmini

Ora permetterai all'astronave di sparare fulmini!

\--- task \---

Aggiungere lo sprite `Fulmine` dalla raccolta Scratch.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

All'avvio del gioco, lo sprite ` Fulmine ` dovrebbe essere nascosto fino a quando l'astronave non li spara dai cannoni laser.

Aggiungi questo codice allo sprite `Fulmine`:

![sprite fulmine](images/lightning-sprite.png)

```blocks3
quando si fa clic sulla bandiera verde
nascondi
```

\--- /task \---

Al momento, il fulmine è davvero grande rispetto alla navicella!

\--- task \---

Sotto il codice che lo sprite `Fulmine` ha già, aggiungi alcuni blocchi per renderlo più piccolo e per farlo anche capovolgere.

![sprite fulmine](images/lightning-sprite.png)

```blocks3
imposta la dimensione a (25) %
punta in direzione (-90)
```

Ora sembra che spari prima la punta della navicella spaziale.

\--- /task \---

\--- task \---

Aggiungi un po' di codice nuovo allo sprite dell'`Astronave` per creare un nuovo clone del fulmine se si preme la <kbd>barra spaziatrice</kbd>.

\--- hint \---

\--- hint \---

`When the green flag is clicked`{:class="block3events"}, keep checking `forever`{:class="block3control"} `if`{:class="block3control"} the `space key is pressed`{:class="block3sensing"}, and in that case `create a clone of the Lightning`{:class="block3control"} sprite.

\--- /hint \---

\--- hint \---

Here are the blocks you need:

```blocks3
if <> then
end

forever
end

create clone of (Lightning v)

<key (space v) pressed?>

when flag clicked
```

\--- /hint \---

\--- hint \---

Here is what your new code should look like:

![rocket sprite](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
    if <key (space v) pressed?> then
        create clone of (Lightning v)
    end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Whenever the game creates a `Lightning` sprite clone, the clone should appear and then move upwards until it reaches the top of the Stage. Then the clone should disappear.

Add this code to the `Lightning` sprite so that clones of it move upwards until they touch the edge of the Stage, and then they get deleted.

![lightning sprite](images/lightning-sprite.png)

```blocks3
    when I start as a clone
    go to (Spaceship v)
    show
    repeat until <touching (edge v) ?>
        change y by (10)
    end
    delete this clone
```

\--- /task \---

\--- task \---

Press the <kbd>space</kbd> key to test whether the lightning bolt moves correctly.

\--- /task \---