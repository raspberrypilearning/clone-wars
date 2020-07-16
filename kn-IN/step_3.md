## ಮಿಂಚಿನ ಬೋಲ್ಟ್

ಈಗ ನೀವು ಆಕಾಶನೌಕೆಗೆ ಮಿಂಚಿನ ಬೋಲ್ಟ್ಗಳನ್ನು ಹಾರಿಸುವ ಸಾಮರ್ಥ್ಯವನ್ನು ನೀಡಲಿದ್ದೀರಿ!

\--- task \---

Scratch ಲೈಬ್ರರಿಯಿಂದ `Lightning`sprite ಅನ್ನು ಸೇರಿಸಿ.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

ಆಟ ಪ್ರಾರಂಭವಾದಾಗ, `Lightning` ಆಕಾಶನೌಕೆ ತನ್ನ ಲೇಸರ್ ಫಿರಂಗಿಗಳನ್ನು ಹಾರಿಸುವವರೆಗೆ sprite ಅನ್ನು ಮರೆಮಾಡಬೇಕು.

ಈ code ಅನ್ನು `Lightning` sprite ಗೆ ಸೇರಿಸಿ:

![lightning sprite](images/lightning-sprite.png)

```blocks3
ಹಸಿರು ಧ್ವಜ ಒತ್ತಿದರೆ
ಮರೆಯಾಗಿ
```

\--- /task \---

ಈ ಸಮಯದಲ್ಲಿ, ಆಕಾಶನೌಕೆಗೆ ಹೋಲಿಸಿದರೆ ಮಿಂಚಿನ ಬೋಲ್ಟ್ ನಿಜವಾಗಿಯೂ ದೊಡ್ಡದಾಗಿದೆ!

\--- task \---

`Lightning`sprite ಈಗಾಗಲೇ ಹೊಂದಿರುವ ಕೋಡ್ ಕೆಳಗೆ, sprite ಅನ್ನು ಚಿಕ್ಕದಾಗಿಸಲು ಮತ್ತು ಅದನ್ನು ತಲೆಕೆಳಗಾಗಿ ಮಾಡಲು ಕೆಲವು ಬ್ಲಾಕ್ ಗಳನ್ನು.

![lightning sprite](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

ಈಗ ಅದು ಆಕಾಶನೌಕೆಯಿಂದ pointy end-first ಅನ್ನು ಹಾರಿಸುತ್ತದೆ ಎಂದು ತೋರುತ್ತಿದೆ.

\--- /task \---

\--- task \---

<kbd>space</kbd> ಕೀಲಿಯನ್ನು ಒತ್ತಿದರೆ lightning bolt ನ ಹೊಸ clone ರಚಿಸಲು `Spaceship` sprite ಗೆ ಹೊಸ ಕೋಡ್ ಸೇರಿಸಿ.

\--- hints \---

\--- hint \---

`ಹಸಿರು ಧ್ವಜದ ಮೇಲೆ ಒತ್ತಿದರೆ `{:class="block3events"},`forever` {:class="block3control"} `if` {:class="block3control"} `ಕೀಲಿ ಒತ್ತಿದರೆ`{:class="block3sensing"}, ಮತ್ತು ಆ ಸಂದರ್ಭದಲ್ಲಿ `create a clone of the Lightning`{:class="block3control "} sprite.

\--- /hint \---

\--- hint \---

ನಿಮಗೆ ಅಗತ್ಯವಿರುವ ಬ್ಲಾಕ್ ಗಳು ಇಲ್ಲಿವೆ:

```blocks3
if <> then
end

forever
end

create clone of (Lightning v)

<key (space v) pressed?>

when flag clicked
```

\--- /hint \---

\--- hint \---

ನಿಮ್ಮ ಹೊಸ ಕೋಡ್ ಹೇಗಿರಬೇಕು ಎಂಬುದು ಇಲ್ಲಿದೆ:

![rocket sprite](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
    if <key (space v) pressed?> then
        create clone of (Lightning v)
    end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

ಆಟವು `Lightning` sprite clone ರಚಿಸಿದಾಗಲೆಲ್ಲಾ, clone ಗೋಚರಿಸಬೇಕು ಮತ್ತು ಅದು ಹಂತದ ಮೇಲ್ಭಾಗವನ್ನು ತಲುಪುವವರೆಗೆ ಮೇಲಕ್ಕೆ ಚಲಿಸಬೇಕು. ನಂತರ clone ಕಣ್ಮರೆಯಾಗಬೇಕು.

ಈ ಕೋಡ್ ಅನ್ನು `Lightning` sprite ಗೆ ಸೇರಿಸಿ ಇದರಿಂದ ಅದರ clones ಹಂತದ ಅಂಚನ್ನು ಮುಟ್ಟುವವರೆಗೆ ಮೇಲಕ್ಕೆ ಚಲಿಸುತ್ತವೆ ಮತ್ತು ನಂತರ ಅವು ಅಳಿಸಿಹೋಗುತ್ತವೆ.

![lightning sprite](images/lightning-sprite.png)

```blocks3
    when I start as a clone
    go to (Spaceship v)
    show
    repeat until <touching (edge v) ?>
        change y by (10)
    end
    delete this clone
```

\--- /task \---

\--- task \---

lightning bolt ಸರಿಯಾಗಿ ಚಲಿಸುತ್ತದೆಯೇ ಎಂಬುದನ್ನು ಪರೀಕ್ಷಿಸಲು <kbd>space</kbd> ಅನ್ನು ಒತ್ತಿರಿ.

\--- /task \---