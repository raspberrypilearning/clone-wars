## 消失的河马

当飞船爆炸时，所有河马都应消失，以便游戏中的玩家可以重新开始。

\--- task \---

将代码添加到宇宙飞船角色中，在`宇宙飞船碰到一只河马`{:class="block3sensing"}时使它`广播`{:class="block3events"} “被击中”的消息。

![火箭角色](images/rocket-sprite.png)

```blocks3
当 ⚑ 被点击
换成 (normal v) 造型
等待 <touching (Hippo1 v)>
换成 (hit v) 造型
```

\--- /task \---

\--- task \---

所有的`河马`角色克隆都将收到“被击中”的消息， 并且你可以指示他们在飞船被击中时消失，将此代码添加到`河马`角色:

![河马角色](images/hippo-sprite.png)

```blocks3
当接收到 [hit v]
删除此克隆体
```

\--- /task \---

\--- task \---

要检查新代码是否正常工作，请单击绿色旗帜并使宇宙飞船与河马碰撞。

![截屏](images/invaders-hippo-collide.png)

\--- /task \---

飞船爆炸后，新的`河马`克隆出现，但飞船仍会爆炸！宇宙飞船被击中后需要自行重置。

\--- task \---

在`飞船`角色的代码末尾添加一个`等待`{:class="block3control"}代码块，以在河马再次出现之前创建一个小暂停。 然后添加一个`重复执行`{:class="block3control"}代码块包含你所有的代码，让代码重复运行。

![火箭角色](images/rocket-sprite.png)

```blocks3
当 ⚑ 被点击
重复执行 
 换成 (normal v) 造型
 等待 <touching (Hippo1 v)>
 换成 (hit v) 造型
 广播 (hit v)
 + 等待 (1) 秒
end
```

\--- /task \---