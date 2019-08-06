## Mellt

Fe awn ati i alluogi’r llong ofod i saethu mellt!

\--- task \---

Ychwanega’r corlun `Mellt` o’r llyfrgell Scratch.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

Pan mae’r gêm yn cychwyn, fe ddylai’r `mellt` fod yn guddiedig tan fod y llong ofod yn tanio ei laser.

Ychwanega’r côd canlynol i’r corlun `Mellt`:

![corlun mellt](images/lightning-sprite.png)

```blocks3
pan fo'r flag werdd yn cael ei glicio
cuddio
```

\--- /task \---

Ar hyn o bryd, mae'r mellt yn fawr iawn o gymharu â'r llong ofod!

\--- task \---

O dan y côd sydd gan y `mellt` yn barod, ychwanega blociau i wneud y corlun yn llai a'i droi ben ei waered.

![corlun mellt](images/lightning-sprite.png)

```blocks3
gosod maint i (25) %
pwyntio i gyfeiriad (-90)
```

Nawr mae'n edrych fel ei fod yn tanio o'r ochr miniog gyntaf.

\--- /task \---

\--- task \---

Ychwanega’r côd canlynol i’r `Llong ofod` i greu mellten newydd pryd bynnag mae’r <kbd>bylchwr</kbd> yn cael ei wasgu.

\--- hints \---

\--- hint \---

`Pan fo'r faner werdd wedi ei glicio`{:class="block3events"}, cadw gwirio `am byth`{:class="block3control"}`os`{:class="block3control"} yw y `bysellfwrdd wedi ei wasgu`{:class="block3sensing"}, ac yn yr achos hynny `creu clôn o'r Mellt`{:class="block3control"}.

\--- /hint \---

\--- hint \---

Dyma'r blociau côd rwyt ti eu hangen:

```blocks3
os <> yna
end

am byth
end

creu clôn o (Lightning v)

<bysell (space v) wedi ei phwyso?>

pan fo'r flag werdd yn cael ei glicio
```

\--- /hint \---

\--- hint \---

Dyma sut dylai dy gôd edrych:

![corlun roced](images/rocket-sprite.png)

```blocks3
pan fo'r flag werdd yn cael ei glicio
am byth 
  os <bysell (space v) wedi ei phwyso?> yna 
    creu clôn o (Lightning v)
  end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Pryd bynnag mae'r gêm yn creu clôn `Mellt`, fe ddylai'r clôn ymddangos ac yna symud fyny tan ei fod yn cyrraedd topy Llwyfan. Yna fe ddylai'r clôn ddiflannu.

Ychwanega'r côd yma i'r corlun `Mellt` fel ei fod yn symud fyny tan ei fod yn cyrraedd top y Llwyfan, ac yna yn cael ei ddileu.

![corlun mellt](images/lightning-sprite.png)

```blocks3
    pan rwy'n dechrau fel clôn
mynd i (Spaceship v)
dangos
ailadrodd hyd at <cyffwrdd (edge v) ?> 
  newid y gan (10)
end
dileu y clôn hwn
```

\--- /task \---

\--- task \---

Gwasga'r allwedd <kbd>bylchwr</kbd> i brofi os yw'r mellt yn symud yn gywir.

\--- /task \---