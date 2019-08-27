## Ystlumod gofod

Er mwyn gwneud eich gêm yn anoddach, byddwch yn creu ystlum a fydd yn taflu orenau at y llong ofod.

![ystlum yn taflu oren at y llong ofod](images/bat-oranges.png)

--- task ---

Bydd angen creu corlun `ystlum` a gosod ei steil cylchdroi o'r **chwith-dde**.

--- /task ---

--- task ---

Gwna i'r corlun `Ystlum` i `symud`{:class="block3motion"} o'r chwith i'r dde ar dop y Llwyfan `am byth`{:class="block3control"}.

![corlun ystlum](images/bat-sprite.png)

```blocks3
pan fo'r flag werdd yn cael ei glicio
gosod maint i (50) %
am byth 
  symud (10) cam
  os ar ymyl, bowndio
end
```

Cofia brofi dy gôd.

--- /task ---

Os wyt ti’n edrych ar wisgoedd yr ystlum, fe weli di fod yna bedwar gwahanol yn barod:

![sgrinlun](images/invaders-bat-costume.png)

--- task ---

Defnyddia’r bloc `gwisg nesaf`{:class="block3looks"} i wneud i’r ystlum symud ei adenydd pan mae’n symud.

--- hints ---


--- hint ---

Ar ôl i'r ystlum symud, fe ddylai ddangos `gwisg newydd`{:class="block3looks"} ac yna `aros`{:class="block3control"} am amser byr.

--- /hint ---

--- hint ---

Mae angen ychwanegu'r blociau yma i dy gôd:

```blocks3
aros (0.3) eiliad

gwisg nesaf
```

--- /hint ---

--- hint --- Fe ddylai dy gôd edrych fel hyn:

```blocks3
pan fo'r flag werdd yn cael ei glicio
gosod maint i (50) %
am byth 
  symud (10) cam
  os ar ymyl, bowndio

  + gwisg nesaf
  + aros (0.3) eiliad
end
```

--- /hint ---

--- /hints ---

--- /task ---

Nawr gwna i'r ystlum daflu orennau!

--- task ---

Ychwanega corlun `Oren` o'r llyfrgell Scratch.

![sgrinlun](images/invaders-orange.png)

--- /task ---

--- task ---

Ychwanega gôd fel `pan fo'r faner wedi ei glicio`{:class="block3events"}, bydd y corlun `Ystlum` `am byth`{:class="block3control"} `yn aros`{:class="block3control"} am hyd amser `ar hap`{:class="block3operators"} rhwng `5 a 10`{:class="block3operators"} eiliad ac yna `creu clôn`{:class="block3control"} o'r corlun `Oren`.

![corlun ystlum](images/bat-sprite.png)

```blocks3
pan fo'r flag werdd yn cael ei glicio
am byth 
  aros (dewis ar hap (5) i (10)) eiliad
  creu clôn o (Orange v)
end
```

--- /task ---

--- task ---

Ychwanega gôd i'r `Oren` i wneud i bob clôn ollwng, yn cychwyn gyda'r `Ystlum` a chwympo tuag at waelod y Llwyfan.

![corlun oren](images/orange-sprite.png)

```blocks3
    pan fo'r flag werdd yn cael ei glicio
cuddio

pan rwy'n dechrau fel clôn
mynd i (Bat v)
dangos
ailadrodd hyd at <cyffwrdd (edge v) ?> 
  newid y gan (-4)
end
dileu y clôn hwn
```

--- /task ---

--- task ---

Ychwanega mwy o gôd i'r corlun `Oren` fel pan fo'r clôn `Oren` yn taro'r `Llong ofod`, mae'r clôn yn diflannu i roi cyfle i'r chwareuwr orffwys:

![corlun oren](images/orange-sprite.png)

```blocks3
    pan rwy'n derbyn [ffrwydro v]
dileu y clôn hwn
```

--- /task ---

--- task ---

Addasa gôd y `Llong ofod` fel pan fo'r corlun yn cael ei "daro" mae'n cyffwrdd corlun `Hippo` neu `Oren`:

![corlun roced](images/rocket-sprite.png)

```blocks3
    aros hyd at <<cyffwrdd (Hippo1 v) ?> neu <cyffwrdd (Orange v) ?>>
```

--- /task ---

--- task ---

Profa dy gêm. Beth sy'n digwydd pan mae'r llong ofod yn cael ei daro gan oren?

--- /task ---