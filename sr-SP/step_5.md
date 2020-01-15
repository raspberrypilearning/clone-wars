## Свемирски нилски коњи

Сада ћеш додати пуно летећих нилских коња, који ће покушати да униште твој свемирски брод.

\--- task \---

Create a new sprite with the 'Hippo1' image in the Scratch library. Use the **shrink** tool to make the `Hippo` sprite a similar size to the `Spaceship` sprite.

![снимак екрана](images/invaders-hippo.png)

\--- /task \---

\--- task \---

Постави ротацију `Нилског коња` на **лево-десно**.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

Add some code to hide the `Hippo` sprite when the game starts.

![лик нилског коња](images/hippo-sprite.png)

```blocks3
када је кликнуто на ⚑
сакриј
```

\--- /task \---

\--- task \---

Add some code to the Stage to create a new `Hippo` clone every few seconds.

\--- hints \---

\--- hint \---

Када је `кликнуто на зелену заставицу`{:class="block3events"}, `понављај заувек`{:class="block3control"} `чекај`{:class="block3control"} `између 2 и 4 секунде`{:class="block3operators"}, а затим `направи дупликат Нилског коња`{:class="block3control"}.

\--- /hint \---

\--- hint \---

Ево блокова кода који су ти потребни:

```blocks3
понављај заувек
end

направи дупликат од (Нилски коњ1 v)

(случајан број од (2) до (4))

када је кликнуто на ⚑

чекај () секунду
```

\--- /hint \---

\--- hint \---

Овако би требао да изгледа твој код:

![лик позорнице](images/stage-sprite.png)

```blocks3
када је кликнуто на ⚑
понављај заувек 
  чекај (случајан број од (2) до (4)) секунду
  направи дупликат од (Нилски коњ1 v)
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

![снимак екрана](images/invaders-var-test.png)

\--- /task \---

\--- task \---

When each `Hippo` clone starts, pick a random speed and starting place for it. Then show the clone on the screen.

```blocks3
када се појавим као умножак
нека [брзина v] буде (случајан број од (2) до (4))
иди до x: (случајан број од (-220) до (220)) y: (150)
прикажи
```

\--- /task \---

\--- task \---

Test your code. Does a new hippo appear every few seconds?

\--- /task \---

At the moment the hippos don't move.

\--- task \---

Each hippo should move around randomly until it gets hit by a lightning bolt. To make that happen, attach this code below the blocks that are already in the `Hippo` sprite's code script:

```blocks3
понављај до <touching (lightning v) ?> 
  иди (брзина :: variables) корака
  окрет ↻ за (случајан број од (-10) до (10)) степени
  ако си на рубу, окрени се
end
обриши овај умножак
```

\--- /task \---

\--- task \---

Test your code again. You should see a new hippo clone appear every few seconds, and each clone should move at a different speed.

\--- no-print \---

![снимак екрана](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Now test the spaceship's laser cannon. If a lightning bolt hits a hippo, does the hippo vanish?

\--- /task \---