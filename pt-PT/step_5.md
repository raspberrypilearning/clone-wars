## Hipopótamos do espaço

Agora vais acrescentar muitos hipopótamos voadores a tentar destruir a tua nave espacial.

\--- task \---

Crie um novo ator com a imagem 'Hippo1' da biblioteca do Scratch. Usa a ferramenta ** encolher **para fazer com que o ator ` Hipopótamo ` tenha um tamanho semelhante ao do ator ` nave espacial `.

![The Scratch stage with a starry background. A rocket sits in the middle at the bottom of the stage and a hippo sprite with wings is at the top.](images/invaders-hippo.png)

\--- /task \---

\--- task \---

Define o estilo de rotação do ator ` Hipopótamo ` para ** esquerda-direita **.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

Acrescenta algum código para ocultar o ator ` Hipopótamo ` quando o jogo começa.

![ator Hipopótamo](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

\--- /task \---

\--- task \---

Acrescenta algum código ao palco para criar um clone do ` Hippo ` a cada poucos segundos.

\--- hints \---

\--- hint \---

Quando a ` bandeira verde é clicada ` {: class = "block3events"}, ` repetidamente ` {: class = "block3control"} ` espera ` {: class = "block3control"} ` entre 2 e 4 segundos ` {: class = "block3operators"} e ` cria um clone do ator Hippo ` {: class = "block3control"}.

\--- /hint \---

\--- hint \---

Aqui estão os blocos de que necessitas:

```blocks3
forever
end

create clone of (Hippo1 v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

\--- /hint \---

\--- hint \---

Este é o aspeto que o teu código deve ter:

![actor palco](images/stage-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (2) to (4)) secs
    create clone of (Hippo1 v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Cada novo clone de hipopótamo deve aparecer numa posição ` x ` aleatória, e todos os clones devem ter uma velocidade aleatória.

\--- task \---

Cria uma nova variável chamada ` velocidade ` {: class = "block3variables"} que é apenas para o ator ` Hipopótamo `.

[[[generic-scratch3-add-variable]]]

Quando concluíres este passo corretamente, a variável terá o nome do ator ao lado, assim:

![The variable sprite that reads "Hippo1: speed 0"](images/invaders-var-test.png)

\--- /task \---

\--- task \---

Quando cada clone ` Hipopótamo ` começa, escolhe de forma aleatória uma velocidade e um ponto de partida e a seguir aparece no ecrã.

```blocks3
when I start as a clone
set [velocidade v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

\--- /task \---

\--- task \---

Testa o teu código. Há um novo hipopótamo a aparecer a cada poucos segundos?

\--- /task \---

De momento os hipopótamos não se mexem.

\--- task \---

Cada hipopótamo deverá mover-se aleatoriamente até ser atingido por um raio. Para que isso aconteça, acrescenta este código por baixo dos blocos que já estão no código do ator ` Hipopótamo`:

```blocks3
repeat until <touching (lightning v) ?>
    move (velocidade :: variables) steps
    turn right (pick random (-10) to (10)) degrees
    if on edge, bounce
end
delete this clone
```

\--- /task \---

\--- task \---

Testa o teu código novamente. Deves ver um novo clone de hipopótamo aparecer a cada poucos segundos, e cada clone deve mover-se a uma velocidade diferente.

\--- no-print \---

![Animation of the Hippo sprite flying around, two clones are created and move independently.](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Agora testa o canhão laser da nave espacial. Os hipopótamos desaparecem quando são atingidos por um raio?

\--- /task \---