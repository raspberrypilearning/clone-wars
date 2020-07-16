## ಆಕಾಶನೌಕೆ ಸ್ಫೋಟ

ಹಿಪ್ಪೋ ನಿಮ್ಮ ಆಕಾಶನೌಕೆಯನ್ನು ಮುಟ್ಟಿದಾಗ, ಆಕಾಶನೌಕೆ ಸ್ಫೋಟಗೊಳ್ಳಬೇಕು!

\--- task \---

`Spaceship`sprite ಆಯ್ಕೆಮಾಡಿ ಮತ್ತು ಅದರ ವೇಷಭೂಷಣ 'normal' ಎಂದು ಮರುಹೆಸರಿಸಿ.

\--- /task \---

\--- task \---

ಸ್ಫೋಟಗೊಳ್ಳುವ ಆಕಾಶನೌಕೆಯ ಮತ್ತೊಂದು ವೇಷಭೂಷಣವನ್ನು ಎಳೆಯಿರಿ, ಮತ್ತು ಹೊಸ ವೇಷಭೂಷಣ 'hit' ಎಂದು ಕರೆಯಿರಿ.

![screenshot](images/invaders-spaceship-costumes.png)

ನೀವು ಸ್ಫೋಟವನ್ನು ಸೆಳೆಯಲು ಬಯಸದಿದ್ದರೆ, ನೀವು Scratch ಲೈಬ್ರರಿಯಿಂದ 'sun' ವೇಷಭೂಷಣವನ್ನು ಆಯ್ಕೆ ಮಾಡಬಹುದು, ತದನಂತರ ವೇಷಭೂಷಣದ ಬಣ್ಣ ಮತ್ತು ಮುಖವನ್ನು ಬದಲಿಸಲು **color a shape** ಸಾಧನವನ್ನು ಬಳಸಿರಿ.

![screenshot](images/invaders-sun.png)

\--- /task \---

\--- task \---

ನಿಮ್ಮ `spaceship` sprite ಕೆಲವು code ಸೇರಿಸಿ ಇದರಿಂದ ಅದು ಆಟ ಪ್ರಾರಂಭವಾದಾಗ 'normal' ವೇಷಭೂಷಣವನ್ನು ತೋರಿಸುತ್ತದೆ ಮತ್ತು ಹಿಪ್ಪೋವನ್ನು ಮುಟ್ಟಿದಾಗ 'hit' ವೇಷಭೂಷಣ ಬದಲಾಗುತ್ತದೆ:

![rocket sprite](images/rocket-sprite.png)

```blocks3
when flag clicked
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (hit v)
```

\--- /task \---

\--- task \---

ನಿಮ್ಮ ಕೋಡ್ ಅನ್ನು ಪರೀಕ್ಷಿಸಿ. ಆಕಾಶನೌಕೆ ಹಿಪ್ಪೋಗೆ ಡಿಕ್ಕಿ ಹೊಡೆಯುವಂತೆ ಮಾಡಿ. ಆಕಾಶನೌಕೆ 'hit' ವೇಷಭೂಷಣ ಬದಲಾಗುತ್ತದೆಯೇ?

\--- /task \---