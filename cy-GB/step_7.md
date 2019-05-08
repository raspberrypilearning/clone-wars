## Hippos sy'n diflannu

Pan fo'r llong ofod yn ffrwydro, fe ddylai'r holl hippos ddiflannu fel bod chwareuwyr y gêm yn gallu ail-gychwyn.

\--- task \---

Ychwanega'r côd i'r corlun llong ofod i wneud iddo `ddarlledu`{:class="block3events"} y neges "taro" pan mae'r `llong ofod yn cyffwrdd hippo`{:class="block3sensing"}.

![corlun roced](images/rocket-sprite.png)

```blocks3
when flag clicked
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (hit v)

+ broadcast (hit v)
```

\--- /task \---

\--- task \---

Bydd yr holl glonau `hippo` yn derbyn y neges "taro", ac mae modd rhoi cyfarwyddyd iddynt i gyd ddiflannu pan mae'r llong ofod yn cael ei dario trwy ychwanegu'r côd yma i'r corlun `hippo`:

![corlun hippo](images/hippo-sprite.png)

```blocks3
when I receive [hit v]
delete this clone
```

\--- /task \---

\--- task \---

I wirio os yw'r côd yma yn gweithio, clicia'r faner werdd i wneud i'r llong ofod wrthdaro gyda hippo.

![sgrinlun](images/invaders-hippo-collide.png)

\--- /task \---

Ar ôl i'r llong ofod ffrwydro, bydd clonau newydd `hippo` yn ymddangos, ond mae'r llong ofod dal wedi ffrwydro! Mae angen i'r llong ofod ailosod ei hun ar ôl cael ei daro.

\--- task \---

Ychwanega bloc `aros`{:class="block3control"} ar ddiwedd côd y `llong ofod` i greu saib fach cyn i'r hippos gychwyn ymddangos eto. Yna ychwanega bloc `am byth`{:class="block3control"} o amgylch dy gôd i wneud i'r côd redeg dro ar ôl tro.

![corlun roced](images/rocket-sprite.png)

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

\--- /task \---