## Haz una nave espacial

¡Primero haz una nave espacial que pueda defender la Tierra!

--- task ---

Abre el proyecto inicial de Scratch 'Guerra de clones'.

**En línea:** abre el proyecto de inicio en [scratch.mit.edu/projects/414636091](https://scratch.mit.edu/projects/414636091){:target="_blank"}.

Si tienes una cuenta Scratch puedes hacer una copia haciendo clic en **Remix**.

**Sin conexión:** descarga el proyecto inicial desde [rpf.io/p/es-LA/clone-wars-go](http://rpf.io/p/es-LA/clone-wars-go), y luego ábrelo con el editor sin conexión.

Si necesitas descargar e instalar el editor sin conexión de Scratch, puedes encontrarlo en [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

![proyecto inicial](images/starter-project.png)

--- task ---

Añade este código al objeto de la nave espacial para hacer que la nave espacial se mueva a la izquierda si la flecha <kbd>izquierda</kbd> está presionada:

![objeto nave espacial](images/rocket-sprite.png)

```blocks3
    when flag clicked
    forever
        if <key (left arrow v) pressed?> then
            change x by (-4)
        end
    end
```

El eje x va desde el lado izquierdo del escenario hasta el lado derecho. Esto significa que la nave espacial se mueve hacia la izquierda cuando se resta del valor de la posición `x` del objeto de la nave espacial. Este bloque código es la parte que hace que tu nave espacial se mueva hacia la izquierda:

```blocks3
change x by (-4)
```

--- /task ---

--- task ---

Añade un poco más de código dentro del bloque `por siempre`{:class="block3control"} para hacer que tu nave espacial se mueva hacia la derecha cuando se presiona la tecla de dirección <kbd>derecha</kbd>.

--- hints ---


--- hint ---

Restando `4` de la posición `x` de la nave espacial hizo que se moviera hacia la izquierda, así que ¿cómo puedes hacer que la nave espacial se mueva hacia la derecha `4` en su lugar?

--- /hint ---

--- hint ---

Necesitas el mismo bloque de código, pero con un número diferente:

```blocks3
change x by ( )
```

--- /hint ---

--- hint ---

Aquí está el código que debes añadir bajo el otro código dentro de tu bloque `por siempre`{:class="block3control"}:

![objeto nave espacial](images/rocket-sprite.png)

```blocks3
if <key (right arrow v) pressed?> then
    change x by (4)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Prueba tu proyecto haciendo clic en la bandera verde. ¿Puedes presionar las teclas de flecha para hacer que tu nave espacial se mueva a la izquierda y a la derecha?

--- /task ---