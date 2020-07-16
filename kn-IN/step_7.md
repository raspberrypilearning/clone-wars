## ಕಣ್ಮರೆಯಾಗುವ ಹಿಪ್ಪೋಸ್

ಆಕಾಶನೌಕೆ ಸ್ಫೋಟಗೊಂಡಾಗ, ಎಲ್ಲಾ ಹಿಪ್ಪೋಗಳು ಕಣ್ಮರೆಯಾಗಬೇಕು ಇದರಿಂದ ಆಟದ ಆಟಗಾರರು ಚೇತರಿಸಿಕೊಳ್ಳಬಹುದು.

\--- task \---

`spaceship touched a hippo`{:class="block3sensing"} ಮುಟ್ಟಿದಾಗ `broadcast`{:class="block3events"} ಎನ್ನುವ "hit" ಸಂದೇಶವನ್ನು ಮಾಡಲು ಆಕಾಶನೌಕೆ sprite ಗೆ ಕೋಡ್ ಅನ್ನು ಸೇರಿಸಿರಿ.

![rocket sprite](images/rocket-sprite.png)

```blocks3
when flag clicked
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (hit v)

+ broadcast (hit v)
```

\--- /task \---

\--- task \---

ಎಲ್ಲಾ `Hippo` sprite clones "hit" ಸಂದೇಶವನ್ನು ಸ್ವೀಕರಿಸುತ್ತವೆ, ಮತ್ತು ಈ ಕೋಡ್ ಅನ್ನು `Hippo`sprite ಸೇರಿಸುವ ಮೂಲಕ ಆಕಾಶನೌಕೆ ಹೊಡೆದಾಗ ಕಣ್ಮರೆಯಾಗುವಂತೆ ನೀವು ಅವರಿಗೆ ಸೂಚಿಸಬಹುದು:

![hippo sprite](images/hippo-sprite.png)

```blocks3
when I receive [hit v]
delete this clone
```

\--- /task \---

\--- task \---

ಹೊಸ ಕೋಡ್ ಕಾರ್ಯನಿರ್ವಹಿಸುತ್ತದೆಯೇ ಎಂದು ಪರಿಶೀಲಿಸಲು, ಹಸಿರು ಧ್ವಜವನ್ನು ಕ್ಲಿಕ್ ಮಾಡಿ ಮತ್ತು ಆಕಾಶನೌಕೆ ಹಿಪ್ಪೋಗೆ ಡಿಕ್ಕಿ ಹೊಡೆಯುವಂತೆ ಮಾಡಿ.

![screenshot](images/invaders-hippo-collide.png)

\--- /task \---

ಆಕಾಶನೌಕೆ ಸ್ಫೋಟಗೊಂಡ ನಂತರ, ಹೊಸ `Hippo`clones ಗೋಚರಿಸುತ್ತವೆ, ಆದರೆ ಆಕಾಶನೌಕೆ ಇನ್ನೂ ಸ್ಫೋಟಗೊಂಡಿದೆ! ಆಕಾಶನೌಕೆ ಹೊಡೆದ ನಂತರ ಸ್ವತಃ ಮರುಹೊಂದಿಸಬೇಕಾಗಿದೆ.

\--- task \---

ಹಿಪ್ಪೋಗಳು ಮತ್ತೆ ಕಾಣಿಸಿಕೊಳ್ಳಲು ಪ್ರಾರಂಭಿಸುವ ಮೊದಲು ಸಣ್ಣ ವಿರಾಮವನ್ನು ರಚಿಸಲು `wait`{:class="block3control"} block ಅನ್ನು `Spaceship` sprite's ಕೋಡ್ ಸೇರಿಸಿ. ನಂತರ ಕೋಡ್ ಅನ್ನು ಪದೇ ಪದೇ run ಮಾಡಲು `forever`{:class="block3control"} ಬ್ಲಾಕ್ ಅನ್ನು ನಿಮ್ಮ ಎಲ್ಲಾ ಕೋಡ್ ಸುತ್ತಲೂ ಸೇರಿಸಿ.

![rocket sprite](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (hit v)
broadcast (hit v)

+ wait (1) seconds
end
```

\--- /task \---