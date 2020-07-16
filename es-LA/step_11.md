## Desafío: mejora tu juego

¿Qué mejoras puedes hacer a tu juego?

Aquí tienes algunas sugerencias:

+ Añade paquetes de salud que puedes recoger para ganar vidas adicionales.

![captura de pantalla](images/invaders-aid.png)

+ Añade rocas flotantes que tu nave espacial debe evitar.

![captura de pantalla](images/invaders-rocks.png)

+ Haz que aparezcan más enemigos cuando tu puntuación llegue a `100`.

```blocks3
    wait until <(score :: variables) = [100]>
```