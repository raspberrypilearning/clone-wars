## Raios

Agora vamos dar à nave espacial a capacidade de disparar raios!

--- task ---

Adicione o ator `Lightning` da biblioteca Scratch, mude o nome dele para raio.

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

Quando o jogo começa, o ator `raio` deve estar oculto até a nave espacial disparar com seus canhões laser.

Adicione este código ao ator `raio`:

![ator raio](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

Até o momento, o raio elétrico está muito grande se comparado à nave espacial!

--- task ---

Abaixo está o código atual do ator `raio`, adicione alguns blocos para deixar o ator menor e para virá-lo de cabeça para baixo.

![ator raio](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

Agora parece que ele dispara com a ponta virada para a nave espacial.

--- /task ---

--- task ---

Adicione mais código no ator da `nave` para criar um novo clone do raio elétrico se a tecla <kbd>espaço</kbd> for pressionada.

--- hints ---


--- hint ---

`quando ⚑ for clicado`{:class="block3events"}, verifica em loop `sempre`{:class="block3control"} `se`{:class="block3control"} a `tecla espaço pressionada`{:class="block3sensing"}, e neste caso `crie clone de raio`{:class="block3control"}.

--- /hint ---

--- hint ---

Aqui estão os blocos que você precisa:

```blocks3
if <> then
end

forever
end

create clone of (raio v)

<key (espaço v) pressed?>

when flag clicked
```

--- /hint ---

--- hint ---

É assim que seu código deve parecer:

![ator foguete](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
	if <key (espaço v) pressed?> then
		create clone of (raio v)
  end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Sempre que o jogo cria um clone do ator `raio`, o clone deve aparecer e depois se mover para cima até atingir o topo do palco e depois desaparecer.

Adicione este código ao ator `raio` para que os clones se movam para cima até que toquem na borda do Palco, e depois eles serão excluídos.

![ator raio](images/lightning-sprite.png)

```blocks3
	when I start as a clone
	go to (nave v)
    show
	repeat until <touching (borda v)?> 
		change y by (10)
	end
	delete this clone
```

--- /task ---

--- task ---

Pressione a tecla <kbd>espaço</kbd> para testar se o raio se move corretamente.

--- /task ---