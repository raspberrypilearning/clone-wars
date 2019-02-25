## 게임 끝

다음으로, 게임이 끝날 때 '게임 오버'메시지를 추가 할 것입니다.

\--- task \---

아직 없으면 `lives`{: class = "block3variables"}라는 새 변수를 만듭니다.

당신의 우주선은 3 개의 생명으로 시작해야하며, 하마 또는 오렌지에 닿으면 언제든지 생명을 잃을 것입니다. ``{{class = "block3variables"}에 달하면 게임이 멈춰야합니다.

\--- /task \---

\--- task \---

**텍스트** 도구를 사용하여 `Game Over` 이라는 새로운 스프라이트를 그립니다.

![스크린샷](images/invaders-game-over.png)

\--- /task \---

\--- task \---

스테이지에, 방송 `을 통해 게임을`게임이 종료 직전에 메시지 : {클래스 = "block3events"}.

![게임 오버 스프라이트](images/stage-sprite.png)

```blocks3
broadcast (game over v) and wait
```

\--- /task \---

\--- task \---

Add this code to your `Game Over` sprite so that it shows at the end of the game:

![gameover sprite](images/gameover-sprite.png)

```blocks3
when flag clicked
hide

when I receive [game over v]
show
```

Because you've used a `broadcast (game over) and wait`{:class="block3events"} block on your Stage, the Stage will wait for the `Game Over` sprite to be displayed before ending the game.

\--- /task \---

\--- task \---

Test your game. How many points can you score? If the game is too easy or too hard, can you think of ways to improve it?

\--- /task \---