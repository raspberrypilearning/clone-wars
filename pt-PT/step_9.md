## Morcego espacial

Para tornar o teu jogo um pouco mais difícil, irás criar um morcego que atira laranjas à nave espacial.

![um morcego a atirar uma laranja à nave espacial](images/bat-oranges.png)

\--- task \---

Acrescenta um ator ` morcego ` e define o seu estilo de rotação para ** esquerda-direita **.

\--- /task \---

\--- task \---

Faz o ator ` morcego ` ` mover-se ` {: class = "block3motion"} da esquerda para a direita no topo do palco ` para sempre ` {: class = "block3control"}.

![ator morcego](images/bat-sprite.png)

```blocks3
quando alguém clicar na bandeira verde
altera o teu tamanho para (50) %
repete para sempre 
  anda (10) passos
  se estiveres a bater na borda, ressalta
end
```

Lembra-te de testar o teu código.

\--- /task \---

Se olhares para os trajes do morcego, poderás ver que há quatro diferentes:

![captura de ecrã](images/invaders-bat-costume.png)

\--- task \---

Usa o bloco ` próximo traje ` {: class = "block3looks"} para fazer com que o morcego bata as asas enquanto se move.

\--- hints \---

\--- hint \---

Depois de o morcego se mover, ele deve mostrar o ` próximo traje ` {: class = "block3looks"} e depois ` aguardar ` {: class = "block3control"} por um curto período de tempo.

\--- /hint \---

\--- hint \---

Vais necessitar acrescentar estes blocos ao teu código:

```blocks3
espera (0.3) s

passa para o teu próximo traje
```

\--- /hint \---

\--- hint \---

O teu código deverá ter este aspeto:

```blocks3
quando alguém clicar na bandeira verde
altera o teu tamanho para (50) %
repete para sempre 
 anda (10) passos
 se estiveres a bater na borda, ressalta
 + passa para o teu próximo traje
 + espera (0.3) s
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Agora faz com que o morcego atire laranjas!

\--- task \---

Acrescenta o ator ` Laranja ` da biblioteca do Scratch.

![captura de ecrã](images/invaders-orange.png)

\--- /task \---

\--- task \---

Adiciona código ao seu morcego para que ` quando a bandeira verde for clicada ` {: class = "block3events"}, o ator ` morcego ` aguarda ` para sempre ` {: class = "block3control"} ` ` {: class = "block3control"} durante um período de tempo ` aleatório ` {: class = "block3operators"} entre ` 5 e 10 ` {: class = "block3operators"} segundos antes de ` criar um clone ` {: class = "block3control"} do ator ` Laranja `.

![ator morcego](images/bat-sprite.png)

```blocks3
quando alguém clicar na bandeira verde
repete para sempre 
  espera (um valor ao acaso entre (5) e (10)) s
  cria um clone de (Orange v)
end
```

\--- /task \---

\--- task \---

Acrescenta código à ` Laraja ` para fazer com que cada um dos seus clones caia, começando no ator ` Morcego ` e caindo depois em direção ao fundo do palco.

![ator laranja](images/orange-sprite.png)

```blocks3
    quando alguém clicar na bandeira verde
esconde-te

Quando fores criado como um clone
vai para (Bat v)
mostra-te
até que  <estás a tocar em (edge v)>, repete 
  adiciona (-4) ao teu y
end
remove-te como clone
```

\--- /task \---

\--- task \---

Acrescenta um pouco mais de código ao ator ` Laranja ` para que quando um clone ` Laranja ` atinge o ator ` nave espacial` ele também desapareça para dar ao jogador a oportunidade de se redefinir:

![ator laranja](images/orange-sprite.png)

```blocks3
    quando receberes a mensagem [hit v]
remove este clone
```

\--- /task \---

\--- task \---

Modifica o código do teu ator ` nave espacial ` para que ele seja "atingido" quando toca num ator ` Hipopótamo ` ou num ator ` Laranja `:

![ator Foguetão](images/rocket-sprite.png)

```blocks3
    espera até que <<estás a tocar em (Hippo1 v)> ou <estás a tocar em (Orange v)>>
```

\--- /task \---

\--- task \---

Testa o teu jogo. O que é que acontece se a nave espacial for atingida por uma laranja em queda?

\--- /task \---