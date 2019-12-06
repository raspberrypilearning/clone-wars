## Construindo uma espaçonave

Primeiro faça uma espaçonave que possa defender a Terra!

\--- task \---

Abra o projeto inicial Scratch 'Guerras Clônicas'.

** Online: ** abra o projeto inicial em [ rpf.io/clone-wars-on ](http://rpf.io/clone-wars-on) {: target = "_ blank"}.

Se você tiver uma conta do Scratch, pode fazer uma cópia clicando em ** Remix **.

**Offline:** baixe o projeto inicial de[rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go), e então abra-o usando o editor offline.

Se você precisa baixar e instalar o editor offline do Scratch, você pode encontra-lo em [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

![projeto inicial](images/starter-project.png)

\--- task \---

Adicione este código ao sprite da espaçonave para fazer a espaçonave se mover para a esquerda se a seta <kbd>esquerda</kbd> for pressionada:

![sprite foguete](images/rocket-sprite.png)

```blocks3
    when flag clicked
    forever
        if <key (left arrow v) pressed?> then
            change x by (-4)
        end
    end
```

O eixo x vai do lado esquerdo da tela para o lado direito. Isso significa que a espaçonave se move para a esquerda quando você subtrai do valor do sprite dela `x` posições. Este bloco de código é a parte que faz sua espaçonave se mover para a esquerda:

```blocks3
change x by (-4)
```

\--- /task \---

\--- task \---

Adicione mais código dentro do bloco `sempre`{:class="block3control"} para fazer sua espaçonave se mover para a direita se a seta <kbd>direita</kbd> for pressionada.

\--- hints \---

\--- hint \---

Subtraindo `4` da posição `x` da espaçonave fez ela se mover para a esquerda, então como você faria para a espaçonave se mover `4` posições para a direita?

\--- /hint \---

\--- hint \---

Você precisa do mesmo bloco de código, porém com um número diferente:

```blocks3
change x by ( )
```

\--- /hint \---

\--- hint \---

Aqui está o código que você precisa adicionar abaixo do outro dentro do bloco `sempre`{:class="block3control"}:

![sprite foguete](images/rocket-sprite.png)

```blocks3
if <key (right arrow v) pressed?> then
    change x by (4)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Teste seu projeto clicando na bandeira verde. Você consegue pressionar as setas para fazer sua espaçonave se mover para a esquerda e direita?

\--- /task \---