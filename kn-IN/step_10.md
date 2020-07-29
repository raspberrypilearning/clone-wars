## ಆಟ ಮುಗಿದಿದೆ

ಮುಂದೆ, ನೀವು ಆಟದ ಕೊನೆಯಲ್ಲಿ ''game over' ಸಂದೇಶವನ್ನು ಸೇರಿಸುತ್ತೀರಿ.

\--- task \---

ನೀವು ಈಗಾಗಲೇ ಇಲ್ಲದಿದ್ದರೆ, `lives` {:class="block3variables"}ಎಂಬ ಹೊಸ variable ಅನ್ನು ರಚಿಸಿ.

ನಿಮ್ಮ ಆಕಾಶನೌಕೆ ಮೂರು ಜೀವಗಳಿಂದ ಪ್ರಾರಂಭವಾಗಬೇಕು ಮತ್ತು ಅದು ಹಿಪ್ಪೋ ಅಥವಾ ಕಿತ್ತಳೆಯನ್ನು ಮುಟ್ಟಿದಾಗಲೆಲ್ಲಾ ಜೀವವನ್ನು ಕಳೆದುಕೊಳ್ಳಬೇಕು. `lives`{:class="block3variables"} ಮುಗಿದಮೇಲೆ ನಿಮ್ಮ ಆಟ ನಿಲ್ಲುತ್ತದೆ.

\--- /task \---

\--- task \---

**text** ಉಪಕರಣವನ್ನು ಬಳಸಿಕೊಂಡು `Game Over` ಎಂಬ ಹೊಸ sprite ಅನ್ನು ರಚಿಸಿ.

![screenshot](images/invaders-game-over.png)

\--- /task \---

\--- task \---

ವೇದಿಕೆ ಮೇಲೆ, ಆಟ ಮುಗಿಯುವ ಮುನ್ನ `game over`{:class="block3events"} ಎನ್ನುವ ಸಂದೇಶವನ್ನು ಪ್ರಸಾರ ಮಾಡಿ.

![gameover sprite](images/stage-sprite.png)

```blocks3
broadcast (game over v) and wait
```

\--- /task \---

\--- task \---

ಈ ಕೋಡ್ ಅನ್ನು ನಿಮ್ಮ `Game Over` sprite ಗೆ ಸೇರಿಸಿ ಇದರಿಂದ ಅದು ಆಟದ ಕೊನೆಯಲ್ಲಿ ತೋರಿಸುತ್ತದೆ:

![gameover sprite](images/gameover-sprite.png)

```blocks3
when flag clicked
hide

when I receive [game over v]
show
```

ನಿಮ್ಮ ಹಂತದಲ್ಲಿ ನೀವು `broadcast (game over) and wait`{:class="block3events"}ಬ್ಲಾಕ್ ಅನ್ನು ಬಳಸಿದ್ದರಿಂದ, ಆಟ ಮುಗಿಯುವ ಮುನ್ನ ಹಂತವು `Game Over` sprite ಅನ್ನು ತೋರಿಸುವುದಕ್ಕಾಗಿ ಕಾಯುತ್ತದೆ.

\--- /task \---

\--- task \---

ನಿಮ್ಮ ಆಟವನ್ನು ಪರೀಕ್ಷಿಸಿ. ನೀವು ಎಷ್ಟು ಅಂಕಗಳನ್ನು ಗಳಿಸಬಹುದು? ಆಟವು ತುಂಬಾ ಸುಲಭ ಅಥವಾ ತುಂಬಾ ಕಠಿಣವಾಗಿದ್ದರೆ, ಅದನ್ನು ಸುಧಾರಿಸುವ ಮಾರ್ಗಗಳ ಬಗ್ಗೆ ನೀವು ಯೋಚಿಸಬಹುದೇ?

\--- /task \---