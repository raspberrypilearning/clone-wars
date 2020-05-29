## Hipopótamos que desaparecem

Quando a nave espacial explodir, todos os hipopótamos devem desaparecer para que os jogadores do jogo possam se recuperar.

\--- task \---

Acrescente código ao ator nave espacial para que ele `transmita` {:class="block3events"} a mensagem "atingida" quando a `nave toca em um hipopótamo`{:class="block3sensing"}.

![ator foguete](images/rocket-sprite.png)

```blocks3
when flag clicked
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (hit v)

+ broadcast (hit v)
```

\--- /task \---

\--- task \---

Todos os clones do ator `hipopótamo1` receberão a mensagem "atingida" e você pode instruí-los a desaparecer quando a nave espacial é atingida adicionando este código ao ator `hipopótamo1`:

![ator hipopótamo](images/hippo-sprite.png)

```blocks3
when I receive [hit v]
delete this clone
```

\--- /task \---

\--- task \---

Para verificar se o novo código funciona, clique na bandeira verde e faça a nave espacial colidir com um hipopótamo.

![captura de tela](images/invaders-hippo-collide.png)

\--- /task \---

Depois que a nave espacial explode, novos clones `hipopótamo1` aparecem, mas a nave espacial ainda está explodida! A nave espacial precisa ser reiniciada após ser atingida.

\--- task \---

Adicione um bloco `espere`{:class="block3control"} no final do código do ator `nave` para criar uma pequena pausa antes que os hipopótamos comecem a aparecer novamente. Em seguida, adicione um bloco `sempre`{:class="block3control"} ao redor de todo o seu código para fazer com que o código seja executado repetidamente.

![ator foguete](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (hit v)
broadcast (hit v)

+ wait (1) seconds
end
```

\--- /task \---