## 宇宙コウモリ

あなたのゲームを少し難しくするために、あなたは宇宙船でオレンジを投げるコウモリを作成します。

![宇宙船にオレンジを投げるコウモリ](images/bat-oranges.png)

\--- 課題 \---

コウモリのスプライトを追加して、回転スタイルを左右のみにします。

\--- /課題 \---

\--- 課題 \---

コウモリのスプライト は、ステージの最上部をずっと左右に動いているようにします。

![コウモリのスプライト](images/bat-sprite.png)

```blocks3
緑の旗が押されたとき
大きさを（50）％にする
ずっと
    （10）歩動かす
    もし端に着いたら、跳ね返る
```

コードをテストするのを忘れないでください。

\--- /課題 \---

あなたがコウモリのコスチュームを見れば、あなたはそれが4つの異なるものを持っていることがわかります：

![スクリーンショット](images/invaders-bat-costume.png)

\--- 課題 \---

「次のコスチュームにする」のブロックを使用して、コウモリが動くにつれて羽を羽ばたかせるように見せます。

\--- ヒント \---

\--- ヒント \---

コウモリが動いた後、次のコスチュームが表示され、しばらく待つ必要があります。

\--- /ヒント \---

\--- ヒント \---

これらのブロックをコードに追加する必要があります。

```blocks3
0.3秒待つ
次のコスチュームにする

```

\--- /ヒント \---

\--- hint \---

You code should look like this:

```blocks3
緑の旗が押されたとき
大きさを（50）％にする
ずっと
（10）歩動かす
もし端に着いたら、跳ね返る
次のコスチュームにする
+次の衣装
（0.3）秒待つ
```

\--- /hint \---

\--- /hints \---

\--- /task \---

Now make the bat throw oranges!

\--- task \---

Add an `Orange` sprite from the Scratch library.

![screenshot](images/invaders-orange.png)

\--- /task \---

\--- task \---

Add code to your bat so that `when the flag is clicked`{:class="block3events"}, the `Bat` sprite `forever`{:class="block3control"} `waits`{:class="block3control"} for a `random`{:class="block3operators"} length of time between `5 to 10`{:class="block3operators"} seconds and then `creates a clone`{:class="block3control"} of the `Orange` sprite.

![bat sprite](images/bat-sprite.png)

```blocks3
緑の旗が押されたとき
ずっと
5から10までの乱数秒待つ
オレンジのクローンを作る
```

\--- /task \---

\--- task \---

Add code to the `Orange` to make each of its clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

![orange sprite](images/orange-sprite.png)

```blocks3
    緑の旗が押されたとき
隠す

クローンされたとき
    （コウモリ）へ行く
    表示する
    端に触れたまで繰り返す
    y座標を（-4）ずつ変える
　このクローンを削除する
```

\--- /task \---

\--- task \---

Add some more code to the `Orange` sprite so that when an `Orange` clone hits the `Spaceship` sprite, the clone also disappears to give the player a chance to reset:

![orange sprite](images/orange-sprite.png)

```blocks3
    「衝突した」のメッセージを受け取ったとき
このクローンを削除する
```

\--- /task \---

\--- task \---

Modify the code of your `Spaceship` sprite so that the sprite is "hit" when it touches a `Hippo` sprite or an `Orange` sprite:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    カバに触れた または オレンジに触れた まで待つ
```

\--- /task \---

\--- task \---

Test your game. What happens if the spaceship gets hit by a falling orange?

\--- /task \---