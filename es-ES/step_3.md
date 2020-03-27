## Relámpagos

¡Ahora vas a dar a la nave espacial la capacidad de disparar relámpagos!

--- task ---

Añade el sprite `relámpago` de la biblioteca Scratch.

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

Cuando comience el juego, el objeto `relámpago` debe ocultarse hasta que la nave espacial dispare sus cañones láser.

Añade este código al objeto `relámpago`:

![objeto relámpago](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

Por el momento, ¡el relámpago es realmente grande comparado con la nave espacial!

--- task ---

Debajo del código que ya tiene el objeto `relámpago`, añade algunos bloques para hacer el objeto más pequeño y darle la vuelta hacia abajo.

![objeto relámpago](images/lightning-sprite.png)

```blocks3
fijar tamaño al (25) %
apuntar en dirección (-90)
```

Ahora parece que sale de la nave espacial con la punta hacia afuera.

--- /task ---

--- task ---

Añade código para hacer que el objeto `nave espacial` cree un nuevo clon del relámpago si se presiona la <kbd>barra espaciadora</kbd>.

--- hints ---


--- hint ---

`Cuando se hace clic en la bandera verde`{:class="block3events"}, sigue revisando `por siempre`{:class="block3control"} `si`{:class="block3control"} `se presiona la barra espaciadora`{:class="block3sensing"} y en ese caso `crea un clon del objeto del relámpago`{:class="block3control"}.

--- /hint ---

--- hint ---

Aquí están los bloques que necesitas:

```blocks3
si <> entonces
end

por siempre
end

crear clon de (relámpago v)

<key (space v) pressed?>

al presionar bandera verde
```

--- /hint ---

--- hint ---

Así es como debería verse tu nuevo código:

![objeto nave espacial](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
	if <key (space v) pressed?> then
		create clone of (relámpago v)
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Cada vez que el juego cree un clon del objeto `relámpago`, el clon debería aparecer y después moverse hacia arriba hasta que alcance la parte superior del escenario. Entonces el clon debería desaparecer.

Añade este código al objeto `relámpago` para que los clones del objeto se muevan hacia arriba hasta que toquen el borde del escenario y luego se eliminen.

![objeto relámpago](images/lightning-sprite.png)

```blocks3
    when I start as a clone
	  go to (nave espacial v)
    show
	  repeat until <touching (edge v) ?>
		  change y by (10)
	  end
	  delete this clone
```

--- /task ---

--- task ---

Presiona la barra <kbd>espaciadora</kbd> para probar si el relámpago mueve correctamente.

--- /task ---