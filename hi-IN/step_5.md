## फ्लाइंग स्पेस-हिप्पोस

अब आप बहुत सारे फ्लाइंग हिप्पो जोड़ने जा रहे हैं जो आपके अंतरिक्ष यान को नष्ट करने का प्रयास करते हैं।

\--- task \---

Scratch लाइब्रेरी में 'Hippo1' इमेज के साथ एक नया स्प्राइट बनाएं। `Spaceship` स्प्राइट के आकर का `Hippo` स्प्राइट बनाने के लिए **shrink** टूल का प्रयोग करें।

![The Scratch stage with a starry background. A rocket sits in the middle at the bottom of the stage and a hippo sprite with wings is at the top.](images/invaders-hippo.png)

\--- /task \---

\--- task \---

`Hippo` स्प्राइट की रोटेशन शैली को **left-right** सेट करें |

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

गेम के शुरू होने पर `Hippo` को छिपाने के लिए कुछ कोड जोड़ते हैं |

![दरियाई-घोड़ा स्प्राइट](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

\--- /task \---

\--- task \---

हर सेकण्ड `Hippo` का एक नया क्लोन बनाने के लिए स्टेज में कुछ कोड जोड़ते हैं |

\--- hints \---

\--- hint \---

When the `green flag is clicked`{:class="block3events"}, `repeatedly`{:class="block3control"} `wait`{:class="block3control"} `between 2 and 4 seconds`{:class="block3operators"} और फिर `create a clone of the Hippo sprite`{:class="block3control"}

\--- /hint \---

\--- hint \---

इन ब्लॉक्स की आपको आवश्यकता होगी:

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

आपका कोड कुछ ऐसा दिखना चाहिए:

![स्टेज स्प्राइट](images/stage-sprite.png)

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

प्रत्येक नया हिप्पो एक अनियमित `x` स्थिति पर दिखना चाहिए, और प्रत्येक क्लोन की एक अनियमित गति होनी चाहिए |

\--- task \---

`speed`{:class="block3variables"} नाम का एक नया चर बनाएं जो कि सिर्फ `Hippo` स्प्राइट के लिए होगा |

[[[generic-scratch3-add-variable]]]

जब आप इसे सही ढंग से कर लेंगे, तब चर का नाम उसके पास वाले स्प्राइट का नाम होगा, जैसे कि:

![The variable sprite that reads "Hippo1: speed 0"](images/invaders-var-test.png)

\--- /task \---

\--- task \---

जब प्रत्येक `Hippo` क्लोन शुरू होता है, इसके लिए एक अनियमित गति और शुरुआती स्थान चुनें। फिर क्लोन को स्क्रीन पर दिखाएं |

```blocks3
when I start as a clone
set [speed v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

\--- /task \---

\--- task \---

अपने कोड का परीक्षण करें। क्या हर कुछ सेकंड में एक नया हिप्पो दिखाई देता है?

\--- /task \---

फिलहाल हिप्पो नहीं चल रहे हैं।

\--- task \---

प्रत्येक हिप्पो को तब तक अनियमित ढंग से घूमना चाहिए जब तक कि वह विद्युत्-तीर की चपेट में न आ जाए। ऐसा करने के लिए, इस कोड को उन ब्लॉक के नीचे संलग्न करें जो पहले से ही `Hippo` स्प्राइट के कोड स्क्रिप्ट में है:

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

फिर से अपने कोड का परीक्षण करें। आपको हर कुछ सेकंड में एक नया हिप्पो का क्लोन दिखाई देना चाहिए, और प्रत्येक क्लोन को एक अलग गति से चलना चाहिए।

\--- no-print \---

![Animation of the Hippo sprite flying around, two clones are created and move independently.](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

अब अंतरिक्ष यान की लेजर तोप का परीक्षण करें। यदि एक विद्युत-तीर एक हिप्पो को हिट करता है, तो क्या हिप्पो गायब हो जाता है?

\--- /task \---