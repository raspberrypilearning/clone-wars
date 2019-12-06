## Raios elétricos

Agora vamos dar à espaçonave a capacidade de disparar raios!

\--- task \---

Adicione o ator `Lightning` da biblioteca Scratch.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Quando o jogo começa, o sprite `Lightning` deve estar oculto até a espaçonave atirar com seus canhões laser.

Adicione este código ao sprite `Lightning`:

![lightning sprite](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

\--- /task \---

Até o momento, o raio elétrico está grande se comparado com a espaçonave!

\--- task \---

Abaixo está o código atual do sprite `Lightning`, adicione alguns blocos para deixar o sprite menor e para vira-lo ao contrário.

![lightning sprite](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

Agora parece que ele dispara para fora da espaçonave.

\--- /task \---

\--- task \---

Adicione um código novo para o sprite da `Espaçonave` para criar um novo clone do raio elétrico se a tecla <kbd>espaço</kbd> for pressionada.

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