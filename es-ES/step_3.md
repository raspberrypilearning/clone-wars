## Haz una nave espacial

¡Hagamos una nave espacial que defenderá la Tierra!

+ Comienza un nuevo proyecto de Scratch y elimina el sprite de gato.

[[[generic-scratch-new-project]]]

+ Añade el fondo de `estrellas` y el sprite de la `nave espacial` a tu proyecto.
    
    ![screenshot](images/invaders-sprites.png)

[[[generic-scratch-backdrop-from-library]]]

[[[generic-scratch-sprite-from-library]]]

+ Usa la herramienta **shrink** para hacer tu sprite `nave espacial` un poco más pequeño y colocalo en la parte inferior de la pantalla.

+ Cuando se presiona la tecla de dirección **izquierda**, lave espacial debería moverse hacia la izquierda. Añade este código para hacer que tu nave espacial se mueva hacia la izquierda cuando se presiona la tecla de dirección **izquierda**:

```blocks
    when flag clicked
    forever
        if <key [left arrow v] pressed?> then
            change x by (-4)
        end
    end
```

El eje x va de izquierda a derecha en el escenario, así que si reduces la posición x de la nave espacial restando de ella, se moverá más hacia la izquierda. Este código es la parte que hace que tu nave espacial se mueva hacia la izquierda:

```blocks
cambia x por (-4)
```

+ Añade un poco más de código dentro del bloque `forever`{:class="blockcontrol"} para hacer que tu nave espacial se mueva hacia la derecha cuando se presiona la tecla de dirección **derecha**.

\--- hints \--- \--- hint \--- Si restando `4` de la posición de la nave espacial hizo que se moviera hacia la izquierda, ¿cómo puedes hacer que se mueva a la derecha por `4`? \--- /hint \--- \--- hint \--- Necesitarás usar el mismo bloque, pero con un número diferente:

```blocks
cambia x por ( )
```

\--- /hint \--- \--- hint \--- Aquí está el código que debes añadir debajo el otro código dentro de tu bloque `forever`{:class="blockcontrol"}:

```blocks
si <key [right arrow v] pressed?> luego
    cambia x por (4)
final
```

\--- /hint \--- \--- /hints \---

+ Prueba tu proyecto haciendo clic en la bandera verde. ¿Puedes hacer que tu nave se mueva a la izquierda y la derecha con las teclas de dirección?