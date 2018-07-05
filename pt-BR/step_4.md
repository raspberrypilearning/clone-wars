## Raios elétricos

Vamos dar à espaçonave a capacidade de disparar raios!

+ Adicione o ator `Lightning` da biblioteca Scratch.

+ Quando o jogo é iniciado, o ator `Raio elétrico` deve estar escondido até que a espaçonave dispare seus canhões de laser. Para isso, adicione este código ao ator `Raio elétrico`:

```blocks
when green flag clicked
hide
```

No momento você tem um raio elétrico gigantesco para a espaçonave disparar!

+ Adicione um código abaixo dos blocos que você acabou de criar para fazer ator `Raio elétrico` menor e virar de cabeça para baixo. Então parecerá que a espaçonave dispara o raio, com a ponta do raio saindo primeiro.

```blocks
set size to (25) %
point in direction (-90 v)
```

+ Mude para o ator `espaçonave` clicando no painel Atores abaixo do Palco.

+ Adicione um novo código para fazer o sprite da `espaçonave` criar um novo raio elétrico sempre que a tecla **espaço** for pressionada.

\--- hints \--- \--- hint \--- Aqui está um pseudocódigo para você:

Quando a bandeira verde é clicada Continue checando para sempre Se a tecla **espaço** foi pressionada, crie um clone do ator `Raio elétrico` \--- / hint \--- \--- hint \--- Aqui estão os blocos que você irá precisar:

![Dica](images/hint-lightning.png) \--- / hint \--- \--- dica \--- Aqui está o código que você irá precisar:

```blocks
when flag clicked
forever
    if <key [space v] pressed?> then
        create clone of [Lightning v]
    end
end
```

\--- /hint \--- \--- /hints \---

+ Volte para o ator `Raio elétrico`.

+ Sempre que um raio é criado, ele deve aparecer e, em seguida, mover-se para cima até chegar ao topo da tela. Então deve desaparecer.

\--- hints \--- \--- hint \---

Quando um novo clone do ator `Here are the blocks you will need:`aparecer:

+ Exiba-o
+ Repetidamente mova-o para cima por `10` até que esteja tocando a borda da tela
+ Em seguida, exclua o clone \--- / hint \--- \--- hint \--- Aqui estão os blocos que você irá precisar:

![Mova o raio elétrico](images/move-hint-lightning.png) \--- / hint \--- \--- hint \--- Aqui está o código que você precisará adicionar ao ator `Raio elétrico`:

```blocks
    when I start as a clone
    show
    repeat until <touching [edge v] ?>
        change y by (10)
    end
    delete this clone
```

\--- /hint \--- \--- /hints \---

+ Teste seu ator `raio elétrico` clicando na bandeira verde e, em seguida, pressionando o a tecla **espaço**. Quando você pressiona **espaço**, o raio aparece e se move para cima na tela? Qual problema você consegue identificar?

## \--- collapse \---

## title: Resposta

Oops - atualmente, o raio elétrico sempre dispara do mesmo lugar, independente de onde a espaçonave esteja!

Adicione este bloco antes do bloco `show` {: class = "blocklooks"} para fazer o clone do `Raio elétrico` se mover para a posição do ator `espaçonave`, antes de aparecer. Isso fará com que pareça que o raio está sendo disparado da espaçonave.

```blocks
go to [Spaceship v]
```

\--- /collapse \---

+ Pressione a tecla **espaço** para testar se o seu raio agora dispara corretamente.

\--- challenge \---

### Desafio: corrigindo o raio

O que acontece se você apertar e segurar a tecla **espaço**? Você consegue usar um block `wait` {: class = "blockcontrol"} para corrigir isso?

\--- /challenge \---