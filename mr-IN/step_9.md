## स्पेस-बॅट

आपला खेळ जरा कठीण करण्यासाठी आपण स्पेसशिपवर संत्री फेकणारी बॅट तयार करणार आहात.

![a bat throwing an orange at the spaceship](images/bat-oranges.png)

--- task ---

आता एक `Bat` sprite जोडा आणि त्याची फिरण्याची शैली **left-right** कडे सेट करा.

--- /task ---

--- task ---

एक `Bat` sprite बनवा आणि त्याला `move`{:class="block3motion"} डावीकडुन ऊजवीकडे आणि स्टेज च्या वरती `forever`{:class="block3control"}.

![bat sprite](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

आपल्या कोडची चाचणी करणे लक्षात ठेवा.

--- /task ---

जर आपण बॅटच्या (bat) पोशाखांकडे पाहिले तर आपण पाहू शकता की यात चार वेगवेगळ्या वस्तू आहेत:

![screenshot](images/invaders-bat-costume.png)

--- task ---

`next costume`{:class="block3looks"} चा वापर बॅटचे पंख फडफडण्यासाठी करा.

--- hints ---


--- hint ---

बॅट हलविल्यानंतर, त्याने `next coustume`{:class="block3looks"} आणि नंतर थोड्या काळासाठी `wait`{:class="block3control"} दर्शविले पाहिजे.

--- /hint ---

--- hint ---

आपल्याला कोडमध्ये हे ब्लॉक्स जोडण्याची आवश्यकता आहे:

```blocks3
wait (0.3) seconds

next costume
```

--- /hint ---

--- hint ---

आपला कोड असा दिसला पाहिजे:

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

--- /hint ---

--- /hints ---

--- /task ---

आता बॅटने संत्री फेका!

--- task ---

एक `Orange` sprite scratch लायब्ररीतून जोडा.

![screenshot](images/invaders-orange.png)

--- /task ---

--- task ---

आपल्या बॅटमध्ये कोड जोडा जेणेकरून `when the flag is clicked`{:class="block3events"}, `Bat` sprite `forever`{:class="block3control"} `waits` `random`{:class="block3operators"} `5 to 10`{:class="block3operators"} दरम्यान कालावधी सेकंद आणि नंतर `creates a clone`{:class="block3control"} चे `Orange` sprite.

![bat sprite](images/bat-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (5) to (10)) secs
    create clone of (Orange v)
end
```

--- /task ---

--- task ---

`Orange` मध्ये कोड जोडा `Bat` पासून प्रारंभ करुन त्याचे प्रत्येक क्लोन ड्रॉप करण्यासाठी स्टेजच्या तळाशी sprite आणि खाली पडणे.

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

--- /task ---

--- task ---

`Orange` sprite मध्ये आणखी काही कोड जोडा जेणेकरून जेव्हा `Orange` क्लोन `Spaceship` ला हिट करते sprite, खेळाडूला रीसेट करण्याची संधी देण्यासाठी क्लोन देखील अदृश्य होतो:

![orange sprite](images/orange-sprite.png)

```blocks3
    when I receive [hit v]
    delete this clone
```

--- /task ---

--- task ---

आपल्या `Spaceship` कोड सुधारित करा sprite जेणेकरुन `Hippo` ला स्पर्श करते तेव्हा sprite "hit" होते sprite किंवा एक `Orange` sprite:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    wait until < <touching (Hippo1 v)?> or <touching (Orange v)?>>
```

--- /task ---

--- task ---

आपल्या खेळाची चाचणी घ्या. जर स्पेसशिपवर कोसळणार्‍या संत्राचा परिणाम झाला तर काय होईल?

--- /task ---