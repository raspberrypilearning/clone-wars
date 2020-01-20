## 우주 박쥐

게임을 조금 더 어렵게 만들려면 우주선에서 오렌지를 던지는 박쥐를 만들어야합니다.

![우주선에서 오렌지를 던지는 박쥐](images/bat-oranges.png)

\--- task \---

`박쥐` 스프라이트를 추가하고 회전 스타일을 왼쪽에서 오른쪽으로 **설정하십시오**.

\--- /task \---

\--- task \---

`박쥐` 스프라이트 `Stage <code>의 맨 위에서 왼쪽에서 오른쪽으로`{: class = "block3motion"} 영원히</code>{: class = "block3control"} 이동시킵니다.

![박쥐 스프 라이트](images/bat-sprite.png)

```blocks3
녹색 깃발을 클릭했을 때
크기를 (50) % 로 정하기
무한 반복
    (10) 만큼 움직이기
    벽에 닿으면 튕기기
끝
```

코드를 테스트하는 것을 기억하세요.

\--- /task \---

박쥐의 의상을 보면 네 가지 의상이 있음을 알 수 있습니다:

![스크린샷](images/invaders-bat-costume.png)

\--- task \---

`다음 모양으로 바꾸기`{:class="block3looks"} 블록을 사용하여 박쥐의 날개를 흔들도록 합니다.

\--- hints \---

\--- hint \---

박쥐가 움직 인 후에는 `다음 모양으로 바꾸기`{: class = "block3looks"}를 한 이후 짧은 시간 동안 `기다리기` {: class = "block3control"} 해야 합니다.

\--- /hint \---

\--- hint \---

코드에 다음 블록을 추가해야합니다.

```blocks3
(0.3) 초 기다리기
다음 모양으로 바꾸기
```

\--- /hint \---

\--- hint \---

You code should look like this:

```blocks3
초록색 깃발을 클릭했을 때
크기를 (50)% 로 정하기
무한 반복
(10) 만큼 이동하기
벽에 닿으면 튕기기

+ 다음 모양으로 바꾸기
+ (0.3)초 기다리기
끝
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Now make the bat throw oranges!

\--- task \---

Add an `Orange` sprite from the Scratch library.

![screenshot](images/invaders-orange.png)

\--- /task \---

\--- task \---

Add code to your bat so that `when the flag is clicked`{:class="block3events"}, the `Bat` sprite `forever`{:class="block3control"} `waits`{:class="block3control"} for a `random`{:class="block3operators"} length of time between `5 to 10`{:class="block3operators"} seconds and then `creates a clone`{:class="block3control"} of the `Orange` sprite.

![bat sprite](images/bat-sprite.png)

```blocks3
초록색 깃발이 클릭되었을 때
무한 반복
   ((5) 부터 (10) 사이의 난수) 초 기다리기
    (Orange v) 복제하기
끝
```

\--- /task \---

\--- task \---

Add code to the `Orange` to make each of its clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

![orange sprite](images/orange-sprite.png)

```blocks3
    초록색 깃발이 클릭되었을 때
    숨기기
    (Bat v) 로 이동
    보이기
    < touching (edge v)? 까지 반복
        y를 (-4) 만큼 바꾸기
    끝
    이 복제본 삭제하기
```

\--- /task \---

\--- task \---

Add some more code to the `Orange` sprite so that when an `Orange` clone hits the `Spaceship` sprite, the clone also disappears to give the player a chance to reset:

![orange sprite](images/orange-sprite.png)

```blocks3
    [hit v] 신호를 받았을 때
    이 복제본 삭제하기
```

\--- /task \---

\--- task \---

Modify the code of your `Spaceship` sprite so that the sprite is "hit" when it touches a `Hippo` sprite or an `Orange` sprite:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    < <touching (Hippo1 v)?> 또는 <touching (Orange v)?> > 까지 기다리기
```

\--- /task \---

\--- task \---

Test your game. What happens if the spaceship gets hit by a falling orange?

\--- /task \---