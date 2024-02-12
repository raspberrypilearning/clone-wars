## 宇宙カバ

今度はあなたはあなたの宇宙船を破壊しようとするたくさんの空飛ぶカバを追加します。

\--- task \---

スクラッチライブラリの 「Hippo1」画像を使って新しいスプライトを作成します。**縮小**ツールを使用して`宇宙カバ`のスプライトを`宇宙船`スプライトと同じサイズにします。

![The Scratch stage with a starry background. A rocket sits in the middle at the bottom of the stage and a hippo sprite with wings is at the top.](images/invaders-hippo.png)

\--- /task \---

\--- task \---

`カバ`のスプライトの回転スタイルを**左右のみ**にします。

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

ゲームが始まったとき、 `カバ`のスプライトを隠した状態にするコードを加えましょう。

![カバのスプライト](images/hippo-sprite.png)

```blocks3
緑の旗が押されたとき
隠す
```

\--- /task \---

\--- task \---

数秒ごとに新しい`カバ`のクローンを作成するためにステージにコードを追加します。

\--- hints \---

\--- hint \---

`緑色の旗が押されたとき`{:class="block3events"}、 `2から4の間`{:class="block3operators"} `繰り返す`{:class="block3control"} `待つ`{:class="block3control"} そして`カバのクローンを作る`{:class="block3control"}。

\--- /hint \---

\--- hint \---

必要なブロックは次のとおりです。

```blocks3
ずっと
end

(カバ v) のクローンを作る

((2) から (4) までの乱数)

⚑ が押されたとき

() 秒待つ
```

\--- /hint \---

\--- hint \---

これはあなたのコードがどのように見えるべきかです：

![ステージのスプライト](images/stage-sprite.png)

```blocks3
⚑ が押されたとき
ずっと 
  ((2) から (4) までの乱数) 秒待つ
  (Hippo1 v) のクローンを作る
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

それぞれの新しいカバクローンは、ランダムなx位置に出現し、すべてのクローンはランダムなスピードで動くようにします。

\--- task \---

`カバ`のスプライト専用の`スピード`{:class="block3variables"}という新しい変数を作成します。

[[[generic-scratch3-add-variable]]]

これを正しく行うと、変数の隣には次のようなスプライトの名前が表示されます。

![The variable sprite that reads "Hippo1: speed 0"](images/invaders-var-test.png)

\--- /task \---

\--- task \---

クローンされた`カバ`はランダムな位置で表示され、ランダムなスピードで動くようにします。

```blocks3
クローンされたとき
[スピード v] を ((2) から (4) までの乱数) にする
x座標を ((-220) から (220) までの乱数) 、y座標を (150) にする
表示する
```

\--- /task \---

\--- task \---

コードをテストしてください。新しいカバは数秒ごとに表示されますか？

\--- /task \---

現時点ではカバは移動しません。

\--- task \---

各`カバ`は、いなずま（稲妻）にぶつかるまでランダムに動き回るようにします。これを実現するには、 カバのスプライトのコードスクリプトに既にあるブロックの下にこのコードを添付します。

```blocks3
<touching (lightning v) ?> まで繰り返す 
  (speed :: variables) 歩動かす
  ↻ ((-10) から (10) までの乱数) 度回す
  もし端に着いたら、跳ね返る
end
このクローンを削除する
```

\--- /task \---

\--- task \---

もう一度コードをテストしてください。新しいカバクローンが数秒ごとに表示され、各クローンは異なる速度で移動するはずです。

\--- no-print \---

![Animation of the Hippo sprite flying around, two clones are created and move independently.](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

今宇宙船のレーザー大砲をテストします。いなずま（稲妻）がカバに当たった場合、カバは消えますか？

\--- /task \---