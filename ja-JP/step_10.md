## Game Over!（ゲーム終了）

Next, you're going to add a 'game over' message at the end of the game.

\--- task \---

If you haven't already, create a new variable called `lives`{:class="block3variables"}.

Your spaceship should start with three lives and lose a life whenever it touches a hippo or an orange. Your game should stop when the `lives`{:class="block3variables"} run out.

\--- /task \---

\--- task \---

**テキスト**ツールを使い`ゲームオーバー`のスプライト（Game Over!）を作りましょう。

![スクリーンショット](images/invaders-game-over.png)

\--- /task \---

\--- task \---

On the Stage, broadcast a `game over`{:class="block3events"} message just before the game ends.

![gameover sprite](images/stage-sprite.png)

![blocks_1546522848_8063066](images/blocks_1546522848_8063066.png)

\--- /task \---

\--- task \---

Add this code to your `Game Over` sprite so that it shows at the end of the game:

![gameover sprite](images/gameover-sprite.png)

![blocks_1546522851_2452476](images/blocks_1546522851_2452476.png)

Because you've used a `broadcast [game over] and wait`{:class="block3events"} block on your Stage, the Stage will wait for the `Game Over` sprite to be displayed before ending the game.

\--- /task \---

\--- task \---

Test your game. How many points can you score? If the game is too easy or too hard, can you think of ways to improve it?

\--- /task \---