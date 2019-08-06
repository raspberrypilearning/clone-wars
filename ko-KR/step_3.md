## 번개

이제 당신은 우주선에게 번개를 발사 할 수있는 능력을 부여 할 것입니다!

\--- task \---

`번개` 스프라이트를 스크래치 라이브러리에서 추가하십시오.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

게임이 시작되면 우주선이 레이저 대포를 발사 할 때까지 `번개` 스프라이트를 숨겨야합니다.

`번개` 스프라이트에 다음 코드를 추가하십시오.

![번개 스프라이트](images/lightning-sprite.png)

```blocks3
녹색 깃발을 클릭 했을 때
숨기기
```

\--- /task \---

현재 번개는 우주선에 비해 정말 큽니다!

\--- task \---

`번개` 스프라이트가 이미 있는 코드에서, 스프라이트를 더 작게 만들고 거꾸로 뒤집을 수 있도록 블록을 추가하세요.

![번개 스프라이트](images/lightning-sprite.png)

```blocks3
크기를 (25) % 로 정하기
(-90) 도 방향 보기
```

이제 번개는 우주선의 뾰족한 부분에서 시작하게 됩니다.

\--- /task \---

\--- task \---

`우주선` 스프라이트에 새로운 코드를 추가하여 <kbd>space</kbd> 키를 누르면 번개가 나오도록 하세요.

\--- hints \---

\--- hint \---

`녹색 깃발을 클릭했을 때`{:class="block3events"}, 계속 `무한반복`{:class="block3control"} 임을 체크한다 `만약`{:class="block3control"} `스페이스 키가 클릭된 경우`{:class="block3sensing"} `새로운 번개 클론 스프라이트를 생성`{:class="block3control"} 하도록 하세요.

\--- /hint \---

\--- hint \---

필요한 코드 블록은 다음과 같습니다.

```blocks3
만약 <> 이라면
끝

무한 반복
끝

(Lightning v) 복제하기

<key (space v) pressed?>

녹색 깃발을 클릭하였을 때
```

\--- /hint \---

\--- hint \---

다음과 같은 코드를 추가해야 합니다:

![로켓 스프라이트](images/rocket-sprite.png)

```blocks3
녹색 깃발을 클릭하였을 때
무한 반복
    만약 <key (space v) pressed?> 이라면
        (Lightning v) 복제하기
    끝
끝
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

게임이 `번개`를 생성 할 때마다 스프라이트 복제본 클론이 나타나야하고 스테이지의 상단에 도달 할 때까지 위쪽으로 이동해야합니다. 그런 다음 클론이 사라져야합니다.

`번개` 스프라이트에 다음 코드를 추가하여, 스테이지의 가장자리에 닿을 때까지 클론이 위로 이동한 후 삭제되도록 하세요. 

![번개 스프라이트](images/lightning-sprite.png)

```blocks3
    복제되었을 때
    (Spaceship v)로 이동
    보이기
    <touching (edge v) ?> 까지 반복하기
        y를 (10) 만큼 바꾸기
    끝
    이 복제본 삭제하기
```

\--- /task \---

\--- task \---

<kbd>space</kbd> 키를 눌러 번개가 올바르게 움직이는지 여부를 테스트하십시오.

\--- /task \---