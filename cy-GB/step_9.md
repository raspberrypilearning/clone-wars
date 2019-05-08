## Ystlumod gofod

To make your game a bit harder, you are going to create a bat that throws oranges at the spaceship.

![ystlum yn taflu oren at y llong ofod](images/bat-oranges.png)

\--- task \---

Bydd angen creu corlun `ystlum` a gosod ei steil cylchdroi o'r **chwith-dde**.

\--- /task \---

\--- task \---

Gwna i'r corlun `Ystlum` i `symud`{:class="block3motion"} o'r chwith i'r dde ar dop y Llwyfan `am byth`{:class="block3control"}.

![corlun ystlum](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

Cofia brofi dy gôd.

\--- /task \---

Os wyt ti’n edrych ar wisgoedd yr ystlum, fe weli di fod yna bedwar gwahanol yn barod:

![sgrinlun](images/invaders-bat-costume.png)

\--- task \---

Defnyddia’r bloc `gwisg nesaf`{:class="block3looks"} i wneud i’r ystlum symud ei adenydd pan mae’n symud.

\--- hints \---

\--- hint \---

Ar ôl i'r ystlum symud, fe ddylai ddangos `gwisg newydd`{:class="block3looks"} ac yna `aros`{:class="block3control"} am amser byr.

\--- /hint \---

\--- hint \---

Mae angen ychwanegu'r blociau yma i dy gôd:

```blocks3
wait (0.3) seconds

next costume
```

\--- /hint \---

\--- hint \--- Fe ddylai dy gôd edrych fel hyn:

```blocks3
when flag clicked
set size to (50) %
forever
move (10) steps
if on edge, bounce

+ next costume
+ wait (0.3) seconds
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Nawr gwna i'r ystlum daflu orennau!

\--- task \---

Ychwanega corlun `Oren` o'r llyfrgell Scratch.

![sgrinlun](images/invaders-orange.png)

\--- /task \---

\--- task \---

Ychwanega gôd fel `pan fo'r faner wedi ei glicio`{:class="block3events"}, bydd y corlun `Ystlum` `am byth`{:class="block3control"} `yn aros`{:class="block3control"} am hyd amser `ar hap`{:class="block3operators"} rhwng `5 a 10`{:class="block3operators"} eiliad ac yna `creu clôn`{:class="block3control"} o'r corlun `Oren`.

![corlun ystlum](images/bat-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (5) to (10)) secs
    create clone of (Orange v)
end
```

\--- /task \---

\--- task \---

Ychwanega gôd i'r `Oren` i wneud i bob clôn ollwng, yn cychwyn gyda'r `Ystlum` a chwympo tuag at waelod y Llwyfan.

![corlun oren](images/orange-sprite.png)

```blocks3
    when flag clicked
    hide

    when I start as a clone
    go to (Bat v)
    show
    repeat until <touching (edge v)?
        change y by (-4)
    end
    delete this clone
```

\--- /task \---

\--- task \---

Ychwanega mwy o gôd i'r corlun `Oren` fel pan fo'r clôn `Oren` yn taro'r `Llong ofod`, mae'r clôn yn diflannu i roi cyfle i'r chwareuwr orffwys:

![corlun oren](images/orange-sprite.png)

```blocks3
    when I receive [hit v]
    delete this clone
```

\--- /task \---

\--- task \---

Addasa gôd y `Llong ofod` fel pan fo'r corlun yn cael ei "daro" mae'n cyffwrdd corlun `Hippo` neu `Oren`:

![corlun roced](images/rocket-sprite.png)

```blocks3
    wait until < <touching (Hippo1 v)?> or <touching (Orange v)?>>
```

\--- /task \---

\--- task \---

Profa dy gêm. Beth sy'n digwydd pan mae'r llong ofod yn cael ei daro gan oren?

\--- /task \---