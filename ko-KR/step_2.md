## 우주선 만들기

지구를 방어할 수 있는 우주선을 만드십시오!

--- task ---

'복제 전쟁' 스크래치 스타터 프로젝트를 여십시오.

**온라인:** [scratch.mit.edu/projects/413427597](https://scratch.mit.edu/projects/413427597){:target="_blank"}에서 스타터 프로젝트를 엽니다.

스크래치 계정이 있는 경우 **Remix**를 클릭하여 사본을 만들 수 있습니다.

**오프라인:** 스타터 프로젝트를 [rpf.io/p/ko-KR/clone-wars-go](https://rpf.io/p/ko-KR/clone-wars-go){:target="_blank"}에서 다운로드하고 오프라인 에디터로 파일을 엽니다.

스크래치 오프라인 에디터를 다운로드 받아야 하는 경우, [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}에서 파일을 다운로드할 수 있습니다.

--- /task ---

![스타터 프로젝트](images/starter-project.png)

--- task ---

아래 코드를 우주선 스프라이트에 추가해 <kbd>왼쪽</kbd> 방향키를 누를 때 우주선이 왼쪽으로 이동하도록 하세요.

![로켓 스프라이트](images/rocket-sprite.png)

```blocks3
    when flag clicked
	forever
		if <key (left arrow v) pressed?> then
			change x by (-4)
		end
	end
```

x 축은 스테이지의 왼쪽에서 오른쪽으로갑니다. 이것은 우주선의 스프라이트의 `x` 위치 값을 빼면 우주선이 왼쪽으로 움직인다는 것을 의미합니다. 따라서 해당 코드 블록은 우주선을 왼쪽으로 이동시키는 부분입니다.

```blocks3
change x by (-4)
```

--- /task ---

--- task ---

`무한 반복`{:class="block3control"} 코드 내부에 더 많은 코드를 추가해 <kbd>오른쪽</kbd> 방향키를 누르면 우주선이 오른쪽으로 이동하게 합니다.

--- hints ---


--- hint ---

전 코드에서는 우주선의 `x` 포지션에서 `4`만큼을 왼쪽으로 이동시켰습니다. 그럼 우주선을 `4` 만큼 오른쪽으로 이동시키려면 어떻게 해야 할까요?

--- /hint ---

--- hint ---

동일한 코드 블록이 필요하지만 숫자는 달라야 합니다.

```blocks3
change x by ( )
```

--- /hint ---

--- hint ---

이 코드를 `무한 반복`{:class="block3control"} 블록 내 코드 아래 추가합니다.

![로켓 스프라이트](images/rocket-sprite.png)

```blocks3
if <key (right arrow v) pressed?> then
	change x by (4)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

녹색 깃발을 클릭해 프로젝트를 테스트하세요. 화살표 키를 누르면 우주선이 좌우로 움직여 집니까?

--- /task ---
