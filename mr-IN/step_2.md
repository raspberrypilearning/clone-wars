## स्पेसशिप बनवा

पहिले पृथ्वीचे रक्षण करू शकणारे अंतरिक्षयान (spaceship) तयार करा!

--- task ---

'clone वॉर' Scratch स्टार्टर प्रकल्प उघडा.

**ऑनलाइन:** स्टार्टर प्रोजेक्ट [rpf.io/clone-wars-on](https://rpf.io/clone-wars-on){:target="_blank"} वर उघडा.

आपल्याकडे scratch खाते असल्यास आपण **Remix** वर क्लिक करुन एक प्रत बनवू शकता.

**ऑफलाइनः** स्टार्टर प्रोजेक्ट [rpf.io/p/mr-IN/clone-wars-go](https://rpf.io/p/mr-IN/clone-wars-go) वरून डाउनलोड करा आणि नंतर ऑफलाइन एडिटर वापरून तो उघडा.

आपल्याला Scratch ऑफलाइन संपादक डाउनलोड आणि स्थापित करण्याची आवश्यकता असल्यास, आपण [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"} वर शोधू शकता.

--- /task ---

![starter project](images/starter-project.png)

--- task ---

<kbd>left</kbd> कडे सोडल्यास स्पेसशिप डावीकडे हलविण्यासाठी हा कोड स्पेसशिप sprite मध्ये जोडा एरो दाबले आहे:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    when flag clicked
    forever
        if <key (left arrow v) pressed?> then
            change x by (-4)
        end
    end
```

X-axis स्टेजच्या डाव्या बाजूपासून उजवीकडे जाते. याचा अर्थ असा की जेव्हा आपण स्पेसशिप sprite `x` च्या मूल्यातून वजा कराल तेव्हा स्पेसशिप डावीकडे सरकले. तर हा कोड ब्लॉक हा एक भाग आहे ज्यामुळे आपला स्पेसशिप डावीकडे हलविला जातो:

```blocks3
change x by (-4)
```

--- /task ---

--- task ---

जेव्हा <kbd>right</kbd> की दाबली जाइल तेव्हा ब्लॉक ला उजवीकडे हलवण्यासाठी `forever`{:class="block3control"} मध्ये आणखी कोड जोडा.

--- hints ---


--- hint ---

जर स्पेसशिपच्या `x` स्थानावरुन त्याला डावीकडे स्थानांतरित करण्यासाठी `4` वजा केले तर मग स्पेसशिपला उजविकडे `4` ने स्थानांतरित करण्यासाठी काय कराल तुम्ही?

--- /hint ---

--- hint ---

आपल्याला समान कोड ब्लॉक आवश्यक आहे, परंतु भिन्न क्रमांकासह:

```blocks3
change x by ( )
```

--- /hint ---

--- hint ---

येथे इतर कोड खाली आपल्याला कायमची जोडण्यासाठी आवश्यक असलेला कोड आहे `forever`{:class="block3control"} ब्लॉक:

![rocket sprite](images/rocket-sprite.png)

```blocks3
if <key (right arrow v) pressed?> then
    change x by (4)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

हिरव्या फ्लैगवर क्लिक करून आपल्या प्रोजेक्टची चाचणी घ्या. आपली स्पेसशिप डावीकडे व उजवीकडे हलविण्यासाठी आपण बाण की दाबू शकता?

--- /task ---
