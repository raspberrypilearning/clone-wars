## Hippos-gofod

Fe awn ati i ychwanegu hippos sy’n hedfan ac yn ceisio dinistrio dy long ofod.

\--- task \---

Bydd angen creu ciplun newydd o’r llun ‘Hippo1’ yn llyfrgell Scratch. Defnyddia'r teclyn **lleihau** i wneud i'r corlun `Hippo1` yn llai na'r corlun `Llong ofod`.

![sgrinlun](images/invaders-hippo.png)

\--- /task \---

\--- task \---

Gosod steil cylchdroi yr `hippo` i'r **chwith-dde** yn unig.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

Ychwanega gôd i guddio'r `hippo` pan fydd y gêm yn cychwyn.

![corlun hippo](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

\--- /task \---

\--- task \---

Ychwanega gôd i'r Llwyfan i greu clôn `hippo` newydd bob ychydig eiliadau.

\--- hints \---

\--- hint \---

Pan `fo'r faner werdd wedi ei glicio`{:class="block3events"}, `ail-adrodd`{:class="block3control"} `aros`{:class="block3control"} `rhwng 2 a 4 eiliad`{:class="block3operators"} yna `creu clôn o'r ciplun Hippo`{:class="block3control"}.

\--- /hint \---

\--- hint \---

Dyma'r blociau côd rwyt ti eu hangen:

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

Dyma sut dylai dy gôd edrych:

![corlun llwyfan](images/stage-sprite.png)

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

Dylai pob clôn hippo newydd ymddangos ar safle `x` ar hap, a dylai fod gan bob clôn gyflymder ar hap.

\--- task \---

Bydd angen creu newidyn newydd o'r enw `cyflymder`{:class="block3variables"} sydd ar gyfer y corlun `Hippo` yn unig.

[[[generic-scratch3-add-variable]]]

Pan wyt ti wedi gwneud hyn yn gywir, mae gan y newidyn enw y corlun drws nesaf iddo, fel hyn:

![sgrinlun](images/invaders-var-test.png)

\--- /task \---

\--- task \---

Pan mae clôn pob `Hippo` yn cychwyn, dewisa cyflymder ar hap a man cychwyn iddo. Yna dangosa'r clôn ar y sgrin.

```blocks3
when I start as a clone
set [speed v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

\--- /task \---

\--- task \---

Profa dy gôd. Ydy dy hippo yn ymddangos bob ychydig eiliadau?

\--- /task \---

Ar hyn o bryd nid yw'r hippo yn symud.

\--- task \---

Fe ddylai pob hippo symud o gwmpas ar hap tan ei fod yn cael ei fwrw gan fellten. I wneud hyn i ddigwydd, atoda'r côd isod i'r blociau sydd yn barod yn sgript yr `hippo`:

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

Profa dy gôd eto. Fe ddylet ti weld clôn hippo yn ymddangos bob ychydig eiliadau, ac fe ddylai pob clôn symud ar gyflymder gwahanol.

\--- no-print \---

![sgrinlun](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Nawr profa canon laser y llong ofod. Os yw mellten yn taro hippo, ydy'r hippo yn diflannu?

\--- /task \---