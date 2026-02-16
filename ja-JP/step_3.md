## 稲妻

今、あなたは宇宙船に稲妻を発射する能力を与えようとしています！

--- task ---

スクラッチのライブラリーから`いなずま (Lightning)`のスプライトを追加します。

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

ゲームが始まるとき、宇宙船がレーザー砲を発射するまで `いなずま (Lightning)`の スプライトは隠されているべきです。

このコードを`いなずま (Lightning)`の スプライトに追加します。

![いなずまのスプライト](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

現時点では、いなずま（稲妻）は宇宙船に比べてとても大きいです！

--- task ---

`いなずま (Lightning)`の スプライトが既に持っているコードの下に、スプライトを小さくして逆さにするためにいくつかのブロックを追加します。

![いなずまのスプライト](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

今は宇宙船から先のとがった端を発射するように見えます。

--- /task ---

--- task ---

<kbd>スペース</kbd>キーが押された場合、 `宇宙船`はいくつかの新しいコードを追加して、いなずまの新しいクローンを作成します。

--- hints ---


--- hint ---

`緑の旗が押されたとき`{:class="block3events"}、`ずっと`{:class="block3control"}`もし`{:class="block3control"}`スペースキーが押された`{:class="block3sensing"}なら、`いなずまのスプライトのクローンを作成する`{:class="block3control"}。

--- /hint ---

--- hint ---

必要なブロックは次のとおりです。

```blocks3
if <> then
end

forever
end

create clone of (いなずま v)

<key (スペース v) pressed?>

when flag clicked
```

--- /hint ---

--- hint ---

新しいコードは次のようになります。

![ロケットスプライト](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
	if <key (スペース v) pressed?> then
		create clone of (いなずま v)
    end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

ゲームが `いなずま (Lightning)`の スプライトクローンを作成するたびに、そのクローンは出現し、それがステージの最上部に達するまで上方に移動します。その後、クローンは消えます。

このコードを`いなずま (Lightning)`のスプライトに追加すると、クローンがステージの端に触れるまで上に移動し、削除されます。

![いなずまのスプライト](images/lightning-sprite.png)

```blocks3
	when I start as a clone
	go to (宇宙船 v)
  show
	repeat until <touching (はし v) ?>
		change y by (10)
	end
	delete this clone
```

--- /task ---

--- task ---

いなずま（稲妻）が正しく動くかどうかテストするために、<kbd>スペース</kbd>キーを押してください。

--- /task ---