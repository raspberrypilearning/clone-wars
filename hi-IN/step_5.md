## अंतरिक्षीय दरियाई घोड़े

अब आप बहुत सारे उड़ते हुए दरियाई घोड़े जोड़ने जा रहे हैं जो आपके अंतरिक्ष-यान को नष्ट करने की कोशिश करते हैं।

\--- task \---

स्क्रैच लाइब्रेरी में 'Hippo1' इमेज के साथ एक नया स्प्राइट बनाएं। `Spaceship` स्प्राइट के आकर का `Hippo` स्प्राइट बनाने के लिए **shrink** टूल का प्रयोग करें।

![स्क्रीनशॉट](images/invaders-hippo.png)

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

` जब हरे झंडे को क्लिक किया जाता है` {:class="block3events"}, चेक करते रहें `forever`{:class="block3control"} `if` {:class="block3control"} `अंतरिक्ष कुंजी दबाया जाता है` {:class="block3sensing"}, और उस स्थिति में `दरियाई घोड़े की एक प्रतिलिपि बनाएं` {:class="block3control"} स्प्राइट।

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

प्रत्येक नया दरियाई-घोडा एक यादृच्छिक `x` स्थिति पर दिखना चाहिए, और प्रत्येक क्लोन की एक यादृच्छिक गति होनी चाहिए |

\--- task \---

`speed`{:class="block3variables"} नाम का एक नया चर बनाएं जो कि सिर्फ `Hippo` स्प्राइट के लिए होगा |

[[[generic-scratch3-add-variable]]]

जब आप इसे सही ढंग से कर लेंगे, तब चर का नाम उसके पास वाले स्प्राइट का नाम होगा, जैसे कि:

![स्क्रीनशॉट](images/invaders-var-test.png)

\--- /task \---

\--- task \---

जब प्रत्येक `Hippo` क्लोन शुरू होता है, इसके लिए एक यादृच्छिक गति और शुरुआती स्थान चुनें। फिर क्लोन को स्क्रीन पर दिखाएं |

```blocks3
when I start as a clone
set [speed v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

\--- /task \---

\--- task \---

अपने कोड का परीक्षण करें। क्या हर कुछ सेकंड में एक नया दरियाई-घोड़ा दिखाई देता है?

\--- /task \---

फिलहाल दरियाई-घोड़े नहीं चलते हैं।

\--- task \---

प्रत्येक दरियाई-घोड़े को तब तक बेतरतीब ढंग से घूमना चाहिए जब तक कि वह विद्युत्-तीर की चपेट में न आ जाए। ऐसा करने के लिए, इस कोड को उन ब्लॉक के नीचे संलग्न करें जो पहले से ही `Hippo` स्प्राइट के कोड स्क्रिप्ट में है:

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

फिर से अपने कोड का परीक्षण करें। आपको हर कुछ सेकंड में एक नया दरियाई-घोड़े का क्लोन दिखाई देना चाहिए, और प्रत्येक क्लोन को एक अलग गति से चलना चाहिए।

\--- no-print \---

![स्क्रीनशॉट](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

अब अंतरिक्ष यान की लेजर तोप का परीक्षण करें। यदि एक विद्युत-तीर एक दरियाई-घोड़े को हिट करता है, तो क्या दरियाई-घोड़ा गायब हो जाता है?

\--- /task \---