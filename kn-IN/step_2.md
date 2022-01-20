## ಆಕಾಶನೌಕೆ ಮಾಡಿ

ಮೊದಲು ಭೂಮಿಯನ್ನು ರಕ್ಷಿಸಬಲ್ಲ ಆಕಾಶನೌಕೆ ಮಾಡಿ!

--- task ---

'Clone wars' Scratch starter ಯೋಜನೆಯನ್ನು ತೆರೆಯಿರಿ.

**ಆನ್‌ಲೈನ್:** [rpf.io/clone-ware-on](https://rpf.io/clone-wars-on){:target="blank"} ನಲ್ಲಿ ಪ್ರಾರಂಭ ಯೋಜನೆಯನ್ನು ತೆರೆಯಿರಿ.

ನೀವು Scratch ಖಾತೆಯನ್ನು ಹೊಂದಿದ್ದರೆ **Remix** ಕ್ಲಿಕ್ ಮಾಡುವ ಮೂಲಕ ನೀವು ನಕಲನ್ನು ಮಾಡಬಹುದು.

**ಆಫ್‌ಲೈನ್:** [rpf.io/p/kn-IN/clone-wars-go](https://rpf.io/p/kn-IN/clone-wars-go) ನಿಂದ ಪ್ರಾರಂಭ ಯೋಜನೆಯನ್ನು ಡೌನ್‌ಲೋಡ್ ಮಾಡಿ, ತದನಂತರ ಅದನ್ನುOffline editor ಬಳಸಿ ತೆರೆಯಿರಿ.

ನಿಮಗೆ Scratch offline editor ಅನ್ನು download ಮತ್ತು install ಮಾಡಬೇಕಾಗಿದ್ದಲ್ಲಿ, ಅದನ್ನು [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="blank"} ಇಲ್ಲಿ ಹುಡುಕಬಹುದು.

--- /task ---

![starter project](images/starter-project.png)

--- task ---

<kbd>left</kbd> ಬಾಣವನ್ನು ಒತ್ತಿದರೆ ಆಕಾಶನೌಕೆ ಎಡಕ್ಕೆ ಚಲಿಸುವಂತೆ ಮಾಡಲು ಈ ಕೋಡ್ ಅನ್ನು ಆಕಾಶನೌಕೆ sprite ಗೆ ಸೇರಿಸಿ:

![ರಾಕೆಟ್ sprite](images/rocket-sprite.png)

```blocks3
    when flag clicked
    forever
        if <key (left arrow v) pressed?> then
            change x by (-4)
        end
    end
```

X- ಅಕ್ಷವು ಹಂತದ ಎಡಭಾಗದಿಂದ ಬಲಭಾಗಕ್ಕೆ ಹೋಗುತ್ತದೆ. ಇದರರ್ಥ ನೀವು ಆಕಾಶನೌಕೆ sprite ನ `x` ಸ್ಥಾನದ ಮೌಲ್ಯದಿಂದ ಕಳೆಯುವಾಗ ಆಕಾಶನೌಕೆ ಎಡಕ್ಕೆ ಚಲಿಸುತ್ತದೆ. ಆದ್ದರಿಂದ ಈ ಕೋಡ್ ಬ್ಲಾಕ್ ನಿಮ್ಮ ಆಕಾಶನೌಕೆ ಎಡಕ್ಕೆ ಚಲಿಸುವಂತೆ ಮಾಡುವ ಭಾಗವಾಗಿದೆ:

```blocks3
change x by (-4)
```

--- /task ---

--- task ---

<kbd>right</kbd> ಬಾಣದ ಕೀಲಿಯನ್ನು ಒತ್ತಿದರೆ ನಿಮ್ಮ ಆಕಾಶನೌಕೆ ಬಲಕ್ಕೆ ಚಲಿಸುವಂತೆ ಮಾಡಲು `forever`{:class="block3control"}ಬ್ಲಾಕ್ ಒಳಗೆ ಇನ್ನೂ ಕೆಲವು ಕೋಡ್ ಸೇರಿಸಿ.

--- hints ---


--- hint ---

ಆಕಾಶನೌಕೆಯ `x` ಸ್ಥಾನದಿಂದ `4` ಅನ್ನು ಕಳೆಯುವುದರಿಂದ ಅದು ಎಡಕ್ಕೆ ಚಲಿಸುವಂತೆ ಮಾಡಿತು, ಆದ್ದರಿಂದ ನೀವು ಆಕಾಶನೌಕೆಯನ್ನು `4` ಮೂಲಕ ಬಲಕ್ಕೆ ಚಲಿಸುವಂತೆ ಮಾಡುವುದು ಹೇಗೆ?

--- /hint ---

--- hint ---

ನಿಮಗೆ ಒಂದೇ ಕೋಡ್ ಬ್ಲಾಕ್ ಅಗತ್ಯವಿದೆ, ಆದರೆ ಬೇರೆ ಸಂಖ್ಯೆಯೊಂದಿಗೆ:

```blocks3
change x by ( )
```

--- /hint ---

--- hint ---

`forever`{:class="block3control"} ಬ್ಲಾಕ್ ಒಳಗೆ ಇತರೆ code ನ ಕೆಳಗೆ ನೀವು ಸೇರಿಸಬೇಕಾದ ಕೋಡ್ ಇಲ್ಲಿದೆ:

![ರಾಕೆಟ್ sprite](images/rocket-sprite.png)

```blocks3
if <key (right arrow v) pressed?> then
    change x by (4)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

ಹಸಿರು ಧ್ವಜವನ್ನು ಕ್ಲಿಕ್ ಮಾಡುವ ಮೂಲಕ ನಿಮ್ಮ ಯೋಜನೆಯನ್ನು ಪರೀಕ್ಷಿಸಿ. ನಿಮ್ಮ ಆಕಾಶನೌಕೆ ಎಡ ಮತ್ತು ಬಲಕ್ಕೆ ಚಲಿಸುವಂತೆ ಮಾಡಲು ನೀವು ಬಾಣದ ಕೀಲಿಗಳನ್ನು ಒತ್ತುವಿರಾ?

--- /task ---
