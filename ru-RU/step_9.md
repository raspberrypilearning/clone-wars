## Космическая летучая мышь

Чтобы сделать твою игру немного сложнее, тебе необходимо создать летучую мышь, которая бросает апельсины на космический корабль.

![летучая мышь бросает апельсин на космический корабль](images/bat-oranges.png)

\--- task \---

Добавь спрайт ` Летучая мышь ` и установи для него стиль вращения ** влево-вправо **.

\--- /task \---

\--- task \---

Сделай так, чтобы спрайт ` Летучая мышь ` ` перемещался ` {:class="block3motion"} слева направо в верхней части Сцены ` всегда ` {:class="block3control"}.

![спрайт летучей мыши](images/bat-sprite.png)

```blocks3
когда флаг нажат
установить размер (50) %
повторять всегда
    идти (10) шагов
    если касается края, оттолкнуться
конец
```

Не забудь проверить свой код.

\--- /task \---

Если ты посмотришь на костюмы летучей мыши, то увидишь, что она имеет четыре разных костюма:

![снимок экрана](images/invaders-bat-costume.png)

\--- task \---

Используй блок `следующий костюм` {:class="block3looks"}, чтобы летучая мышь взмахивала крыльями при движении.

\--- hints \---

\--- hint \---

После того, как летучая мышь начала двигаться, должен показываться `следующий костюм` {:class="block3looks"} и затем `ждать` {:class="block3control"} на короткое время.

\--- /hint \---

\--- hint \---

Тебе нужно будет добавить эти блоки в свой код:

```blocks3
ждать (0,3) секунд

следующий костюм
```

\--- /hint \---

\--- hint \---

You code should look like this:

```blocks3
когда флаг нажат
установить размер (50)%
повторять всегда
идти (10) шагов
если касается края, оттолкнуться

+ следующий костюм
+ ждать (0,3) секунд
конец
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Now make the bat throw oranges!

\--- task \---

Add an `Orange` sprite from the Scratch library.

![screenshot](images/invaders-orange.png)

\--- /task \---

\--- task \---

Add code to your bat so that `when the flag is clicked`{:class="block3events"}, the `Bat` sprite `forever`{:class="block3control"} `waits`{:class="block3control"} for a `random`{:class="block3operators"} length of time between `5 to 10`{:class="block3operators"} seconds and then `creates a clone`{:class="block3control"} of the `Orange` sprite.

![bat sprite](images/bat-sprite.png)

```blocks3
когда флаг нажат
повторять всегда
    ждать (выдать случайное от (5) до (10)) секунд
    создать клон (Апельсин)
конец
```

\--- /task \---

\--- task \---

Add code to the `Orange` to make each of its clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

![orange sprite](images/orange-sprite.png)

```blocks3
    когда флаг нажат
    спрятаться

    когда я начинаю как клон
    перейти на (Летучая мышь)
    показаться
    повторять пока не (касается (край)?
        изменить y на (-4)
    конец
    удалить клон
```

\--- /task \---

\--- task \---

Add some more code to the `Orange` sprite so that when an `Orange` clone hits the `Spaceship` sprite, the clone also disappears to give the player a chance to reset:

![orange sprite](images/orange-sprite.png)

```blocks3
    когда я получу [удар]
удалить клон
```

\--- /task \---

\--- task \---

Modify the code of your `Spaceship` sprite so that the sprite is "hit" when it touches a `Hippo` sprite or an `Orange` sprite:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    ждать до <touching (Hippo1 v)?> или <touching (Orange v)?>
```

\--- /task \---

\--- task \---

Test your game. What happens if the spaceship gets hit by a falling orange?

\--- /task \---