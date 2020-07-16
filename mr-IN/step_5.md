## स्पेस-हिप्पो

आता आपण बरेच उडणारे हिप्पोज जोडणार आहात जे आपले स्पेसशिप नष्ट करण्याचा प्रयत्न करतात.

\--- task \---

Scratch लायब्ररीत 'Hippo 1' प्रतिमेसह एक नवीन sprite तयार करा. **shrink** वापरा `Hippo` बनविण्याचे साधन `Spaceship`वर समान आकाराचे sprite करा.

![screenshot](images/invaders-hippo.png)

\--- /task \---

\--- task \---

`Hippo` sprite चे रोटेशन फिरवण्यासाठी स्टाइल **left-right** वर सेट करा.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

`Hippo` लपविण्यासाठी काही कोड जोडा. खेळ सुरू झाल्यावर स्प्राइट(sprite) करा.

![hippo sprite](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

\--- /task \---

\--- task \---

नवीन `Hippo` तयार करण्यासाठी स्टेजमध्ये काही कोड जोडा दर काही सेकंदात क्लोन करा.

\--- hints \---

\--- hint \---

जेव्हा `green flag is clicked`{:class="block3events"}, `repeatedly`{:class="block3control"} `wait`{:class="block3control"} `between 2 and 4 seconds`{:class="block3operators"} आणि नंतर `create a clone of the Hippo sprite`{:class="block3control"}.

\--- /hint \---

\--- hint \---

आपल्याला आवश्यक असलेले ब्लॉक येथे आहेत:

```blocks3
forever
end

create clone of (Hippo1 v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

\--- /hint \---

\--- hint \---

तुमचा कोड असा दिसला पाहिजे:

![stage sprite](images/stage-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (2) to (4)) secs
    create clone of (Hippo1 v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

प्रत्येक नवीन हिप्पो क्लोन यादृच्छिक(random) ` x` वर दिसला पाहिजे स्थिती आणि प्रत्येक क्लोनची यादृच्छिक गती असावी.

\--- task \---

`speed`{:class= "block3variables"} नावाचा नवीन व्हेरिएबल तयार करा. जे `Hippo` साठी आहे केवळ sprite साठी आहे.

[[[generic-scratch3-add-variable]]]

आपण हे योग्यरित्या पूर्ण केल्यावर, व्हेरिएबलच्या पुढे असलेल्या sprite चे नाव असे आहे:

![screenshot](images/invaders-var-test.png)

\--- /task \---

\--- task \---

जेव्हा प्रत्येक `Hippo` क्लोन सुरू होते, यादृच्छिक गती आणि त्यासाठी प्रारंभ करण्याचे ठिकाण निवडा. नंतर स्क्रीनवर क्लोन दर्शवा.

```blocks3
when I start as a clone
set [speed v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

\--- /task \---

\--- task \---

आपल्या कोडची चाचणी घ्या. दर काही सेकंदांत नवीन हिप्पो दिसतो का?

\--- /task \---

याक्षणी हिप्पोज हलत नाहीत.

\--- task \---

प्रत्येक हिप्पोला विजेच्या गाठीला धरुन येईपर्यंत यादृच्छिक हलवावे. ते करण्यासाठी, आधीपासून `Hippo` मध्ये असलेल्या ब्लॉक्सच्या खाली हा कोड जोडा sprite ची कोड स्क्रिप्ट:

```blocks3
repeat until <touching (lightning v) ?>
    move (speed :: variables) steps
    turn right (pick random (-10) to (10)) degrees
    if on edge, bounce
end
delete this clone
```

\--- /task \---

\--- task \---

आपल्या कोडची पुन्हा चाचणी घ्या. आपण दर काही सेकंदात नवीन हिप्पो क्लोन दिसला पाहिजे आणि प्रत्येक क्लोन वेगळ्या वेगाने हलला पाहिजे.

\--- no-print \---

![screenshot](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

आता स्पेसशिपच्या लेसर तोफांची चाचणी घ्या. जर विजेचा आवाज एखाद्या हिप्पोवर आदळला तर हिप्पो नाहीसा होतो का?

\--- /task \---