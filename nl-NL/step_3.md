## Bliksemschichten

Nu ga je het ruimteschip de mogelijkheid geven om bliksemschichten af te vuren!

\--- task \---

Voeg de `Lightning ` sprite toe uit de Scratch-bibliotheek.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Wanneer het spel begint, moeten de `Lightning` sprites verborgen worden totdat het spaceship zijn laser kanon afschiet.

Voeg deze code toe aan de `Lightning` sprite:

![lightning sprite](images/lightning-sprite.png)

```blocks3
wanneer groene vlag wordt aangeklikt 
 verdwijn
```

\--- /task \---

Op dit moment is de bliksemschicht echt groot in vergelijking met het ruimteschip!

\--- task \---

Onder de code die `Lightning` sprite al heeft, voeg je enkele blokken toe om de sprite kleiner te maken en om deze om te draaien.

![lightning sprite](images/lightning-sprite.png)

```blocks3
maak grootte (25) %
richt naar (-90) graden
```

Nu lijkt het erop dat de punt het eerst uit het ruimteschip wordt geschoten.

\--- /task \---

\--- task \---

Add some new code to the `Spaceship` sprite to create a new clone of the lightning bolt if the <kbd>space</kbd> key is pressed.

\--- hints \---

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