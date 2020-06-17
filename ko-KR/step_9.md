## 우주-박쥐

게임을 조금 더 어렵게 만들기 위해 우주선에서 오렌지를 투하하는 박쥐를 만들어 볼 것입니다.

![우주선에서 오렌지를 투하하는 박쥐](images/bat-oranges.png)

\--- task \---

`박쥐` 스프라이트를 추가하고 회전 스타일을 **왼쪽에서 오른쪽으로** 설정하십시오.

\--- /task \---

\--- task \---

`박쥐` 스프라이트가 스테이지 맨 상단 에서 왼쪽에서 오른쪽으로 `무한반복`{:class="block3control"} `움직이게`{:class="block3motion"} 합니다.

![박쥐 스프라이트](images/bat-sprite.png)

```blocks3
깃발이 클릭 되었을 때
크기를 (50) % 로 정하기
무한 반복
    (10) 만큼 움직이기
    벽에 닿으면 튕기기
종료
```

코드를 테스트하는 것을 기억하세요.

\--- /task \---

박쥐 코스튬엔 네 종류가 있습니다:

![스크린샷](images/invaders-bat-costume.png)

\--- task \---

`다음 코스튬`{:class="block3looks"} 블록을 사용해 박쥐가 움직일 때마다 날개를 퍼덕거리게 합니다.

\--- hints \---

\--- hint \---

박쥐가 움직인 후 `다음 코스튬`{: class = "block3looks"} 이 나타나고 짧게 `대기` {: class = "block3control"} 하도록 합니다.

\--- /hint \---

\--- hint \---

다음과 같은 블록을 코드에 추가해야합니다.

```blocks3
(0.3) 초 대기

다음 코스튬
```

\--- /hint \---

\--- hint \---

다음과 같은 코드가 될 것입니다.:

```blocks3
깃발이 클릭 되었을 때
크기를 (50)% 로 정하기
무한 반복
(10) 만큼 이동하기
벽에 닿으면 튕기기

+ 다음 코스튬
+ (0.3) 초 대기
종료
```

\--- /hint \---

\--- /hints \---

\--- /task \---

이제 박쥐가 오렌지를 투하하게 하세요!

\--- task \---

스크래치 라이브러리에서 `오렌지` 스프라이트를 추가하세요.

![스크린샷](images/invaders-orange.png)

\--- /task \---

\--- task \---

박쥐 스프라이트에 다음의 코드를 추가하여 `깃발이 클릭되었을 때`{:class="block3events"}, `박쥐` 스프라이트가 `무한반복`{:class="block3control"} 한 후 `5 에서 10`{:class="block3operators"} 초 간 `랜덤`{:class="block3operators"} 하게 `대기`{:class="block3control"} 한 후 `오렌지` 스프라이트 `복제본을 생성`{:class="block3control"} 하게 합니다.

![박쥐 스프라이트](images/bat-sprite.png)

```blocks3
깃발이 클릭되었을 때
무한 반복
   ((5) 부터 (10) 사이의 난수) 초 대기
    (Orange v) 복제본 생성
종료
```

\--- /task \---

\--- task \---

`오렌지` 에 코드를 추가해 각 복제본의 투하가 `박쥐 ` 스프라이트에서 시작되어 스테이지 아래로 낙하하게 합니다.

![오렌지 스프라이트](images/orange-sprite.png)

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

`오렌지` 스프라이트에 코드를 좀 더 추가해 `오렌지` 복제본이 `우주선` 스프라이트에 부딪힐 때 복제본도 사라져서 플레이어가 리셋을 할 수 있게 합니다:

![오렌지 스프라이트](images/orange-sprite.png)

```blocks3
    when I receive [hit v]
    delete this clone
```

\--- /task \---

\--- task \---

`우주선` 스프라이트의 코드를 수정해 `하마` 스프라이트나 `오렌지` 스프라이트에 닿을 때 "맞도록" 합니다:

![로켓 스프라이트](images/rocket-sprite.png)

```blocks3
    wait until < <touching (Hippo1 v)?> or <touching (Orange v)?>>
```

\--- /task \---

\--- task \---

게임을 테스트해 보세요. 낙하하는 오렌지에 우주선이 맞으면 어떻게 되나요?

\--- /task \---