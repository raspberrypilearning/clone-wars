## ಸ್ಪೇಸ್-ಬ್ಯಾಟ್

ನಿಮ್ಮ ಆಟವನ್ನು ಸ್ವಲ್ಪ ಕಠಿಣವಾಗಿಸಲು, ನೀವು ಆಕಾಶನೌಕೆಗೆ ಕಿತ್ತಳೆ ಎಸೆಯುವ ಬ್ಯಾಟ್ ಅನ್ನು ರಚಿಸಲಿದ್ದೀರಿ.

![a bat throwing an orange at the spaceship](images/bat-oranges.png)

\--- task \---

`Bat` sprite ಮತ್ತು ಅದರ ತಿರುಗುವಿಕೆಯ ಶೈಲಿಯನ್ನು **left-right** ಹೊಂದಿಸಿ.

\--- /task \---

\--- task \---

`Bat`ಅನ್ನು `forever`{:class="block3control"} ಮೇಲಿನ ಹಂತದಲ್ಲಿ sprite ಅನ್ನು ಎಡದಿಂದ ಬಲಕ್ಕೆ `move`{:class="block3motion"}.

![bat sprite](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

ನಿಮ್ಮ ಕೋಡ್ ಅನ್ನು ಪರೀಕ್ಷಿಸುವುದನ್ನು ಮರೆಯದಿರಿ.

\--- /task \---

ನೀವು ಬ್ಯಾಟ್‌ನ costumes ನೋಡಿದರೆ, ಅದು ನಾಲ್ಕು ವಿಭಿನ್ನವಾದವುಗಳನ್ನು ಹೊಂದಿದೆ ಎಂದು ನೀವು ನೋಡಬಹುದು:

![screenshot](images/invaders-bat-costume.png)

\--- task \---

ಚಲಿಸುವಾಗ ಬ್ಯಾಟ್ ತನ್ನ ರೆಕ್ಕೆಗಳನ್ನು ಬೀಸುವಂತೆ ಮಾಡಲು `next costume`{:class="block3looks"} ಬ್ಲಾಕ್ ಅನ್ನು ಉಪಯೋಗಿಸಿರಿ.

\--- hints \---

\--- hint \---

ಬ್ಯಾಟ್ ಚಲಿಸಿದ ನಂತರ, ಅದು `next costume`{:class="block3looks"} ತೋರಿಸಬೇಕು ಮತ್ತು ನಂತರ ಅಲ್ಪಾವಧಿಗೆ `wait`{:class="block3control"}.

\--- /hint \---

\--- hint \---

ಈ ಬ್ಲಾಕ್ ಗಳನ್ನು ನಿಮ್ಮ ಕೋಡ್ ಗೆ ಸೇರಿಸಬೇಕಾಗುತ್ತದೆ:

```blocks3
wait (0.3) seconds

next costume
```

\--- /hint \---

\--- hint \---

ನಿಮ್ಮಕೋಡ್ ಈ ರೀತಿ ಕಾಣಿಸಬೇಕು:

```blocks3
when flag clicked
set size to (50) %
forever
move (10) steps
if on edge, bounce

+ next costume
+ wait (0.3) seconds
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

ಈಗ ನಿಮ್ಮ ಬ್ಯಾಟ್, ಕಿತ್ತಳೆಯನ್ನು ಎಸೆಯುವಂತೆ ಮಾಡಿ!

\--- task \---

Scratch ಲೈಬ್ರರಿಯಿಂದ ` Orange` sprite ಸೇರಿಸಿ.

![screenshot](images/invaders-orange.png)

\--- /task \---

\--- task \---

ನಿಮ್ಮ ಬ್ಯಾಟ್‌ಗೆ ಕೋಡ್ ಸೇರಿಸಿ ಇದರಿಂದ `when the flag is clicked`{:class="block3events"}, `Bat`sprite `forever`{:class="block3control"} `waits`{:class="block3control"} `random`{:class="block3operators"} `5 to 10`{:class="block3operators"} seconds and then`creates a clone` `Orange ` sprite{:class="block3control"}.

![bat sprite](images/bat-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (5) to (10)) secs
    create clone of (Orange v)
end
```

\--- /task \---

\--- task \---

`Bat` sprite ಪ್ರಾರಂಭಿಸಿ ಮತ್ತು ಹಂತದ ಕೆಳಭಾಗಕ್ಕೆ ಬೀಳುವ ಅದರ ಪ್ರತಿಯೊಂದು clone ಡ್ರಾಪ್ ಮಾಡಲು ಕೋಡ್ ಅನ್ನು `Orange` ಗೆ ಸೇರಿಸಿ.

![orange sprite](images/orange-sprite.png)

```blocks3
    when flag clicked
    hide

    when I start as a clone
    go to (Bat v)
    show
    repeat until <touching (edge v)?
        change y by (-4)
    end
    delete this clone
```

\--- /task \---

\--- task \---

`Orange` sprite ಇನ್ನೂ ಕೆಲವು ಕೋಡ್ ಸೇರಿಸಿ ಇದರಿಂದ `Orange` clone `Spaceship` sprite ಹೊಡೆದಾಗ, ಆಟಗಾರನಿಗೆ ಮರುಹೊಂದಿಸಲು ಅವಕಾಶ ನೀಡಲು clone ಸಹ ಕಣ್ಮರೆಯಾಗುತ್ತದೆ:

![orange sprite](images/orange-sprite.png)

```blocks3
    when I receive [hit v]
    delete this clone
```

\--- /task \---

\--- task \---

ನಿಮ್ಮ `Spaceship`sprite ಕೋಡ್ ಅನ್ನು ಮಾರ್ಪಡಿಸಿ ಇದರಿಂದ sprite `Hippo`sprite ಅಥವಾ `Orange` sprite ಅನ್ನು ಮುಟ್ಟಿದಾಗ ಅದು "hit" ಆಗುತ್ತದೆ:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    wait until < <touching (Hippo1 v)?> or <touching (Orange v)?>>
```

\--- /task \---

\--- task \---

ನಿಮ್ಮ ಆಟವನ್ನು ಪರೀಕ್ಷಿಸಿ. ಬೀಳುವ ಕಿತ್ತಳೆಯಿಂದ ಆಕಾಶನೌಕೆ ಹೊಡೆದರೆ ಏನಾಗುತ್ತದೆ?

\--- /task \---