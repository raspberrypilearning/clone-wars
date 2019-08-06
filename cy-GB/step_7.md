## Hippos sy'n diflannu

Pan fo'r llong ofod yn ffrwydro, fe ddylai'r holl hippos ddiflannu fel bod chwareuwyr y gêm yn gallu ail-gychwyn.

\--- task \---

Ychwanega'r côd i'r corlun llong ofod i wneud iddo `ddarlledu`{:class="block3events"} y neges "taro" pan mae'r `llong ofod yn cyffwrdd hippo`{:class="block3sensing"}.

![corlun roced](images/rocket-sprite.png)

```blocks3
pan fo'r flag werdd yn cael ei glicio
newid gwisg i (normal v)
aros hyd at <cyffwrdd (Hippo1 v) ?>
newid gwisg i (ffrwydro v)

+ darlledu (ffrwydro v)
```

\--- /task \---

\--- task \---

Bydd yr holl glonau `hippo` yn derbyn y neges "taro", ac mae modd rhoi cyfarwyddyd iddynt i gyd ddiflannu pan mae'r llong ofod yn cael ei dario trwy ychwanegu'r côd yma i'r corlun `hippo`:

![corlun hippo](images/hippo-sprite.png)

```blocks3
pan rwy'n derbyn [ffrwydro v]
dileu y clôn hwn
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
pan fo'r flag werdd yn cael ei glicio
am byth 
  newid gwisg i (normal v)
  aros hyd at <cyffwrdd (Hippo1 v) ?>
  newid gwisg i (ffrwydro v)
  darlledu (ffrwydro v)

+  aros (1) eiliad
end
```

\--- /task \---