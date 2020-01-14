## Муње

Сада ћеш свемирском броду дати могућност да испаљује муње!

\--- task \---

Додај лик `Муње` из библиотеке Скреча.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

When the game starts, the `Lightning` sprite should be hidden until the spaceship fires its laser cannons.

Додај овај код лику `Муње`:

![лик муње](images/lightning-sprite.png)

```blocks3
када је кликнуто на ⚑
сакриј
```

\--- /task \---

At the moment, the lightning bolt is really big compared to the spaceship!

\--- task \---

Below the code that the `Lightning` sprite already has, add some blocks to make the sprite smaller and to turn it upside down.

![лик муње](images/lightning-sprite.png)

```blocks3
нека величина буде (25) %
усмери се ка (-90)
```

Now it looks like it fires pointy end–first out of the spaceship.

\--- /task \---

\--- task \---

Add some new code to the `Spaceship` sprite to create a new clone of the lightning bolt if the <kbd>space</kbd> key is pressed.

\--- hints \---

\--- hint \---

`When the green flag is clicked`{:class="block3events"}, keep checking `forever`{:class="block3control"} `if`{:class="block3control"} the `space key is pressed`{:class="block3sensing"}, and in that case `create a clone of the Lightning`{:class="block3control"} sprite.

\--- /hint \---

\--- hint \---

Ево блокова кода који су ти потребни:

```blocks3
ако је <> онда
end

понављај заувек
end

направи дупликат од (Муња v)

<key (space v) pressed?>

када је кликнуто на ⚑
```

\--- /hint \---

\--- hint \---

Овако би требало да изгледа твој нови код:

![лик ракете](images/rocket-sprite.png)

```blocks3
када је кликнуто на ⚑
понављај заувек 
  ако је <key (space v) pressed?> онда 
    направи дупликат од (Муња v)
  end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Whenever the game creates a `Lightning` sprite clone, the clone should appear and then move upwards until it reaches the top of the Stage. Then the clone should disappear.

Add this code to the `Lightning` sprite so that clones of it move upwards until they touch the edge of the Stage, and then they get deleted.

![лик муње](images/lightning-sprite.png)

```blocks3
    када се појавим као умножак
иди до (Свемирски брод v)
прикажи
понављај до <touching (edge v) ?> 
  промени y за (10)
end
обриши овај умножак
```

\--- /task \---

\--- task \---

Press the <kbd>space</kbd> key to test whether the lightning bolt moves correctly.

\--- /task \---