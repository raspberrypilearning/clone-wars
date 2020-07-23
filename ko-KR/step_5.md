## 우주-하마

이제 우주선을 파괴하려는 하마를 많이 추가 할 것입니다.

--- task ---

스크래치 라이브러리에 'Hippo1' 이미지가 있는 새로운 스프라이트를 만듭니다. **shrink** 도구를 사용하여 `하마` 스프라이트를 `우주선` 스프라이트와 유사한 크기로 만듭니다.

![스크린샷](images/invaders-hippo.png)

--- /task ---

--- task ---

`하마` 스프라이트의 회전 스타일을 **왼쪽에서 오른쪽으로** 설정하십시오.

[[[generic-scratch3-sprite-rotation-style]]]

--- /task ---

--- task ---

게임 시작 시 `하마` 스프라이트를 숨기는 코드를 추가하십시오.

![하마 스프라이트](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

--- task ---

몇 초마다 한 번씩 `하마` 가 생성되도록 스테이지에 코드를 몇 개 추가합니다.

--- hints ---


--- hint ---

`녹색 플래그가 클릭 되면`{:class="block3events"}, `2 ~ 4 초`{:class="block3operators"} `반복`{:class="block3control"} `대기`{:class="block3control"} 한 후 `하마 스프라이트를 복제 생성`{:class="block3control"}.

--- /hint ---

--- hint ---

필요한 블록은 다음과 같습니다.

```blocks3
forever
end

create clone of (하마1 v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

--- /hint ---

--- hint ---

코드는 다음과 같이 설계되어야 합니다:

![무대 스프라이트](images/stage-sprite.png)

```blocks3
when flag clicked
forever
	wait (pick random (2) to (4)) secs
	create clone of (하마1 v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

생성된 복제 하마는 각각 랜덤한 `x` 포지션에 등장하고 랜덤한 속도를 가져야 합니다.

--- task ---

`하마` 스프라이트 고유의 `속도`{:class="block3variables"} 변수를 새롭게 제작하세요.

[[[generic-scratch3-add-variable]]]

이 작업을 올바르게 수행하면 해당 변수 옆에 다음과 같이 스프라이트 이름이 오게 됩니다:

![스크린샷](images/invaders-var-test.png)

--- /task ---

--- task ---

각 `하마` 복제가 시작되면 랜덤한 속도와 시작 지점을 선택하십시오. 그런 다음 해당 복제를 화면에 표시합니다.

```blocks3
when I start as a clone
set [속도 v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

--- /task ---

--- task ---

코드를 테스트하십시오. 몇 초마다 새로운 하마가 나타납니까?

--- /task ---

현재 하마는 움직이지 않습니다.

--- task ---

각 하마는 번개에 맞을 때까지 무작위로 움직여야 합니다. 이를 위해 `하마` 스프라이트에 있는 코드 아래에 이 코드를 붙여야 합니다:

```blocks3
repeat until <touching (번개 v) ?>
	move (속도 :: variables) steps
	turn right (pick random (-10) to (10)) degrees
	if on edge, bounce
end
delete this clone
```

--- /task ---

--- task ---

코드를 다시 테스트하십시오. 몇 초마다 새롭게 복제된 하마가 나타나야 하며 이들은 각자 다른 속도로 움직여야 합니다.

--- no-print ---

![스크린샷](images/hippo-clones.gif)

--- /no-print ---

--- /task ---

--- task ---

이제 우주선의 레이저 대포를 시험해보십시오. 번개가 하마에 부딪칠 때 하마가 사라지나요?

--- /task ---