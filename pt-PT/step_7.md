## Hipopótamos que desaparecem

Quando a nave espacial explode, todos os hipopótamos devem desaparecer para que os jogadores possam recuperar-se.

\--- task \---

Acrescenta código ao ator da nave espacial para ele ` difundir ` {: class = "block3events"} a mensagem "atingido" quando a ` nave espacial toca num hipopótamo ` {: class = "block3sensing"}.

![ator Foguetão](images/rocket-sprite.png)

```blocks3
quando alguém clicar na bandeira verde
muda o teu traje para (normal v)
espera até que <estás a tocar em (Hippo1 v)>
muda o teu traje para (hit v)

+ difunde a mensagem (hit v)
```

\--- /task \---

\--- task \---

Todos os clones do ator ` Hipopótamo ` irão receber a mensagem "atingido" e poderás assim ordenar-lhes que desapareçam quando a nave é atingida, acrescentando este código ao ator ` Hippo `:

![ator hipopótamo](images/hippo-sprite.png)

```blocks3
quando receberes a mensagem [hit v]
remove este clone
```

\--- /task \---

\--- task \---

Para verificar se o novo código funciona, clica na bandeira verde e faz com que a nave colida com um hipopótamo.

![captura de ecrã](images/invaders-hippo-collide.png)

\--- /task \---

Depois da nave espacial explodir, novos clones do ` Hippo ` aparecem, mas a nave espacial ainda está explodida! Ela necessita redefinir-se após ser atingida.

\--- task \---

Adiciona um bloco ` espera ` {: class = "block3control"} no final do código do ator ` nave espacial ` para criar uma pequena pausa antes de os hipopótamos voltarem a aparecer. Seguidamente, acrescenta um bloco ` para sempre ` {: class = "block3control"} em redor de todo o código para fazer com que este seja executado repetidamente.

![ator foguetão](images/rocket-sprite.png)

```blocks3
quando alguém clicar na bandeira verde
repete para sempre 
 muda o teu traje para (normal v)
 espera até que <estás a tocar em (Hippo1 v)>
 muda o teu traje para (hit v)
 difunde a mensagem (hit v)
 + espera (1) s
end
```

\--- /task \---