## अदृश्य होणारे हिप्पो

जेव्हा स्पेसशिपचा स्फोट होतो, तेव्हा सर्व हिप्पोज अदृश्य व्हावेत जेणेकरुन खेळाचे खेळाडू पुनर्संचयित होऊ शकतील.

--- task ---

आकाशयान च्या sprite मध्ये `broadcast`{:class="block3events"} कोड जोडा ज्याने निरोप "hit" येणार जे `spaceship touches a hippo`{:class="block3sensing"}.

![rocket sprite](images/rocket-sprite.png)

```blocks3
when flag clicked
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (hit v)

+ broadcast (hit v)
```

--- /task ---

--- task ---

सर्व `Hippo` sprite क्लोनला "hit" निरोप प्राप्त होईल आणि आपण सूचना देऊ शकतो त्यांना अदृश्य होण्याचा जेव्हा आकाशयान त्यांना आपटेल त्यासाठी हा `Hippo` sprite: कोड जोडावा लागेल:

![hippo sprite](images/hippo-sprite.png)

```blocks3
when I receive [hit v]
delete this clone
```

--- /task ---

--- task ---

नवीन कोड कार्यरत आहे की नाही हे चाचणी करण्या साठी हिरव्या ध्वजांवर क्लिक करा आणि आकाश्यानला हिप्पोने टक्कर द्या.

![screenshot](images/invaders-hippo-collide.png)

--- /task ---

जेव्हा स्पेसशिपचा चा स्फोट झाल्यावर, नवीन `Hippo` clones दिसणार, पण आकाशयान अद्याप स्फोट आहे! आपटल्या नंतर स्लापेसशिप स्वतःला पुन्हा रचना करणा आवश्यक आहे.

--- task ---

हिप्पोस पुन्हा दिसायला सुरू होण्यापुर्वी एक अल्प विराम घेण्यासाठी `wait`{:class="block3control"} हा कोड `Spaceship` च्या शेवटी जोडा. नंतर आपला कोड वारंवार चालवण्यासाठी `forever`{:class="block3control"} तुमच्या कोड मध्ये जोडा.

![rocket sprite](images/rocket-sprite.png)

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