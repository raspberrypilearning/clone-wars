## Hipopótamos espaciales

Ahora vas a añadir muchos hipopótamos voladores que intentan destruir tu nave espacial.

--- task ---

Crea un nuevo objeto con la imagen 'Hippo1' en la biblioteca de Scratch. Usa la herramienta **tamaño** para hacer que el objeto `hipopótamo` tenga un tamaño similar al de la `nave espacial`.

![captura de pantalla](images/invaders-hippo.png)

--- /task ---

--- task ---

Establece el estilo de la rotación del objeto `hipopótamo` para hacerlo **de izquierda a derecha**.

[[[generic-scratch3-sprite-rotation-style]]]

--- /task ---

--- task ---

Agrega algo de código para ocultar el objeto `hipopótamo` cuando comienza el juego.

![objeto hipopótamo](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

--- task ---

Añade código al escenario para crear un nuevo clon de `hipopótamo` cada pocos segundos.

--- hints ---


--- hint ---

Cuando `se hace clic en la bandera verde`{:class="block3events"}, `repetidamente`{:class="block3control"} `esperar`{:class="block3control"} `entre 2 y 4 segundos`{:class="block3operators"} y entonces `crear un clon del objeto hipopótamo`{:class="block3control"}.

--- /hint ---

--- hint ---

Aquí están los bloques que necesitas:

```blocks3
forever
end

create clone of (Hippo1 v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

--- /hint ---

--- hint ---

Así es como debería verse tu código:

![objeto escenario](images/stage-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (2) to (4)) secs
    create clone of (Hippo1 v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

Cada nuevo clon del hipopótamo debe aparecer en una posición `x` aleatoria y cada clon debería tener una velocidad aleatoria.

--- task ---

Crea una nueva variable llamada `velocidad`{:class="block3variables"} que es solo para el objeto `hipopótamo`.

[[[generic-scratch3-add-variable]]]

Cuando hayas hecho esto correctamente, la variable tiene el nombre del objeto al lado, así:

![captura de pantalla](images/invaders-var-test.png)

--- /task ---

--- task ---

Cuando cada clon del `hipopótamo` empiece, elige una velocidad y punto de partida aleatorios para él. Luego muestra el clon en la pantalla.

```blocks3
when I start as a clone
set [velocidad v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

--- /task ---

--- task ---

Prueba tu código. ¿Aparece un nuevo hipopótamo cada pocos segundos?

--- /task ---

Por el momento los hipopótamos no se mueven.

--- task ---

Cada hipopótamo debe moverse al azar hasta ser alcanzado por un rayo. Para que eso suceda, añade este código debajo de los bloques que ya están en el código del objeto `hipopótamo`:

```blocks3
repeat until <touching (lightning v) ?>
    move (velocidad :: variables) steps
    turn right (pick random (-10) to (10)) degrees
    if on edge, bounce
end
delete this clone
```

--- /task ---

--- task ---

Prueba tu código de nuevo. Deberías ver un nuevo clon de hipopótamo aparecer cada pocos segundos y cada clon debería moverse a una velocidad diferente.

--- no-print ---

![captura de pantalla](images/hippo-clones.gif)

--- /no-print ---

--- /task ---

--- task ---

Ahora prueba el cañón láser de la nave espacial. Si un rayo golpea un hipopótamo ¿desaparece el hipopótamo?

--- /task ---