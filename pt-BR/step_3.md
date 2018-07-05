## Construindo uma espaçonave

Vamos fazer uma espaçonave que vá defender a Terra!

+ Inicie um novo projeto do Scratch e exclua o ator do gato.

[[[generic-scratch-new-project]]]

+ Adicione as `estrelas` de pano de fundo e o ator da ` espaçonave ` para o seu projeto.
    
    ![captura de tela](images/invaders-sprites.png)

[[[generic-scratch-backdrop-from-library]]]

[[[generic-scratch-sprite-from-library]]]

+ Use a ferramenta **encolher** para reduzir o tamanho do ator da sua `espaçonave` e posicione-o perto da parte inferior da tela.

+ Quando a seta **esquerda** for pressionada, a espaçonave deve se mover para a esquerda. Adicione este código para fazer a sua espaçonave se mover para a esquerda quando a seta **esquerda** for pressionada:

```blocks
    when flag clicked
    forever
        if <key [left arrow v] pressed?> then
            change x by (-4)
        end
    end
```

O eixo x vai da esquerda para a direita no Palco, então se você diminuir a posição x da espaçonave, ela se moverá mais para a esquerda. Este código é a parte que faz a sua espaçonave se mover para a esquerda:

```blocks
change x by (-4)
```

+ Adicione mais código dentro do bloco `forever` {: class = "blockcontrol"} para fazer sua espaçonave se mover para a direita quando a seta **direita** for pressionada.

\--- hints \--- \--- hint \---- Se subtrair `4` da posição da espaçonave fez com que ela se movesse para a esquerda, como você poderia fazer ela se mover para a direita por ` 4 `? \--- / hint \--- \--- hint \--- Você precisará usar o mesmo bloco, mas com um número diferente:

```blocks
change x by ( )
```

\--- / hint \--- \--- hint \--- Este é o código que você precisará adicionar abaixo do outro código dentro do bloco `forever` {: class = "blockcontrol"}:

```blocks
if <key [right arrow v] pressed?> then
    change x by (4)
end
```

\--- /hint \--- \--- /hints \---

+ Teste seu projeto clicando na bandeira verde. Você consegue fazer sua espaçonave se mover para a esquerda e para a direita com as setas?