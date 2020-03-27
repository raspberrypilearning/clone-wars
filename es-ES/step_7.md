## Hipopótamos que desaparecen

Cuando la nave espacial explota, todos los hipopótamos deben desaparecer para que los jugadores puedan recuperarse.

--- task ---

Añade código al objeto nave espacial para que `envíe`{:class="block3events"} el mensaje "golpeada" cuando la `nave espacial toque un hipopótamo`{:class="block3sensing"}.

![objeto nave espacial](images/rocket-sprite.png)

```blocks3
al presionar bandera verde
cambiar disfraz a (normal v)
esperar hasta que <touching (hipopótamo v)>
cambiar disfraz a (golpeada v)
+ enviar (golpeada v)
```

--- /task ---

--- task ---

Todos los clones del objeto `hipopótamo` recibirán el mensaje "golpeada" y puedes indicarles que desaparezcan cuando chocan con la nave espacial añadiendo este código a tu objeto `hipopótamo`:

![objeto hipopótamo](images/hippo-sprite.png)

```blocks3
al recibir [golpeada v]
eliminar este clon
```

--- /task ---

--- task ---

Para comprobar si el nuevo código funciona, haz clic en la bandera verde y haz que la nave espacial colisione con un hipopótamo.

![captura de pantalla](images/invaders-hippo-collide.png)

--- /task ---

Después de que la nave espacial explote, aparecen nuevos clones del `hipopótamo`, ¡pero la nave espacial aún está explotada! La nave espacial necesita reiniciarse.

--- task ---

Añade un bloque `espera`{:class="block3control"} al final del código del objeto `nave espacial` para crear una pequeña pausa antes de que los hipopótamos comiencen a aparecer de nuevo. Luego añade un bloque `por siempre`{:class="block3control"} alrededor de todo tu código para hacer que se ejecute repetidamente.

![objeto nave espacial](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
switch costume to (normal v)
wait until <touching (hipopótamo v)>?
switch costume to (golpeada v)
broadcast (golpeada v)
+ wait (1) seconds
end
```

--- /task ---