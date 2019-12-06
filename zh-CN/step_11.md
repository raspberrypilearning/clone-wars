## 挑战：完善你的游戏

您可以对自己的游戏进行哪些改进？

下面是一些建议：

+ 添加您可以收集来获得额外生命的医疗包。

![截屏](images/invaders-aid.png)

+ 添加您的飞船必须避免的浮石。

![截屏](images/invaders-rocks.png)

+ 当你得分达到`100`时，让更多的敌人出现。

```blocks3
    wait until <(score :: variables) = [100]>
```