## 우주선 폭발

하마가 우주선에 닿으면 우주선이 폭발해야 합니다!

--- task ---

`우주선` 스프라이트를 선택하고 코스튬 이름을 '정상' 으로 변경하십시오.

--- /task ---

--- task ---

폭발하는 우주선의 또 다른 새 코스튬을 그려서 그 이름을 '히트' 로 정합니다.

![스크린샷](images/invaders-spaceship-costumes.png)

폭발을 그리길 원치 않으면 Scratch 라이브러리에서 'Sun' 코스튬을 선택한 다음 **Color a shape** 도구를 사용하여 코스튬의 색과 얼굴을 바꿀 수 있습니다.

![스크린샷](images/invaders-sun.png)

--- /task ---

--- task ---

`우주선` 스프라이트에 코드를 추가해 게임이 시작하면 '정상' 코스튬이 나타나도록 하고 하마에 닿으면 '히트' 코스튬으로 전환하게 합니다:

![로켓 스프라이트](images/rocket-sprite.png)

```blocks3
when flag clicked
switch costume to (기본 v)
wait until <touching (하마1 v)>?
switch costume to (부딪침 v)
```

--- /task ---

--- task ---

코드를 테스트해 보세요. 우주선이 하마와 충돌하게 해보세요. 우주선이 'hit' 코스튬으로 바뀌었습니까?

--- /task ---