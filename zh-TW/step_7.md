## 河馬消失了

當宇宙飛船爆炸時，所有的河馬都應該消失，這樣遊戲的玩家才能恢復。

\---任務\---

添加代碼到太空飛船精靈，使其成為 `廣播`{：class =“block3events”}當 `艘太空飛船接觸河馬`{：class =“block3sensing”}時，消息“命中”。

![火箭精靈](images/rocket-sprite.png)

```blocks3
當標誌點擊
切換服裝到（正常v）
等待 <touching (Hippo1 v)>？
開關服裝到（打v）

+廣播（點擊v）
```

\--- /任務\---

\---任務\---

所有 `Hippo` sprite克隆都將收到“命中”消息，你可以通過將此代碼添加到 `Hippo` 精靈來指示它們在飛船被擊中時消失：

![河馬精靈](images/hippo-sprite.png)

```blocks3
當我收到[點擊v]
刪除此克隆
```

\--- /任務\---

\---任務\---

要檢查新代碼是否有效，請單擊綠色標記並使太空飛船與河馬發生碰撞。

![截圖](images/invaders-hippo-collide.png)

\--- /任務\---

宇宙飛船爆炸後，出現了新的 `Hippo` 克隆，但宇宙飛船仍在爆炸！宇宙飛船在被擊中後需要自行重置。

\---任務\---

在 `艘Spaceship` 精靈的代碼末尾添加一個 `等待`{：class =“block3control”}塊，以便在河馬再次出現之前創建一個小暫停。 然後在所有代碼周圍添加一個 `永久`{：class =“block3control”}塊，以使代碼重複運行。

![火箭精靈](images/rocket-sprite.png)

```blocks3
當標誌點擊
永遠
開關服裝到（正常v）
等到 <touching (Hippo1 v)>？
開關服裝到（點擊v）
廣播（點擊v）

+等待（1）秒
結束
```

\--- /任務\---