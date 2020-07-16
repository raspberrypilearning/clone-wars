## खेळ समाप्त

पुढे, आपण खेळच्या शेवटी 'game over' संदेश जोडणार आहात.

\--- task \---

जर तूम्ही आधी व्हेरिएबल बनवला नसेल तर, आत्ता `lives`{:class="block3variables"} नावाचा एक व्हेरिएबल बनवा.

आपले स्पेसशिप तीन जीवनांपासून सुरू झाले पाहिजे आणि जेव्हा तो हिप्पो किंवा संत्र्याला स्पर्श करेल तेव्हा आपले जीवन गमावले पाहिजे. जेव्हा `lives` {:class= "block3variables"} संपतील तेव्हा तुमचा खेळ संपला पाहिजे.

\--- /task \---

\--- task \---

**text** ह्या टूल चा वापर करून`Game over` नावाचा एक नवीन sprite बनवा.

![screenshot](images/invaders-game-over.png)

\--- /task \---

\--- task \---

स्टेजवर, खेळ संपण्यापुर्वी `Game over`{:class="block3events"} संदेश प्रदर्शित करा.

![gameover sprite](images/stage-sprite.png)

```blocks3
broadcast (game over v) and wait
```

\--- /task \---

\--- task \---

आपल्या `Game over` sprite मध्ये हा कोड जोडा जेणेकरून ते खेळच्या शेवटी दिसते:

![gameover sprite](images/gameover-sprite.png)

```blocks3
when flag clicked
hide

when I receive [game over v]
show
```

कारण आपण ` broadcast (game over) and wait `{:class="block3events"} अवरोधित (block) करा, स्टेज वर थांबेल आणि प्रतीक्षा करेल`Game Over` sprite प्रदर्शित होणार खेळ समाप्त होण्याचा आधी.

\--- /task \---

\--- task \---

आपल्या खेळाची चाचणी घ्या. आपण किती गुण मिळवू शकता? जर खेळ खूप सोपा किंवा कठोर असेल तर आपण त्या सुधारण्याच्या मार्गांचा विचार करू शकता?

\--- /task \---