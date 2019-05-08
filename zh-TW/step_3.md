## 閃電

現在你要給太空船發射閃電的能力了！

\---任務\---

從Scratch庫中添加 `Lightning` sprite。

[[[generic-scratch3-sprite-from-library]]]

\--- /任務\---

\---任務\---

當遊戲開始時，應該隱藏 `閃電` 精靈，直到宇宙飛船發射激光炮。

將此代碼添加到 `Lightning` 精靈：

![閃電精靈](images/lightning-sprite.png)

```blocks3
點擊綠色標誌時
隱藏
```

\--- /任務\---

目前，與宇宙飛船相比，閃電確實很大！

\---任務\---

在 `Lightning` 精靈已有的代碼下方，添加一些塊以使精靈更小並將其顛倒。

![閃電精靈](images/lightning-sprite.png)

```blocks3
將大小設置為（25）％
方向（-90）
```

現在它似乎從太空船發射尖端的尖端。

\--- /任務\---

\---任務\---

如果按下 <kbd>空格</kbd> 鍵，則向 `Spaceship` 精靈添加一些新代碼以創建閃電的新克隆。

\---提示\---

\---提示\---

`當單擊綠色標誌`{：class =“block3events”}時，請繼續檢查 `{`} = {block3control“} `如果`{：class =”block3control“}按下 `空格鍵`{： class =“block3sensing”}，在這種情況下， `創建一個Lightning`{：class =“block3control”}精靈的克隆。

\--- /提示\---

\---提示\---

以下是您需要的塊：

```blocks3
如果 <> 然後
結束

永遠
結束

當標記點擊時創建（Lightning v）

<key (space v) pressed?>

克隆
```

\--- /提示\---

\---提示\---

以下是您的新代碼應如下所示：

![火箭精靈](images/rocket-sprite.png)

```blocks3
當標誌點擊
永遠
    如果 <key (space v) pressed?> 然後
        創建克隆（閃電v）
    結束
結束
```

\--- /提示\---

\--- /提示\---

\--- /任務\---

\---任務\---

每當遊戲創建 `Lightning` 精靈克隆時，克隆應該出現，然後向上移動直到它到達舞台的頂部。然後克隆應該消失。

將此代碼添加到 `Lightning` 精靈中，以便它的克隆向上移動直到它們觸及舞台的邊緣，然後它們被刪除。

![閃電精靈](images/lightning-sprite.png)

```blocks3
    當我作為克隆
    開始時去（太空飛船v）
    顯示
    重複直到 <touching (edge v) ?>
        改變y由（10）
    結束
    刪除此克隆
```

\--- /任務\---

\---任務\---

按 <kbd>空格</kbd> 鍵測試閃電是否正確移動。

\--- /任務\---