## 우주 - 하마

이제 우주선을 파괴하려고하는 많은 하마를 추가 할 것입니다.

\--- task \---

스크래치 라이브러리에 'Hippo1'이미지가있는 새로운 스프라이트를 만듭니다. **shrink** 도구를 사용하여 `Hippo` 스프라이트를 `Spaceship` 스프라이트와 비슷한 크기로 만듭니다.

![스크린샷](images/invaders-hippo.png)

\--- /task \---

\--- task \---

`하마` 스프라이트의 회전 스타일을 **왼쪽에서 오른쪽으로 설정하십시오**.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

게임 시작시 `하마` 스프라이트를 숨기는 코드를 추가하십시오.

![하마 스프라이트](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

\--- /task \---

\--- task \---

새로 만들 스테이지에 일부 코드를 추가 `하마` 복제를 몇 초마다.

\--- 힌트 \---

\--- hint \---

`녹색 플래그가 클릭되면`{: class = "block3events"}, `반복`{: class = "block3control"} `대기`{: class = "block3control"} `2 ~ 4 초`{: class = "block3operators"} 다음 `하마 스프라이트의 클론 만들`{: 클래스 = "block3control"}.

\--- /귀뜸말 \---

\--- hint \---

필요한 블록은 다음과 같습니다.

```blocks3
forever
end

create clone of (Hippo1 v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

\--- /귀뜸말 \---

\--- hint \---

This is what your code should look like:

![stage sprite](images/stage-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (2) to (4)) secs
    create clone of (Hippo1 v)
end
```

\--- /귀뜸말 \---

\--- / 귀뜸말 \---

\--- /task \---

Each new hippo clone should appear at a random `x` position, and every clone should have a random speed.

\--- task \---

Create a new variable called `speed`{:class="block3variables"} that is for the `Hippo` sprite only.

[[[generic-scratch3-add-variable]]]

When you've done this correctly, the variable has the name of the sprite next to it, like this:

![스크린샷](images/invaders-var-test.png)

\--- /task \---

\--- task \---

When each `Hippo` clone starts, pick a random speed and starting place for it. Then show the clone on the screen.

```blocks3
when I start as a clone
set [speed v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

\--- /task \---

\--- task \---

Test your code. Does a new hippo appear every few seconds?

\--- /task \---

At the moment the hippos don't move.

\--- task \---

Each hippo should move around randomly until it gets hit by a lightning bolt. To make that happen, attach this code below the blocks that are already in the `Hippo` sprite's code script:

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

Test your code again. You should see a new hippo clone appear every few seconds, and each clone should move at a different speed.

\--- no-print \---

![스크린샷](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Now test the spaceship's laser cannon. If a lightning bolt hits a hippo, does the hippo vanish?

\--- /task \---