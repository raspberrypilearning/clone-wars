## 사라지는 하마

우주선이 폭발하면 모든 하마가 다 사라져 게임 플레이가 복원될 수 있습니다.

--- task ---

우주선 스프라이트에 코드를 추가해 `우주선이 하마에 닿을 때`{:class="block3sensing"} "부딪침" 메시지를 `브로드캐스트`{:class="block3events"} 하게 합니다.

![로켓 스프라이트](images/rocket-sprite.png)

```blocks3
when flag clicked
switch costume to (기본 v)
wait until <touching (하마1 v)>?
switch costume to (부딪침 v)
+ broadcast (부딪침 v)
```

--- /task ---

--- task ---

모든 `하마` 스프라이트 복제본은 "부딪침" 메시지를 받게 될 것이고 해당 코드를 하마 스프라이트에 추가해 우주선이 부딪쳤을 때 `하마` 가 사라지게 지시내릴 수 있습니다.

![하마 스프라이트](images/hippo-sprite.png)

```blocks3
when I receive [부딪침 v]
delete this clone
```

--- /task ---

--- task ---

새 코드가 작동하는지 확인하려면 녹색 깃발을 클릭하고 우주선을 하마와 충돌시켜 보세오.

![스크린샷](images/invaders-hippo-collide.png)

--- /task ---

우주선 폭발 후 새로운 `하마` 복제본이 나타나더라도 우주선은 이미 폭발되어버린 것입니다! 우주선은 부딪친 후 자체 리셋되어야 합니다.

--- task ---

`대기`{:class="block3control"} 블록을 `우주선` 스프라이트 코드 끝에 추가해 하마가 다시 나타나기 이전 짧은 대기 시간을 만드세요. 그러고 나서 코드 전반에 `무한 반복`{:class="block3control"} 블록을 추가해 코드가 반복적으로 실행되게 하세요.

![로켓 스프라이트](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
switch costume to (기본 v)
wait until <touching (하마1 v)>?
switch costume to (부딪침 v)
broadcast (부딪침 v)
+ wait (1) seconds
end
```

--- /task ---