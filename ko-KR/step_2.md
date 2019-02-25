## 우주선을 만드십시오.

지구를 방어 할 수있는 우주선을 만드십시오!

\--- task \---

'복제 전쟁'스크래치 초보 프로젝트를 엽니 다.

**Online :** [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){: target = "_ blank"}에서 시작 프로젝트를 엽니 다.

**오프라인 :** 다운로드에서 스타터 프로젝트 [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go)다음 및 오프라인 편집기를 사용하여 엽니 다.

Scratch 오프라인 편집기를 다운로드하여 설치해야하는 경우 [rpf.io/scratchoff](https://rpf.io/scratchoff){: target = "_ blank"}에서 찾을 수 있습니다.

\--- /task \---

![시동기 프로젝트](images/starter-project.png)

\--- task \---

경우 우주선 이동이 왼쪽으로 만들기 위해 우주선 스프라이트에이 코드를 추가 <kbd>왼쪽</kbd> 화살표를 누르면 :

![로켓 스프라이트](images/rocket-sprite.png)

```blocks3
    when flag clicked
    forever
        if <key (left arrow v) pressed?> then
            change x by (-4)
        end
    end
```

The x-axis goes from the left side of the Stage to the right side. This means that the spaceship moves to the left when you subtract from the value of the spaceship sprite's `x` position. So this code block is the part that makes your spaceship move left:

```blocks3
change x by (-4)
```

\--- /task \---

\--- task \---

Add some more code inside the `forever`{:class="block3control"} block to make your spaceship move to the right if the <kbd>right</kbd> arrow key is pressed.

\--- hints \---

\--- hint \---

Subtracting `4` from the spaceship's `x` position made it move left, so how could you make the spaceship move right by `4` instead?

\--- /hint \---

\--- hint \---

You need the same code block, but with a different number:

```blocks3
change x by ( )
```

\--- /hint \---

\--- hint \---

Here is the code you need to add below the other code inside the `forever`{:class="block3control"} block:

![rocket sprite](images/rocket-sprite.png)

```blocks3
if <key (right arrow v) pressed?> then
    change x by (4)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

Test your project by clicking the green flag. Can you press the arrow keys to make your spaceship move left and right?

\--- /task \---