## 번개

이제 당신은 우주선에게 번개를 발사 할 수 있는 능력을 부여 할 것입니다!

--- task ---

`번개` 스프라이트를 스크래치 라이브러리에서 추가하십시오.

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

게임이 시작되면 우주선이 레이저 대포를 발사 할 때까지 `번개` 스프라이트를 숨겨야 합니다.

`번개` 스프라이트에 다음 코드를 추가하십시오:

![번개 스프라이트](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

현재 번개는 우주선에 비해 정말 큽니다!

--- task ---

`번개` 스프라이트가 이미 있는 코드에서, 스프라이트를 더 작게 만들고 거꾸로 뒤집을 수 있도록 블록을 추가하세요.

![번개 스프라이트](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

이제 우주선의 뾰족한 끝을 번개가 때리며 시작되는 모습입니다.

--- /task ---

--- task ---

`우주선` 스프라이트에 새로운 코드를 추가해 <kbd>space</kbd> 키를 누르면 번개가 복제되 나오도록 하세요.

--- hints ---


--- hint ---

`녹색 깃발을 클릭했을 때`{:class="block3events"}, `만약`{:class="block3control"} `스페이스 키가 클릭된 경우라면`{:class="block3sensing"} 계속 `무한반복`{:class="block3control"} 임을 체크하고 이 경우에 `새로운 번개 클론 스프라이트를 생성`{:class="block3control"} 하도록 하세요.

--- /hint ---

--- hint ---

필요한 코드 블록은 다음과 같습니다.

```blocks3
if <> then
end

forever
end

create clone of (번개 v)

<key (space v) pressed?>

when flag clicked
```

--- /hint ---

--- hint ---

다음과 같은 코드를 추가해야 합니다:

![로켓 스프라이트](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
	if <key (space v) pressed?> then
		create clone of (번개 v)
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

게임이 `번개` 스프라이트 클론을 생성 할 때마다 해당 클론이 나타나서 위쪽으로 이동해 스테이지 상단에 도달해야 합니다. 그러고나서 클론이 사라져야합니다.

`번개` 스프라이트에 다음 코드를 추가하여, 스테이지의 가장자리에 닿을 때까지 클론이 위로 이동한 후 삭제되도록 하세요. 

![번개 스프라이트](images/lightning-sprite.png)

```blocks3
    when I start as a clone
	go to (기본 v)
    show
	repeat until <touching (edge v) ?>
		change y by (10)
	end
	delete this clone
```

--- /task ---

--- task ---

<kbd>space</kbd> 키를 눌러 번개가 올바르게 움직이는지 테스트하십시오.

--- /task ---