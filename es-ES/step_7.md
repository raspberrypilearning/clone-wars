## Hipopótamos que desaparecen

Cuando se encuentra la nave espacial, los hipopótamos deben desaparecer para dar al jugador una oportunidad para recuperar.

+ Añade un bloque a tu código para enviar un `broadcast` del mensaje "hit" cuando la nave espacial esté en contacto con un hipopótamo.

[[[generic-scratch-broadcast-message]]]

\--- hints \--- \--- hint \--- Crea un bloque `broadcast` 'hit' arrastrando el bloque de la pestaña **Eventos** y luego, haciendo clic en el menú desplegable y seleccionando **nuevo mensaje**. \--- /hint \--- \--- hint \--- Aquí están los bloques que necesitarás:

```blocks
broadcast [hit v]
```

\--- /hint \--- \--- hint \--- Aquí está el código que necesitarás:

```blocks
al presionar la bandera
cambia el disfraz a [normal v]
espera hasta que <touching [Hippo1 v]>
cambia el disfraz a [hit v]
broadcast [hit v]
```

\--- /hint \--- \--- /hints \---

Todos los clones del sprite `Hippo` escuchará este mensaje, por lo que ahora puedes indicar que desaparecen cuando la nave espacial se ve afectada.

+ Agregue este código al sprite `hipopótamo`:

```blocks
al recibir [hit v]
elimina este clon
```

+ Prueba este código comenzando un nuevo juego y chocando deliberadamente con un hipopótamo.

![screenshot](images/invaders-hippo-collide.png)

Después de ser golpeado, hipopótamos comienzan a reaparecer pero la nave espacial se ha disparado todavía! Vamos a hacer posible que la nave espacial reajuste después de ser golpeada.

+ Agrega un bloque `forever`{:class="blockcontrol"} alrededor de todo tu código para hacer que el processo se repita, y un bloque `esperar`{:class="blockcontrol"} al fin para agregar una pausa pequeña antes de que los hipopótamos comienzen a aparecerse una vez más.

```blocks
al presionar la bandera
para siempre
    cambia el disfraz a [normal v]
    hasta que <touching [Hippo1 v]>?
    cambia el disfraz a [hit v]
    broadcast [hit v]
    espera (1) seg
fin
```

\--- challenge \---

### Desafío: vidas y marcador

Por el momento, el jugador tiene vidas infinitas. ¿Puedes añadir `vidas`{:class="blockdata"}, un `marcador`{:class="blockdata"}, o incluso una `puntuación alta`{:class="blockdata"} a tu juego?

[[[generic-scratch-high-score]]] \--- /challenge \---