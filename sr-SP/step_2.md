## Направи свемирски брод

Прво направи свемирски брод који може да одбрани Земљу!

\--- task \---

Отвори Скреч почетни пројекат 'Ратови клонова'.

**На мрежи:** Отвори почетни пројекат на [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target="_blank"}.

Ако имаш Скреч налог, можеш да направиш копију тако што ћеш кликнути на **Преради**.

**Ван мреже:** преузми почетни пројекат са [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go){:target="_blank"}, а затим га отвори помоћу уређивача ван мреже.

Ако је потребно да преузмеш и инсталираш Скреч уређивач ван мреже, можеш га пронаћи на [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

![почетни пројекат](images/starter-project.png)

\--- task \---

Add this code to the spaceship sprite to make the spaceship move left if the <kbd>left</kbd> arrow is pressed:

![лик ракете](images/rocket-sprite.png)

```blocks3
    када је кликнуто на ⚑
понављај заувек 
  ако је <key (left arrow v) pressed?> онда 
    промени x за (-4)
  end
end
```

The x-axis goes from the left side of the Stage to the right side. This means that the spaceship moves to the left when you subtract from the value of the spaceship sprite's `x` position. So this code block is the part that makes your spaceship move left:

```blocks3
промени x за (-4)
```

\--- /task \---

\--- task \---

Add some more code inside the `forever`{:class="block3control"} block to make your spaceship move to the right if the <kbd>right</kbd> arrow key is pressed.

\--- hints \---

\--- hint \---

Subtracting `4` from the spaceship's `x` position made it move left, so how could you make the spaceship move right by `4` instead?

\--- /hint \---

\--- hint \---

You need the same code block, but with a different number:

```blocks3
промени x за ()
```

\--- /hint \---

\--- hint \---

Here is the code you need to add below the other code inside the `forever`{:class="block3control"} block:

![лик ракете](images/rocket-sprite.png)

```blocks3
ако је <key (right arrow v) pressed?> онда 
  промени x за (4)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Test your project by clicking the green flag. Can you press the arrow keys to make your spaceship move left and right?

\--- /task \---