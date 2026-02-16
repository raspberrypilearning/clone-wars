## 宇宙コウモリ

あなたのゲームを少し難しくするために、あなたは宇宙船でオレンジを投げるコウモリを作成します。

![宇宙船にオレンジを投げるコウモリ](images/bat-oranges.png)

--- task ---

`コウモリ`のスプライトを追加して、回転スタイルを**左右のみ**にします。

--- /task ---

--- task ---

`コウモリ`のスプライト は、ステージの最上部を`ずっと`{:class="block3control"}左右に`動いている`{:class="block3motion"}ようにします。

![コウモリのスプライト](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

コードをテストするのを忘れないでください。

--- /task ---

あなたがコウモリのコスチュームを見れば、あなたはそれが4つの異なるものを持っていることがわかります：

![スクリーンショット](images/invaders-bat-costume.png)

--- task ---

`次のコスチュームにする`{:class="block3looks"}のブロックを使用して、コウモリが動くにつれて羽を羽ばたかせるように見せます。

--- hints ---

--- hint ---

コウモリが動いた後、`次のコスチューム`{:class="block3looks"}が表示され、しばらく`待つ`{:class="block3control"}必要があります。

--- /hint ---

--- hint ---

これらのブロックをコードに追加する必要があります。

```blocks3
wait (0.3) seconds

next costume
```

--- /hint ---

--- hint ---

コードは以下のようになります：

```blocks3
when flag clicked
set size to (50) %
forever
move (10) steps
if on edge, bounce
+ next costume
+ wait (0.3) seconds
end
```

--- /hint ---

--- /hints ---

--- /task ---

コウモリがオレンジを投げるようにします！

--- task ---

スクラッチライブラリから `オレンジ (Orange)`のスプライトを追加します。

![スクリーンショット](images/invaders-orange.png)

--- /task ---

--- task ---

コードをコウモリに追加して、`緑の旗がクリックされたとき`{:class="block3events"} に、`コウモリ`スプライトが `ずっと`{:class="block3control"} `5から10`{:class="block3operators"}の`乱数`{:class="block3operators"} 秒 `待つ`{:class="block3control"}、 `オレンジ`スプライトを `クローンする`{:class="block3control"} ようにします。

![コウモリのスプライト](images/bat-sprite.png)

```blocks3
when flag clicked
forever
	wait (pick random (5) to (10)) secs
	create clone of (オレンジ v)
end
```

--- /task ---

--- task ---

`オレンジ`に`コウモリ`の場所にクローンを作って、ステージの下部へ落とすコードを追加します。

![オレンジのスプライト](images/orange-sprite.png)

```blocks3
	when flag clicked
	hide

	when I start as a clone
	go to (コウモリ v)
	show
	repeat until <touching (はし v)?
		change y by (-4)
	end
	delete this clone
```

--- /task ---

--- task ---

`オレンジ`のスプライトにさらにコードを追加して、`オレンジ`のクローンが`宇宙船`に当たったときにもクローンを消して、プレーヤーにリセットの機会を与えます。

![オレンジのスプライト](images/orange-sprite.png)

```blocks3
	when I receive [衝突 v]
	delete this clone
```

--- /task ---

--- task ---

`宇宙船`のスプライトのコードを修正して、 `カバ`のスプライトまたは`オレンジ`のスプライトに"触れた"ときに、そのスプライトが爆発するようにします。

![ロケットスプライト](images/rocket-sprite.png)

```blocks3
	wait until < <touching (カバ1 v)?> or <touching (オレンジ v)?>>
```

--- /task ---

--- task ---

ゲームをテストしてください。宇宙船がオレンジの落下に当たったら、どうなりますか？

--- /task ---