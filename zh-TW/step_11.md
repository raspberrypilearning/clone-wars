## 挑戰：遊戲改良

你的遊戲有哪些地方可以改良？

給你一些靈感：

+ 添加醫療包，飛船獲得後可增加生命。

![截圖](images/invaders-aid.png)

+ 你的飛船還要避開漂浮在太空的隕石。

![截圖](images/invaders-rocks.png)

+ 當你的得分達到 `100`時，分身大軍會傾巢而出。

```blocks3
wait until <(得分 :: variables) = [100]>
```