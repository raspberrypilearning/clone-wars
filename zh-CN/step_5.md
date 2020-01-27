## 会飞的太空河马

现在，您将添加许多试图破坏飞船的飞行河马。

\--- task \---

在 Scratch 库中用'Hippo1' 图像创建一个新的角色。 使用**收缩**工具使`河马`角色和`飞船`差不多大小。

![截屏](images/invaders-hippo.png)

\--- /task \---

\--- task \---

设置`河马`角色的旋转样式为** 左-右 ** 。

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

添加一些代码以在游戏开始时隐藏`河马`角色。

![河马角色](images/hippo-sprite.png)

```blocks3
当 ⚑ 被点击
隐藏
```

\--- /task \---

\--- task \---

添加一些代码到舞台，每隔几秒钟创建一个`河马`克隆。

\--- hints \---

\--- hint \---

当 `绿色旗帜被点击时`{:class="block3events"}, `重复地`{:class="block3control"} `等待`{:class="block3control"} `2~4秒`{:class="block3operators"} 然后 `创建一个河马角色克隆`{:class="block3control"}.

\--- /hint \---

\--- hint \---

以下是你需要的代码块：

```blocks3
重复执行
end

克隆 (Hippo1 v)

(在 (2) 和 (4) 之间取随机数)

当 ⚑ 被点击

等待 () 秒
```

\--- /hint \---

\--- hint \---

你的代码看起来应该是这样的：

![舞台角色](images/stage-sprite.png)

```blocks3
当 ⚑ 被点击
重复执行 
  等待 (在 (2) 和 (4) 之间取随机数) 秒
  克隆 (Hippo1 v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

每个新的河马克隆都应该出现在随机的`x`位置上，每个克隆都应该有随机的速度。

\--- task \---

创建一个新变量，名为`速度`{:class="block3variables"}，只应用于 `河马` 角色

[[[generic-scratch3-add-variable]]]

正确完成此操作后，变量旁边会带有角色的名称，如下所示：

![截屏](images/invaders-var-test.png)

\--- /task \---

\--- task \---

每个`河马`克隆启动时，选择随机的速度和起点。然后在屏幕上显示克隆。

```blocks3
当作为克隆体启动时
将 [speed v] 设为 (在 (2) 和 (4) 之间取随机数)
移到 x: (在 (-220) 和 (220) 之间取随机数) y: (150)
显示
```

\--- /task \---

\--- task \---

测试您的代码。是否每隔几秒钟出现一个新的河马？

\--- /task \---

目前，河马没有移动。

\--- task \---

每个河马都应该随机移动，直到被闪电击中。 要做到这一点，请在`河马`角色已有的的代码脚本中的代码块下面附上此代码：

```blocks3
重复执行直到 <touching (lightning v) ?> 
  移动 (speed :: variables) 步
  右转 ↻ (在 (-10) 和 (10) 之间取随机数) 度
  碰到边缘就反弹
end
删除此克隆体
```

\--- /task \---

\--- task \---

再次测试您的代码。您应该看到每隔几秒钟就会出现一个新的河马克隆，并且每个克隆应以不同的速度移动。

\--- no-print \---

![截屏](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

现在测试飞船的激光大炮。如果闪电击中河马，河马会消失吗？

\--- /task \---