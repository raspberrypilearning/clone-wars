## स्पेसशिपचा स्फोट

जेव्हा हिप्पो आपल्या स्पेसशिपला स्पर्श करते तेव्हा स्पेसशिपचा स्फोट झाला पाहिजे!

\--- task \---

`Spaceship` sprite निवडा त्याचे पोशाख 'normal' असे करा आणि नाव बदला.

\--- /task \---

\--- task \---

विस्फोटित स्पेसशिपचा दुसरा पोशाख काढा आणि नवीन पोशाखला 'हिट' म्हणा.

![screenshot](images/invaders-spaceship-costumes.png)

आपल्याला स्फोट काढायचा नसल्यास आपण scratch लायब्ररीमधून 'Sun' पोशाख निवडू शकता आणि नंतर **Color a shape** वापरून पोशाखाचा रंग आणि चेहरा बदलण्याचे साधन.

![screenshot](images/invaders-sun.png)

\--- /task \---

\--- task \---

आपल्या `Spaceship` Sprite मध्ये काही कोड जोडा जेणेकरून खेळ सुरू झाल्यावर ते 'सामान्य' पोशाख प्रदर्शित करते आणि जेव्हा हिप्पोला स्पर्श करते तेव्हा 'हिट' पोशाखात बदलते:

![rocket sprite](images/rocket-sprite.png)

```blocks3
when flag clicked
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (hit v)
```

\--- /task \---

\--- task \---

आपल्या कोडची चाचणी घ्या. स्पेसशिपला हिप्पोने टक्कर द्या. स्पेसशिप 'hit' पोशाखात बदलते?

\--- /task \---