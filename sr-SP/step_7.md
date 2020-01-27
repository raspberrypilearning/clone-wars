## Нилски коњи који нестају

Када свемирски брод експлодира, сви нилски коњи би требали да нестану, тако да се играчи могу опоравити.

\--- task \---

Add code to the spaceship sprite to make it `broadcast`{:class="block3events"} the message "hit" when the `spaceship touches a hippo`{:class="block3sensing"}.

![лик ракете](images/rocket-sprite.png)

```blocks3
када је кликнуто на ⚑
замени костим са (нормалан v)
чекај док не <touching (Hippo1 v)>?
замени костим са (ударац v)

+ разгласи (hit v)
```

\--- /task \---

\--- task \---

All of the `Hippo` sprite clones will receive the "hit" message, and you can instruct them to disappear when the spaceship is hit by adding this code to the `Hippo` sprite:

![лик нилског коња](images/hippo-sprite.png)

```blocks3
када примим [ударац v]
обриши овај умножак
```

\--- /task \---

\--- task \---

Да провериш исправност новог кода, кликни на зелену заставицу и судари свемирски брод са нилским коњем.

![снимак екрана](images/invaders-hippo-collide.png)

\--- /task \---

Након што свемирски брод експлодира, нови клонови `Нилског коња` се појављују, али је свемирски брод још увек уништен! Свемирски брод мора да се ресетује након што је погођен.

\--- task \---

Add a `wait`{:class="block3control"} block at the end of the `Spaceship` sprite's code to create a small pause before hippos begin appearing again. Then add a `forever`{:class="block3control"} block around all of your code to make the code run repeatedly.

![лик ракете](images/rocket-sprite.png)

```blocks3
када је кликнуто на ⚑
понављај заувек 
  замени костим са (нормалан v)
  чекај док не <touching (Hippo1 v)>?
  замени костим са (ударац v)
  разгласи (ударац v)

+ чекај (1) секунду
end
```

\--- /task \---