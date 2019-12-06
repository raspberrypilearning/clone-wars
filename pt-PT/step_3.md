## Relâmpagos

Agora vais dar à nave espacial a capacidade de disparar raios!

\--- task \---

Adiciona o ator ` Relâmpago ` da biblioteca do Scratch.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Quando o jogo começa, o ator ` Relâmpago ` deve ficar oculto até a nave espacial disparar os seus canhões laser.

Adiciona este código ao ator ` Relâmpago `:

![ator Relâmpago](images/lightning-sprite.png)

```blocks3
quando alguém clicar na bandeira verde
esconde-te
```

\--- /task \---

Neste momento, o raio é realmente muito grande quando comparado com a nave espacial!

\--- task \---

Por baixo do código que o ator ` Relâmpago ` já possui, acrescenta alguns blocos para o diminuir e virar de cabeça para baixo.

![ator Relâmpago](images/lightning-sprite.png)

```blocks3
altera o teu tamanho para (25) %
altera a tua direção para (-90) °
```

Agora parece que está a ser disparado com a ponta virada para a nave espacial.

\--- /task \---

\--- task \---

Acrescenta um novo bloco de código ao ator ` nave espacial ` para criar um novo clone do relâmpago quando a tecla <kbd> espaço </kbd> é pressionada.

\--- hints \---

\--- hint \---

` Quando a bandeira verde é clicada ` {: class = "block3events"}, verifica continuamente ` para sempre ` {: class = "block3control"} ` se ` {: class = "block3control"} a tecla de espaço ` está a ser pressionada ` {: class = "block3sensing"} e, nesse caso, ` cria um clone do ator Relâmpago ` {: class = "block3control"}.

\--- /hint \---

\--- hint \---

Aqui estão os blocos de que necessitas:

```blocks3
se <>, então
end

repete para sempre
end

cria um clone de (Lightning v)

<a tecla (space v) está a ser pressionada>

Quando alguém clicar na bandeira verde
```

\--- /hint \---

\--- hint \---

Este é o aspeto que o teu código deve ter:

![ator Foguetão](images/rocket-sprite.png)

```blocks3
quando alguém clicar na bandeira verde
repete para sempre 
  se <a tecla (space v) está a ser pressionada>, então 
    cria um clone de (Lightning v)
  end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Sempre que o jogo cria um clone do ator` Relâmpago `, o clone deverá aparecer e depois mover-se para cima até atingir o topo do palco e depois desaparecer.

Acrescenta este código ao ator ` Relâmpago ` para que os clones se movam para cima até tocar na borda do palco e depois serem eliminados.

![ator Relâmpago](images/lightning-sprite.png)

```blocks3
    quando fores criado como um clone
vai para (Spaceship v)
mostra-te
até que <estás a tocar em (edge v)>, repete 
  adiciona (10) ao teu y
end
remove-te como clone
```

\--- /task \---

\--- task \---

Pressiona a tecla <kbd> espaço </kbd> para testar se o relâmpago se move corretamente.

\--- /task \---