## Constrói uma nave espacial

Começa por construir uma nave espacial que possa defender a Terra!

\--- task \---

Abre o projeto inicial 'Guerra dos Clones' em Scratch.

**Online:** abre o projeto inicial Scratch em [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target="_blank"}.

Se tiveres uma 'conta Scratch' podes fazer uma cópia ao clicares **Remix**.

**Offline:** descarrega o projeto inicial de [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go), e depois abre-o no editor offline do Scratch.

Se precisares de descarregar e instalar o editor offline do Scratch, podes encontrá-lo em [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

![projeto inicial](images/starter-project.png)

\--- task \---

Acrescenta este código ao ator da nave espacial para fazer com que a nave se mova para a esquerda quando a seta <kbd> esquerda </kbd> é pressionada:

![ator Foguetão](images/rocket-sprite.png)

```blocks3
    quando alguém clicar na bandeira verde
repete para sempre 
  se <a tecla (left arrow v) está a ser pressionada>, então 
    adiciona (-4) ao teu x
  end
end
```

O eixo dos x vai do lado esquerdo do palco para o lado direito. Isto significa que a nave espacial se move para a esquerda quando se subtrai ao valor do ` x ` da posição do ator nave espacial. Portanto, este bloco de código é a parte que faz com que a tua nave espacial se mova para a esquerda:

```blocks3
adiciona (-4) ao teu x
```

\--- /task \---

\--- task \---

Acrescenta um pouco mais de código dentro do `repete para sempre ` {: class = "block3control"} para fazer com que a tua nave espacial se mova para a direita, se a tecla de seta <kbd> direita </kbd> for pressionada.

\--- hints \---

\--- hint \---

Como subtrair ` 4 ` ao ` x ` da posição da nave espacial faz com que ela se mova para a esquerda, consegues em vez disso fazer com que a nave espacial se mova por ` 4 ` para a direita?

\--- /hint \---

\--- hint \---

Vais necessitar do mesmo bloco de código, mas com um número diferente:

```blocks3
adiciona () ao teu x
```

\--- /hint \---

\--- hint \---

Aqui está o código que vai ter que adicionar por baixo do código dentro do Bloco ` repete para sempre ` {: class = "block3control"}:

![ator foguetão](images/rocket-sprite.png)

```blocks3
se <a tecla (right arrow v) está a ser pressionada>, então 
  adiciona (4) ao teu x
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Teste o teu projeto clicando na bandeira verde. Consegues pressionar as teclas de seta para fazer a tua nave espacial mover-se para a esquerda e para a direita?

\--- /task \---