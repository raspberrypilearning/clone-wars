## Hipopótamos espaciais

Agora você vai adicionar muitos hipopótamos voadores que tentarão destruir a sua nave espacial.

\--- task \---

Crie um novo ator com a imagem 'Hippo1' da biblioteca do Scratch e mude o nome dele para hipopótamo1. Use a ferramenta ** encolher** para fazer com que o ator `hipopótamo1` tenha um tamanho semelhante ao do ator `nave`.

![The Scratch stage with a starry background. A rocket sits in the middle at the bottom of the stage and a hippo sprite with wings is at the top.](images/invaders-hippo.png)

\--- /task \---

\--- task \---

Defina o estilo de rotação do ator `hipopótamo1` como **esquerda-direita**.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

Adicione código para esconder o ator `hipopótamo1` quando o jogo começar.

![ator hipopótamo1](images/hippo-sprite.png)

```blocks3
quando ⚑ for clicado
esconda
```

\--- /task \---

\--- task \---

Adicione código ao Palco para criar um novo clone de `hipopótamo1` a cada poucos segundos.

\--- dica \---

\--- hint \---

Quando a `bandeira verde é clicada`{:class="block3events"}, `sempre`{:class="block3control"} `espere`{:class="block3control"} `entre 2 e 4 segundos`{:class="block3operators"} e `crie um clone do ator hipopótamo1`{:class="block3control"}.

\--- /hint \---

\--- hint \---

Aqui estão os blocos que você precisa:

```blocks3
sempre
end

crie clone de (hipopótamo1 v)

(número aleatório entre (2) e (4))

quando ⚑ for clicado

espere () seg
```

\--- /hint \---

\--- hint \---

É assim que seu código deve estar:

![ator palco](images/stage-sprite.png)

```blocks3
quando ⚑ for clicado
sempre 
  espere (número aleatório entre (2) e (4)) seg
  crie clone de (hipopótamo1 v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Cada novo clone do hipopótamo deve aparecer numa posição `x` aleatória, e cada clone deve ter uma velocidade aleatória.

\--- task \---

Crie uma nova variável chamada `velocidade`{:class="block3variables"} apenas para o ator `hipopótamo1`.

[[[generic-scratch3-add-variable]]]

Quando você fizer isso corretamente, a variável terá o nome do ator ao lado, assim:

![The variable sprite that reads "Hippo1: speed 0"](images/invaders-var-test.png)

\--- /task \---

\--- task \---

Quando cada clone de `hipopótamo1` começar, escolha uma velocidade aleatória e um ponto de partida. Em seguida, mostre o clone na tela.

```blocks3
quando eu começar como um clone
mude [velocidade v] para (número aleatório entre (2) e (4))
vá para x: (número aleatório entre (-220) e (220)) y: (150)
mostre
```

\--- /task \---

\--- task \---

Teste seu código. Um novo hipopótamo aparece a cada poucos segundos?

\--- /task \---

No momento os hipopótamos não se movem.

\--- task \---

Cada hipopótamo deve se mover aleatoriamente até ser atingido por um raio. Para que isso aconteça, acrescente este código abaixo dos blocos que já estão no código do ator `hipopótamo1`:

```blocks3
repita até que <tocando em (raio v) ?> 
  mova (velocidade :: variables) passos
  gire ↻ (número aleatório entre (-10) e (10)) graus
  se tocar na borda, volte
end
apague este clone
```

\--- /task \---

\--- task \---

Teste seu código novamente. Você deve ver um novo clone de hipopótamo aparecer a cada poucos segundos, e cada clone deve se mover a uma velocidade diferente.

\--- no-print \---

![Animation of the Hippo sprite flying around, two clones are created and move independently.](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Agora teste o canhão de laser da nave espacial. Se um raio atingir um hipopótamo, o hipopótamo desaparece?

\--- /task \---