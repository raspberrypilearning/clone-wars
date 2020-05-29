## Construindo uma nave espacial

Primeiro faça uma nave espacial que possa defender a Terra!

--- task ---

Abra o projeto inicial 'Guerras dos Clones' no Scratch.

**Online:** abra o projeto inicial em [scratch.mit.edu/projects/400277313](https://scratch.mit.edu/projects/400277313){:target="_blank"}.

Se você tiver uma conta do Scratch, pode fazer uma cópia clicando em **Remix**.

**Offline:** baixe o projeto inicial de [rpf.io/p/pt-BR/clone-wars-go](http://rpf.io/p/pt-BR/clone-wars-go), e abra-o usando o editor offline.

Se você precisa baixar e instalar o editor offline do Scratch, você pode encontrá-lo em [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

![projeto inicial](images/starter-project.png)

--- task ---

Adicione este código ao ator da nave espacial para fazer a nave espacial se mover para a esquerda se a seta <kbd>esquerda</kbd> for pressionada:

![ator foguete](images/rocket-sprite.png)

```blocks3
    quando ⚑ for clicado
sempre 
  se <tecla (seta para esquerda v) pressionada?> então 
    adicione (-4) a x
  end
end
```

O eixo x vai do lado esquerdo do palco para o lado direito. Isso significa que a nave espacial se move para a esquerda quando diminui o valor da posição `x` do ator da nave espacial. Este bloco de código é a parte que faz sua nave espacial se mover para a esquerda:

```blocks3
adicione (-4) a x
```

--- /task ---

--- task ---

Adicione mais código dentro do bloco `sempre`{:class="block3control"} para fazer sua nave espacial se mover para a direita se a seta <kbd>direita</kbd> for pressionada.

--- hints ---


--- hint ---

Subtraindo `4` da posição `x` da nave espacial fez ela se mover para a esquerda, então como você faria para a nave espacial se mover `4` posições para a direita?

--- /hint ---

--- hint ---

Você precisa do mesmo bloco de código, porém com um número diferente:

```blocks3
adicione ( ) a x
```

--- /hint ---

--- hint ---

Aqui está o código que você precisa adicionar abaixo do outro código dentro do bloco `sempre`{:class="block3control"}:

![ator foguete](images/rocket-sprite.png)

```blocks3
se <tecla (seta para direita v) pressionada?> então 
  adicione (4) a x
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Teste seu projeto clicando na bandeira verde. Você consegue pressionar as setas para fazer sua nave espacial se mover para a esquerda e direita?

--- /task ---