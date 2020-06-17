## दरियाई-घोड़े जो गायब हो जाते हैं

जब अंतरिक्ष यान फटता है, तो सभी हिप्पो को गायब हो जाना चाहिए ताकि गेम के खिलाड़ी ठीक हो सकें।

--- task ---

अपने 'spaceship' स्प्राइट में कुछ कोड जोड़ें जिससे कि वह दरियाई-घोड़े को छूने पर 'hit' संदेश प्रसारित कर सके ।

![रॉकेट स्प्राइट](images/rocket-sprite.png)

```blocks3
when flag clicked
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (hit v)
+ broadcast (hit v)
```

--- /task ---

--- task ---

सभी `Hippo` स्प्राइट क्लोन को "hit" संदेश प्राप्त होगा, और आप इस कोड को `Hippo` स्प्राइट में जोड़कर, अंतरिक्ष-यान से टक्कर होने पर, उन्हें गायब होने का निर्देश दे सकते हैं ।

![hippo स्प्राइट](images/hippo-sprite.png)

```blocks3
when I receive [hit v]
delete this clone
```

--- /task ---

--- task ---

यह जांचने के लिए कि नया कोड काम करता है या नहीं, हरी झंडी पर क्लिक करें और अंतरिक्ष-यान की दरियाई-घोड़े से टक्कर कराएं।

![स्क्रीनशॉट](images/invaders-hippo-collide.png)

--- /task ---

अंतररिक्ष-यान के फटने के बाद, नए `Hippo` क्लोन दिखाई देते हैं, लेकिन अंतरिक्ष-यान अभी भी फटा हुआ है! अंतरिक्ष-यान की टक्कर होने के बाद उसे खुद को फिर से पुरानी अवस्था में लाना होगा ।

--- task ---

`Spaceship` स्प्राइट के कोड के अंत में `wait`{:class="block3control"} ब्लॉक जोड़ें जिससे दरियाई-घोड़े पुनः प्रदर्शित होने से पहले एक छोटा सा अंतराल जोड़ा जा सके । उसके बाद, कोड को लगातार चलते रहने देने के लिए अपने कोड को `forever`{:class="block3control"} ब्लॉक से बंद करें ।

![रॉकेट स्प्राइट](images/rocket-sprite.png)

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

--- /task ---