## Creu Llong Ofod

Fe awn ati i greu llong ofod fydd yn amddiffyn y Ddaear!

--- task ---

Agora'r prosiect cychwynnol 'Brwydr Clonau'.

**Arlein:** agora brosiect Scratch newydd yma [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target="_blank"}.

Os oes ganddot ti gyfrif Scratch galli di wneud copi drwy glicio ar **Remix**.

**All-lein:** lawrlwytha'r prosiect cychwynnol o [rpf.io/p/cy-GB/clone-wars-go](http://rpf.io/p/cy-GB/clone-wars-go) ac yna ei agor gan ddefnyddio'r golygydd all-lein.

Os oes angen i ti lawrlwytho a gosod golygydd Scratch all-lein, mae modd dod o hyd iddo yma [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

--- /task ---

![prosiect cychwynnol](images/starter-project.png)

--- task ---

Ychwanega côd i symud dy long ofod i’r chwith pan rwyt ti’n gwasgu’r saeth <kbd>chwith</kbd> ar y bysellfwrdd:

![corlun roced](images/rocket-sprite.png)

```blocks3
    pan fo'r flag werdd yn cael ei glicio
    am byth 
        os <bysell (saeth chwith v) wedi ei phwyso?> yna
            newid x gan (-4)
        end
    end
```

Mae'r echelin-x yn mynd o ochr chwith y Llwyfan i'r ochr dde. Mae hyn yn golygu bod y llong ofod yn symud i'r chwith pan fyddwn yn tynnu o werth y llong ofod yn y safle `x`. Felly mae'r bloc côd yma yn rhan o'r hyn sy'n gwneud i'r llong ofod symud i'r chwith:

```blocks3
newid x gan (-4)
```

--- /task ---

--- task ---

Ychwanega mwy o gôd o fewn y bloc `am byth`{:class="block3control"} i symud dy long ofod i’r dde pan wyt ti’n gwasgu’r saeth <kbd>dde</kbd>.

--- hints ---


--- hint ---

Fe wnaeth tynnu `4` o safle `x` y llong ofod wneud iddo symud i'r chwith, felly sut mae gwneud i'r llong ofod symud i'r dde wrth `4` yn lle?

--- /hint ---

--- hint ---

Rwyt ti angen yr un bloc côd, ond gyda rhif gwahanol:

```blocks3
newid x gan ( )
```

--- /hint ---

--- hint ---

Dyma'r côd rwyt ti ei angen ychwanegu o dan y côd o fewn y bloc `am byth`{:class="block3control"}:

![corlun roced](images/rocket-sprite.png)

```blocks3
os <bysell (saeth de v) wedi ei phwyso?> yna 
  newid x gan (4)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Profa dy brosiect drwy glicio ar y faner werdd. Alli di wasgu'r bysellau saeth i wneud dy llong ofod symud i'r chwith ac i'r dde?

--- /task ---