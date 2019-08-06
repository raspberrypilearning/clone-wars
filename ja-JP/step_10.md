## Game Over!（ゲーム終了）

次に、ゲーム終了時に「ゲームオーバー」メッセージを追加します。

\--- task \---

まだ行っていない場合は、 `lives`{：class = "block3variables"}という新しい変数を作成します。

あなたの宇宙船は3つの命から始まり、それがカバやオレンジに触れるたびに命を落とすはずです。 `寿命が`{ </code> ：class = "block3variables"}になると、ゲームは停止します。

\--- /task \---

\--- task \---

**テキスト**ツールを使い`ゲームオーバー`のスプライト（Game Over!）を作りましょう。

![スクリーンショット](images/invaders-game-over.png)

\--- /task \---

\--- task \---

ステージ上で、ゲームが終了する直前に</code>{ `}を超える<code>ゲームをブロードキャスト{：class = "block3events"}してください。</p>

<p><img src="images/stage-sprite.png" alt="ゲームオーバースプライト" /></p>

<pre><code class="blocks3">ブロードキャスト（vでゲーム）して待つ
`</pre> 

\--- /task \---

\--- task \---

ゲーム終了時に表示されるように、このコードを `Game Over` スプライトに追加します`</p>

<p><img src="images/gameover-sprite.png" alt="ゲームオーバースプライト" /></p>

<pre><code class="blocks3">⚑ がクリックされたとき
隠す

[ゲームオーバー v] を受け取ったとき
表示する
`</pre> 

`ブロードキャスト（ゲームオーバー）を使用し、ステージで`{：class = "block3events"}ブロック待機しているため、ステージはゲーム終了前に `Game Over` スプライトが表示されるのを待ちます。

\--- /task \---

\--- task \---

ゲームをテストしてください。何ポイント獲得できますか？ゲームが簡単すぎる、または難しすぎる場合、あなたはそれを改善する方法を考えることができますか？

\--- /task \---