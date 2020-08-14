## 發射雷電

現在，你要賦予你的飛船發射雷電的能力了！

--- task ---

從範例庫中選取 `Lightning` 當作角色，然後我們把它的名稱改成「閃電」。

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

遊戲一開始，應該要隱藏`閃電`，直到飛船發射。

在`閃電`角色上添加程式：

![閃電角色](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

目前，和飛船相比，這閃電也太大了吧！

--- task ---

在`閃電`現有程式下，添加一些程式，把閃電變得小一點，並讓它轉個方向。

![閃電角色](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

現在，它看起來就比較像是從飛船船頭發射出的子彈了。

--- /task ---

--- task ---

為`飛船`編寫程式，在<kbd>空白</kbd>鍵被點擊時，創建新的閃電分身。

--- hints ---


--- hint ---

`點擊綠旗`{:class="block3events"}啟動專案，在運行時`重複不斷`{:class="block3control"}的檢查，`如果`{:class="block3control"}鍵盤上的`空白鍵被按下`{:class="block3sensing"}，就`建立閃電的分身`{:class="block3control"}。

--- /hint ---

--- hint ---

這裡是你需要的程式積木：

```blocks3
if <> then
end

forever
end

create clone of (閃電 v)

<key (space v) pressed?>

when flag clicked
```

--- /hint ---

--- hint ---

你的程式看起來應該像這樣：

![飛船角色](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
	if <key (space v) pressed?> then
		create clone of (閃電 v)
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

每次建立`閃電`的分身時，分身應該要出現，然後往上方移動，直到它碰到舞台的頂部才消失。

在`閃電`角色上編寫程式，讓被建立的分身往舞台頂部垂直移動，到頂時再把分身刪除。

![閃電角色](images/lightning-sprite.png)

```blocks3
    when I start as a clone
	go to (飛船 v)
    show
	repeat until <touching (edge v) ?>
		change y by (10)
	end
	delete this clone
```

--- /task ---

--- task ---

按下<kbd>空白</kbd>鍵，測試閃電是否像預期那樣動作。

--- /task ---