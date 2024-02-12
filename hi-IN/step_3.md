## विद्युत तीर

अब आप अंतरिक्ष यान को विद्युत तीर मारने की क्षमता देने जा रहे हैं!

\--- task \---

Scratch लाइब्रेरी से `Lightning` स्प्राइट को जोडें |

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

जब खेल शुरू होता है, तो `Lightning` स्प्राइट को तब तक छिपाया जाना चाहिए जब तक कि अंतरिक्ष यान अपनी लेजर तोपें ना दगाये।

इस कोड को अपने `Lightning` स्प्राइट में जोड़ें:

![lightning स्प्राइट](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

\--- /task \---

इस समय, अंतरिक्ष यान की तुलना में विद्युत तीर काफी बड़ा है!

\--- task \---

`Lightning` स्प्राइट का कोड जो पहले से वहाँ है, के नीचे, स्प्राइट को छोटा करने के लिए और इसे उल्टा करने के लिए कुछ ब्लॉक जोड़ें।

![lightning स्प्राइट](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

अब ऐसा लग रहा है कि यह अंतरिक्ष-यान के नुकीले हिस्से से फायर करता है।

\--- /task \---

\--- task \---

<kbd>Space</kbd> बटन दबने पर विद्युत तीर की नयी प्रतिलिपि बनाने के लिए `Spaceship` स्प्राइट में कुछ नया कोड जोड़ते हैं |

\--- hints \---

\--- hint \---

`When the green flag is clicked`{:class="block3events"}, चेक करते रहें `forever`{:class="block3control"} `if` {:class="block3control"} `space key is pressed`{:class="block3sensing"}, और उस स्थिति में `create a clone of the Lightning`{:class="block3control"} स्प्राइट।

\--- /hint \---

\--- hint \---

इन ब्लॉक्स की आपको आवश्यकता होगी:

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

यहाँ आपका नया कोड कुछ ऐसा दिखना चाहिए:

![रॉकेट स्प्राइट](images/rocket-sprite.png)

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

जब भी खेल `Lightning` स्प्राइट की प्रतिलिपि बनाता है, तब प्रतिलिपि दिखाई देनी चाहिए और इसे ऊपर की ओर तब तक बढ़ना चाहिए जब तक की वो स्टेज के शिखर तक ना पहुँच जाये | उसके बाद प्रतिलिपि गायब हो जानी चाहिए |

इस कोड को `Lightning` स्प्राइट में जोड़ें जिससे कि इसकी प्रतिलिपियाँ ऊपर की ओर तब तक बढ़ें जब तक कि वो स्टेज के किनारे तक न पहुँच जाएं, और उसके बाद गायब हो जाएं |

![lightning स्प्राइट](images/lightning-sprite.png)

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

विद्युत तीर सही से स्थानांतरित हो रहा है कि नहीं यह परीक्षण करने के लिए <kbd>space</kbd> बटन दबाएं |

\--- /task \---