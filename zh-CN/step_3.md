## 闪电束

现在，您将让您的飞船能够发射闪电束！

\--- task \---

从Scratch库添加 `闪电` 角色。

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

游戏开始时，在飞船发射激光大炮之前，`闪电`角色应当是隐藏起来的。

将此代码添加到`闪电`角色：

![闪电角色](images/lightning-sprite.png)

```blocks3
当 ⚑ 被点击
隐藏
```

\--- /task \---

此时，闪电比宇宙飞船还要大！

\--- task \---

在`闪电`精灵已有的代码下，添加一些代码块使角色变小并向将其上下颠倒。

![闪电角色](images/lightning-sprite.png)

```blocks3
将大小设为 (25)
面向 (-90) 方向
```

现在它看起来像是尖尖的尾巴-首先从飞船中射出。

\--- /task \---

\--- task \---

给`飞船` sprite 添加一些新代码，以便在按下 <kbd>空格</kbd> 键时创建一个新的闪电的克隆。

\--- hint \---

\--- hint \---

`当绿色旗帜被点击时`{:class="block3events"}, 持续检查 `重复执行`{:class="block3control"} `如果`{:class="block3control"}`按下空格键`{:class="block3sensing"}, 那么 `创建一个克隆闪电`{:class="block3control"}角色.

\--- /hint \---

\--- hint \---

以下是您需要的代码块：

```blocks3
如果 <> 那么
end

重复执行
end

克隆 (Lightning v)

<key (space v) pressed?>

当 ⚑ 被点击
```

\--- /hint \---

\--- hint \---

您的代码看起来应该是这样的：

![火箭角色](images/rocket-sprite.png)

```blocks3
当 ⚑ 被点击
重复执行 
  如果 <key (space v) pressed?> 那么 
    克隆 (Lightning v)
  end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

每当游戏创建一个 `闪电` 角色克隆时，克隆的角色就会出现并且向上移动直到到达舞台顶端。 之后克隆就会消失。

将此代码添加到`闪电`角色，从而使其克隆向上移动，直到他们碰到舞台的边缘。 然后他们将被删除。

![闪电角色](images/lightning-sprite.png)

```blocks3
    当作为克隆体启动时
移到 (Spaceship v)
显示
重复执行直到 <touching (edge v) ?> 
  将y坐标增加 (10)
end
删除此克隆体
```

\--- /task \---

\--- task \---

按<kbd>空格</kbd>键测试闪电是否正确移动。

\--- /task \---