## 宇宙カバ

今度はあなたはあなたの宇宙船を破壊しようとするたくさんの空飛ぶカバを追加します。

--- task ---

スクラッチライブラリの 「Hippo1」画像を使って新しいスプライトを作成します。**縮小**ツールを使用して`宇宙カバ`のスプライトを`宇宙船`スプライトと同じサイズにします。

![スクリーンショット](images/invaders-hippo.png)

--- /task ---

--- task ---

`カバ`のスプライトの回転スタイルを**左右のみ**にします。

[[[generic-scratch3-sprite-rotation-style]]]

--- /task ---

--- task ---

ゲームが始まったとき、 `カバ`のスプライトを隠した状態にするコードを加えましょう。

![カバのスプライト](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

--- task ---

数秒ごとに新しい`カバ`のクローンを作成するためにステージにコードを追加します。

--- hints ---


--- hint ---

`緑色の旗が押されたとき`{:class="block3events"}、 `2から4の間`{:class="block3operators"} `繰り返す`{:class="block3control"} `待つ`{:class="block3control"} そして`カバのクローンを作る`{:class="block3control"}。

--- /hint ---

--- hint ---

必要なブロックは次のとおりです。

```blocks3
forever
end

create clone of (カバ v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

--- /hint ---

--- hint ---

これはあなたのコードがどのように見えるべきかです：

![ステージのスプライト](images/stage-sprite.png)

```blocks3
when flag clicked
forever
	wait (pick random (2) to (4)) secs
	create clone of (カバ v)
end
```

--- /hint ---

--- /hints ---

--- /task ---

それぞれの新しいカバクローンは、ランダムなx位置に出現し、すべてのクローンはランダムなスピードで動くようにします。

--- task ---

`カバ`のスプライト専用の`スピード`{:class="block3variables"}という新しい変数を作成します。

[[[generic-scratch3-add-variable]]]

これを正しく行うと、変数の隣には次のようなスプライトの名前が表示されます。

![スクリーンショット](images/invaders-var-test.png)

--- /task ---

--- task ---

クローンされた`カバ`はランダムな位置で表示され、ランダムなスピードで動くようにします。

```blocks3
when I start as a clone
set [スピード v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

--- /task ---

--- task ---

コードをテストしてください。新しいカバは数秒ごとに表示されますか？

--- /task ---

現時点ではカバは移動しません。

--- task ---

各`カバ`は、いなずま（稲妻）にぶつかるまでランダムに動き回るようにします。これを実現するには、 カバのスプライトのコードスクリプトに既にあるブロックの下にこのコードを添付します。

```blocks3
repeat until <touching (いなずま v) ?>
	move (スピード :: variables) steps
	turn right (pick random (-10) to (10)) degrees
	if on edge, bounce
end
delete this clone
```	

--- /task ---

--- task ---

もう一度コードをテストしてください。新しいカバクローンが数秒ごとに表示され、各クローンは異なる速度で移動するはずです。

--- no-print ---

![スクリーンショット](images/hippo-clones.gif)

--- /no-print ---

--- /task ---

--- task ---

今宇宙船のレーザー大砲をテストします。いなずま（稲妻）がカバに当たった場合、カバは消えますか？

--- /task ---