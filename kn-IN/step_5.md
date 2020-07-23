## ಸ್ಪೇಸ್-ಹಿಪ್ಪೋಸ್

ಈಗ ನೀವು ನಿಮ್ಮ ಆಕಾಶನೌಕೆಯನ್ನು ನಾಶಮಾಡಲು ಪ್ರಯತ್ನಿಸುವ ಸಾಕಷ್ಟು ಹಾರುವ ಹಿಪ್ಪೋಗಳನ್ನು ಸೇರಿಸಲು ಹೊರಟಿದ್ದೀರಿ.

--- task ---

Scratch ಲೈಬ್ರರಿಯಲ್ಲಿ 'hippo 1' ಚಿತ್ರದ ಜೊತೆಗೆ ಹೊಸ sprite ಅನ್ನು ರಚಿಸಿ. `Hippo` sprite ಅನ್ನು `Spaceship` sprite ಹೋಲುವಂತೆ ಮಾಡಲು **shrink** ಉಪಕರಣವನ್ನು ಬಳಸಿ.

![screenshot](images/invaders-hippo.png)

--- /task ---

--- task ---

`Hippo` sprite ನ ತಿರುಗುವಿಕೆಯ ಶೈಲಿಯನ್ನು **left-right** ಗೆ ಹೊಂದಿಸಿ.

[[[generic-scratch3-sprite-rotation-style]]]

--- /task ---

--- task ---

ಆಟ ಪ್ರಾರಂಭವಾದಾಗ `Hippo` sprite ಅನ್ನು ಮರೆಮಾಡಲು ಕೆಲವು ಕೋಡ್ ಸೇರಿಸಿ.

![hippo sprite](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

--- task ---

ಪ್ರತಿ ಕೆಲವು ಸೆಕೆಂಡುಗಳಲ್ಲಿ ಹೊಸ `Hippo` clone ರಚಿಸಲು ಹಂತಕ್ಕೆ ಕೆಲವು ಕೋಡ್ ಸೇರಿಸಿ.

--- hints ---


--- hint ---

ಯಾವಾಗ `green flag is clicked` {:class="block3events"}, `repeatedly`{:class="block3control"} `wait`{:class="block3control"} `between 2 and 4 seconds ` {:class="block3operators"} ತದನಂತರ `create a clone of the Hippo sprite` {:class="block3control"}.

--- /hint ---

--- hint ---

ನಿಮಗೆ ಅಗತ್ಯವಿರುವ ಬ್ಲಾಕ್ ಗಳು ಇಲ್ಲಿವೆ:

```blocks3
forever
end

create clone of (Hippo1 v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

--- /hint ---

--- hint ---

ನಿಮ್ಮ ಹೊಸ ಕೋಡ್ ಹೇಗಿರಬೇಕು ಎಂಬುದು ಇಲ್ಲಿದೆ:

![stage sprite](images/stage-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (2) to (4)) secs
    create clone of (Hippo1 v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

ಪ್ರತಿಯೊಂದು ಹೊಸ ಹಿಪ್ಪೋ clone ಮನ ಬಂದಂತಹ `x` ಸ್ಥಾನದಲ್ಲಿ ಕಾಣಬೇಕು, ಮತ್ತು ಪ್ರತಿ clone ಯಾದೃಚ್ ವೇಗವನ್ನು ಹೊಂದಿರಬೇಕು.

--- task ---

`Hippo` sprite ಗೆ ಮಾತ್ರ ಬೇಕಾಗಿರುವ `speed`{:class="block3variables"} ಎಂಬ ಹೊಸ variable ಅನ್ನು ತಯಾರಿಸಿ.

[[[generic-scratch3-add-variable]]]

ನೀವು ಇದನ್ನು ಸರಿಯಾಗಿ ಮಾಡಿದಾಗ, variable ನ ಪಕ್ಕದಲ್ಲಿ sprite ನ ಹೆಸರನ್ನು ಹೊಂದಿರುತ್ತದೆ, ಈ ರೀತಿಯಾಗಿ:

![screenshot](images/invaders-var-test.png)

--- /task ---

--- task ---

ಪ್ರತಿ `Hippo` clone ಪ್ರಾರಂಭವಾದಾಗ, ಯಾದೃಚ್ ವೇಗ ಮತ್ತು ಅದಕ್ಕಾಗಿ ಪ್ರಾರಂಭದ ಸ್ಥಳವನ್ನು ಆರಿಸಿ. ನಂತರ ಪರದೆಯ ಮೇಲೆ clone ತೋರಿಸಿ.

```blocks3
when I start as a clone
set [speed v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

--- /task ---

--- task ---

ನಿಮ್ಮ ಕೋಡ್ ಅನ್ನು ಪರೀಕ್ಷಿಸಿ. ಪ್ರತಿ ಕೆಲವು ಸೆಕೆಂಡುಗಳಲ್ಲಿ ಹೊಸ ಹಿಪ್ಪೋ ಕಾಣಿಸಿಕೊಳ್ಳುತ್ತದೆಯೇ?

--- /task ---

ಈ ಸಮಯದಲ್ಲಿ ಹಿಪ್ಪೋಗಳು ಚಲಿಸುವುದಿಲ್ಲ.

--- task ---

ಪ್ರತಿ ಹಿಪ್ಪೋ ಮಿಂಚಿನ ಹೊಡೆತಕ್ಕೆ ಸಿಲುಕುವವರೆಗೆ ಯಾದೃಚ್ ತಿರುಗಬೇಕು. ಹಾಗೆ ಆಗಬೇಕಾದರೆ, ಈ ಕೋಡ್ ಅನ್ನು ಈಗಾಗಲೇ `Hippo` sprite ನ code script ನಲ್ಲಿರುವ ಕೆಳಗಿನ ಬ್ಲಾಕ್ ನಲ್ಲಿ ಲಗತ್ತಿಸಿರಿ:

```blocks3
repeat until <touching (lightning v) ?>
	move (speed :: variables) steps
	turn right (pick random (-10) to (10)) degrees
	if on edge, bounce
end
delete this clone
```

--- /task ---

--- task ---

ನಿಮ್ಮಕೋಡ್ ಅನ್ನು ಮತ್ತೆ ಪರೀಕ್ಷಿಸಿ. ಪ್ರತಿ ಕೆಲವು ಸೆಕೆಂಡುಗಳಲ್ಲಿ ಹೊಸ ಹಿಪ್ಪೋ clone ಕಾಣಿಸಿಕೊಳ್ಳುವುದನ್ನು ನೀವು ನೋಡಬೇಕು, ಮತ್ತು ಪ್ರತಿ clone ಬೇರೆ ವೇಗದಲ್ಲಿ ಚಲಿಸಬೇಕು.

--- no-print ---

![screenshot](images/hippo-clones.gif)

--- /no-print ---

--- /task ---

--- task ---

ಈಗ ಆಕಾಶನೌಕೆಯ ಲೇಸರ್ ಫಿರಂಗಿಯನ್ನು ಪರೀಕ್ಷಿಸಿ. ಮಿಂಚಿನ ಹಿಪ್ಪೋವನ್ನು ಹೊಡೆದರೆ, ಹಿಪ್ಪೋ ಕಣ್ಮರೆಯಾಗುತ್ತದೆಯೇ?

--- /task ---