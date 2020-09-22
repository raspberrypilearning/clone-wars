## विजेच्या बोल्ट

आता आपण स्पेसशिपला विजेच्या बोल्टला आग लावण्याची क्षमता देणार आहात!

\--- task \---

`Lightning` sprite Scratch लाइब्रेरी मधून जोडा.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

खेळ सुरू झाल्यावर `Lightning` sprite स्पेसशिपने आपल्या लेसर तोफांना आग लागेपर्यंत लपविला पाहिजे.

`Lightning` sprite मध्ये हा कोड जोडा:

![lightning sprite](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

\--- /task \---

या क्षणी, स्पेसशिपच्या तुलनेत विजेचा बोल्ट खरोखरच मोठा आहे!

\--- task \---

त्या कोडच्या खाली `Lightning` sprite आधीपासूनच आहे, sprite आणखी लहान करण्यासाठी आणि त्यास उलथून टाकण्यासाठी काही ब्लॉक्स जोडा.

![lightning sprite](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

आता असे दिसते की हे स्पेसशिपच्या पहिल्या स्थानावरून अगदी थोडक्यात संपेल.

\--- /task \---

\--- task \---

`Spaceship` मध्ये काही नवीन कोड जोडल्यास विजेचा बोल्टचा नवीन क्लोन तयार करण्यासाठी स्प्राइट <kbd>space</kbd> की दाबली आहे.

\--- hints \---

\--- hint \---

जेव्हा `When the green flag is clicked`{:class="block3events"}क्लिक केला जाईल`forever`{:class="block3control"} `if`{:class="block3control"} `space key is pressed`{:class="block3sensing"} ते सेकंद दरम्यान `create a clone of the Lightning`{:class="block3control"}.

\--- /hint \---

\--- hint \---

आपल्याला आवश्यक असलेले ब्लॉक्स येथे आहेत:

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

आपला कोड कसा दिसला पाहिजे:

![rocket sprite](images/rocket-sprite.png)

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

जेव्हा खेळ तयार करते तेव्हा `Lightning` sprite क्लोन, क्लोन दिसायला हवा आणि नंतर तो स्टेजच्या शिखरावर येईपर्यंत वरच्या बाजूस फिरवा. मग क्लोन अदृश्य व्हावा.

हा कोड `Lightning` sprite वर जोडा जेणेकरुन त्यातील क्लोन्स स्टेजच्या काठाला स्पर्श करेपर्यंत वरच्या दिशेने जातील आणि नंतर ते हटविले जातील.

![lightning sprite](images/lightning-sprite.png)

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

<kbd>Space</kbd> दाबा विजेचा बोल्ट योग्य प्रकारे हलतो की नाही याची चाचणी करण्यासाठी.

\--- /task \---