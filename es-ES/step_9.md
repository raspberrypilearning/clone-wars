## Murciélago espacial

Para hacer tu juego un poco más difícil, vas a crear un murciélago que arroje naranjas a la nave espacial.

![un murciélago arrojando una naranja a la nave espacial](images/bat-oranges.png)

\--- task \---

Añade un objeto `murciélago` y establece su estilo de rotación en **izquierda-derecha**.

\--- /task \---

\--- task \---

Haz que el objeto `murciélago` se `mueva`{:class="block3motion"} de izquierda a derecha en la parte superior del escenario `por siempre`{:class="block3control"}.

![objeto murciélago](images/bat-sprite.png)

```blocks3
al presionar bandera verde
fijar tamaño al (50) %
por siempre 
  mover (10) pasos
  si toca un borde, rebotar
end
```

Recuerda probar tu código.

\--- /task \---

Si miras los disfraces del murciélago, puedes ver que tiene cuatro diferentes:

![captura de pantalla](images/invaders-bat-costume.png)

\--- task \---

Usa el bloque `siguiente disfraz`{:class="block3looks"} para hacer que el murciélago bata sus alas mientras se mueve.

\--- hints\---

\--- hint \---

Después de que el murciélago se haya movido, debería mostrar el `siguiente disfraz`{:class="block3looks"} y luego `esperar`{:class="block3control"} por poco tiempo.

\--- /hint \---

\--- hint \---

Tienes que añadir estos bloques a tu código:

```blocks3
esperar (0.3) segundos

siguiente disfraz
```

\--- /hint \---

\--- hint \---

Tu código debe parecerse a esto:

```blocks3
al presionar bandera verde
fijar tamaño al (50) %
por siempre 
 mover (10) pasos
 si toca un borde, rebotar
 + siguiente disfraz
 + esperar (0.3) segundos
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

¡Ahora haz que el murciélago lance naranjas!

\--- task \---

Añade el objeto `murciélago` (Bat) de la biblioteca de Scratch.

![captura de pantalla](images/invaders-orange.png)

\--- /task \---

\--- task \---

Añade código a tu murciélago para que `cuando se hace clic en la bandera`{:class="block3events"}, el objeto `murciélago` `espere`{:class="block3control"} `por siempre`{:class="block3control"} durante un período de tiempo `aleatorio`{:class="block3operators"} de `5 a 10`{:class="block3operators"} segundos y luego `crea un clon`{:class="block3control"} del objeto `naranja`.

![objeto murciélago](images/bat-sprite.png)

```blocks3
al presionar bandera verde
por siempre 
  esperar (número aleatorio entre (5) y (10)) segundos
  crear clon de (Orange v)
end
```

\--- /task \---

\--- task \---

Añade código a la `naranja` para hacer que cada uno de sus clones caiga desde el objeto `murciélago` y cayendo hacia abajo en el escenario.

![objeto de una naranja](images/orange-sprite.png)

```blocks3
    al presionar bandera verde
esconder

al comenzar como clon
ir a (murciélago v)
mostrar
repetir hasta que <¿tocando (edge v)?
  sumar a y (-4)
end
eliminar este clon
```

\--- /task \---

\--- task \---

Añade algo más de código al objeto `naranja` para que cuando un clon de la `naranja` golpee el objeto `nave espacial`, el clon también desaparezca para dar al jugador la oportunidad de reiniciar:

![objeto naranja](images/orange-sprite.png)

```blocks3
    al recibir [hit v]
eliminar este clon
```

\--- /task \---

\--- task \---

Modifica el código de tu objeto `nave espacial` para que el objeto sea "golpeado" cuando toque un objeto `hipopótamo` o un objeto `naranja`:

![objeto nave espacial](images/rocket-sprite.png)

```blocks3
    esperar hasta que <<touching (Hippo1 v)?> o <touching (Orange v)?>>
```

\--- /task \---

\--- task \---

Prueba tu juego. ¿Qué pasa si una naranja que cae golpea a la nave espacial?

\--- /task \---