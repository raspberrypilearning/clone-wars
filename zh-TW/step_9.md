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

\---提示\--- 您的代碼應如下所示：

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

\--- /提示\---

\--- /提示\---

\--- /任務\---

現在讓蝙蝠扔掉橘子！

\---任務\---

從Scratch庫中添加 `Orange` 精靈。

![截圖](images/invaders-orange.png)

\--- /任務\---

\---任務\---

將代碼添加到你的蝙蝠，使得 `當標誌被點擊`{：類=“block3events”}，該 `蝙蝠` 子畫面 `永遠`{：類=“block3control”} `等待`{：類=“block3control”}對於 `隨機的`{：class =“block3operators”}時間長度在 `5到10`{：class =“block3operators”}秒然後 `創建一個克隆`{：class =“block3control”}的 `Orange` 精靈。

![蝙蝠精靈](images/bat-sprite.png)

```blocks3
當標誌點擊
永遠
    等待（隨機選擇（5）到（10））秒
    創建克隆（橙色v）
結束
```

\--- /任務\---

\---任務\---

將代碼添加到 `Orange` 以使其每個克隆下降，從 `Bat` 精靈開始並向舞台底部下降。

![橙色精靈](images/orange-sprite.png)

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

\--- /任務\---

\---任務\---

為 `Orange` 精靈添加更多代碼，這樣當 `Orange` 克隆擊中 `Spaceship` 精靈時，克隆也會消失，讓玩家有機會重置：

![橙色精靈](images/orange-sprite.png)

```blocks3
    當我收到[點擊v]
    刪除此克隆
```

\--- /任務\---

\---任務\---

修改 `Spaceship` 精靈的代碼，以便精靈在接觸到 `Hippo` 精靈或 `橙色` 精靈時被“擊中”：

![火箭精靈](images/rocket-sprite.png)

```blocks3
    等到 < <touching (Hippo1 v)?> 或 <touching (Orange v)?>>
```

\--- /任務\---

\---任務\---

測試你的遊戲。如果宇宙飛船被落下的橙色擊中會發生什麼？

\--- /任務\---