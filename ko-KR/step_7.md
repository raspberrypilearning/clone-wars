## 사라지는 하마

우주선이 폭발하면 모든 하마가 사라져 게임 플레이어가 회복 될 수 있습니다.

\--- task \---

우주선 스프라이트에 코드를 추가하여 `으로 만듭니다.`{: class = "block3events"} `우주선이 하마를 만났을 때 "hit"메시지가`{: class = "block3sensing"}됩니다.

![로켓 스프라이트](images/rocket-sprite.png)

```blocks3
녹색 깃발이 클릭된 경우
모양을 (normal v) 로 바꾸기
<touching (Hippo1 v)> 까지 기다리기
모양을 (hit v) 로 바꾸기

 + (hit v) 신호 보내기
```

\--- /task \---

\--- task \---

모든 `하마` 스프라이트 클론은 "hit" 메시지를 받을 수 있으며, 하마 스프라이트에 이 코드를 추가하여 우주선이 공격을 받을 때 `하마` 가 사라지도록 할 수 있습니다.

![하마 스프라이트](images/hippo-sprite.png)

```blocks3
[hit v] 신호를 받았을 때
이 복제본 삭제하기
```

\--- /task \---

\--- task \---

새 코드가 작동하는지 확인하려면 녹색 깃발을 클릭하고 우주선을 하마와 충돌 시키십시오.

![스크린샷](images/invaders-hippo-collide.png)

\--- /task \---

우주선이 폭발 한 후에 새로운 `하마` 클론이 나타나지만 우주선은 여전히 폭발하고 있습니다! 우주선은 공격당한 후에 스스로 리셋되어야 합니다.

\--- task \---

`기다리기`{:class="block3control"} 블록을 `우주선` 스프라이트 코드에 추가하여 하마가 다시 나타나기 전에 짧은 대기시간을 만드세요. 이후 `무한 반복`{:class="block3control"} 블록을 코드에 추가하여 무한 반복되도록 하세요.

![로켓 스프라이트](images/rocket-sprite.png)

```blocks3
초록색 깃발이 클릭되었을 때
무한 반복
모양을 (normal v) 로 바꾸기
<touching (Hippo1 v)> 만큼 기다리기
모양을 (hit v) 로 바꾸기
(hit v) 신호 보내기

+ (1) 초 기다리기
끝
```

\--- /task \---