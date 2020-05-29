## Raios elétricos

Agora vamos dar à nave espacial a capacidade de disparar raios!

\--- task \---

Adicione o ator `Lightning` da biblioteca Scratch, mude o nome dele para raio.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Quando o jogo começa, o ator `raio` deve estar oculto até a nave espacial disparar com seus canhões laser.

Adicione este código ao ator `raio`:

![ator raio](images/lightning-sprite.png)

```blocks3
quando ⚑ for clicado
esconda
```

\--- /task \---

Até o momento, o raio elétrico está muito grande se comparado à nave espacial!

\--- task \---

Abaixo está o código atual do ator `raio`, adicione alguns blocos para deixar o ator menor e para virá-lo de cabeça para baixo.

![ator raio](images/lightning-sprite.png)

```blocks3
defina o tamanho como (25) %
aponte para a direção (-90)
```

Agora parece que ele dispara com a ponta virada para a nave espacial.

\--- /task \---

\--- task \---

Adicione mais código no ator da `nave` para criar um novo clone do raio elétrico se a tecla <kbd>espaço</kbd> for pressionada.

\--- hints \---

\--- hint \---

`quando ⚑ for clicado`{:class="block3events"}, verifica em loop `sempre`{:class="block3control"} `se`{:class="block3control"} a `tecla espaço pressionada`{:class="block3sensing"}, e neste caso `crie clone de raio`{:class="block3control"}.

\--- /hint \---

\--- hint \---

Aqui estão os blocos que você precisa:

```blocks3
se <> então
end

sempre
end

crie clone de (raio v)

<tecla (espaço v) pressionada?>

quando ⚑ for clicado
```

\--- /hint \---

\--- hint \---

É assim que seu código deve parecer:

![ator foguete](images/rocket-sprite.png)

```blocks3
quando ⚑ for clicado
sempre 
  se <tecla (espaço v) pressionada?> então 
    crie clone de (raio v)
  end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Sempre que o jogo cria um clone do ator `raio`, o clone deve aparecer e depois se mover para cima até atingir o topo do palco e depois desaparecer.

Adicione este código ao ator `raio` para que os clones se movam para cima até que toquem na borda do Palco, e depois eles serão excluídos.

![ator raio](images/lightning-sprite.png)

```blocks3
    quando eu começar como um clone
vá para (nave v)
mostre
repita até que <tocando em (borda v)?> 
  adicione (10) a y
end
apague este clone
```

\--- /task \---

\--- task \---

Pressione a tecla <kbd>espaço</kbd> para testar se o raio se move corretamente.

\--- /task \---