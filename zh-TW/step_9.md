## 空間蝙蝠

為了讓你的遊戲更加困難，你將創造一種在飛船上投擲橙子的蝙蝠。

![一隻蝙蝠在飛船上扔橙子](images/bat-oranges.png)

\---任務\---

添加 `Bat` 精靈並將其旋轉樣式設置為 **左右**。

\--- /任務\---

\---任務\---

讓 `Bat` 精靈 `從舞台 <code>的頂部從左到右移動`{：class =“block3motion”}</code>{：class =“block3control”}。

![蝙蝠精靈](images/bat-sprite.png)

```blocks3
當標記點擊時
設置大小為（50）％
永遠
    移動（10）步驟
    如果在邊緣，反彈
結束
```

記得測試你的代碼。

\--- /任務\---

如果你看看蝙蝠的服裝，你可以看到它有四種不同的服裝：

![截圖](images/invaders-bat-costume.png)

\---任務\---

使用 `下一個服裝`{：class =“block3looks”}塊來使蝙蝠在移動時拍打它的翅膀。

\---提示\---

\---提示\---

蝙蝠移動後，它應該顯示 `下一個服裝`{：class =“block3looks”}然後 `等待`{：class =“block3control”}一小段時間。

\--- /提示\---

\---提示\---

您需要將這些塊添加到代碼中：

```blocks3
等待（0.3）秒

下一個服裝
```

\--- /提示\---

\--- hint \---

You code should look like this:

```blocks3
當標誌點擊
設置大小為（50）％
永遠
移動（10）步驟
如果在邊緣，反彈

+下一個服裝
+等待（0.3）秒
結束
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
當標誌點擊
永遠
    等待（隨機選擇（5）到（10））秒
    創建克隆（橙色v）
結束
```

\--- /task \---

\--- task \---

Add code to the `Orange` to make each of its clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

![orange sprite](images/orange-sprite.png)

```blocks3
    當標記點擊時
    隱藏

    當我作為克隆
    開始時去（Bat v）
    顯示
    重複直到 <觸摸（邊緣v）？
        更改y by（-4）
    end
    刪除此克隆
```

\--- /task \---

\--- task \---

Add some more code to the `Orange` sprite so that when an `Orange` clone hits the `Spaceship` sprite, the clone also disappears to give the player a chance to reset:

![orange sprite](images/orange-sprite.png)

```blocks3
    當我收到[點擊v]
    刪除此克隆
```

\--- /task \---

\--- task \---

Modify the code of your `Spaceship` sprite so that the sprite is "hit" when it touches a `Hippo` sprite or an `Orange` sprite:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    等到 < <touching (Hippo1 v)?> 或 <touching (Orange v)?>>
```

\--- /task \---

\--- task \---

Test your game. What happens if the spaceship gets hit by a falling orange?

\--- /task \---