## 制作一个宇宙飞船

首先造一个可以保护地球的宇宙飞船！

\--- task \---

打开“克隆战争”的Scratch初始项目。

**在线：** 在 [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target =“_ blank”}打开初始项目。

如果您有Scratch帐户，可以单击**改编**制作副本。

**离线：** 从 [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go) 下载初始项目，然后使用Scratch离线编辑器打开它。

如果您需要下载并安装Scratch离线编辑器，可以在[ rpf.io/scratchoff ](https://rpf.io/scratchoff)中获取 {：target="_blank"}。

\--- /task \---

![初始项目](images/starter-project.png)

\--- task \---

添加此代码到飞船角色中，让飞船在按下<kbd>左</kbd> 箭头键时向左移动：

![火箭角色](images/rocket-sprite.png)

```blocks3
    当 ⚑ 被点击
重复执行 
  如果 <key (left arrow v) pressed?> 那么 
    将x坐标增加 (-4)
  end
end
```

x轴从舞台的左侧到右侧。 这意味着当您减少飞船角色的`x`位置值时，它将往左移动。 因此，此代码块的这个部分将会使您的飞船向左移动：

```blocks3
将x改变（-4）
```

\--- /task \---

\--- task \---

在`重复执行`{:clas="block3control"} 块里添加一些代码，使你的飞船在按下 <kbd>右</kbd> 箭头键时往右移动。

\--- hints \---

\--- hint \---

从飞船的位置值`x`中减去`4`使其向左移动，所以相反的，你如何使飞船向右移动`4`？

\--- /hint \---

\--- hint \---

您需要相同的代码块，但数字不同：

```blocks3
将x改变（）
```

\--- /hint \---

\--- hint \---

这是你需要在`重复执行`{:class="block3control"} 块内的其它代码下添加的代码：

![火箭角色](images/rocket-sprite.png)

```blocks3
if <key (right arrow v) pressed?> then
    change x by (4)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

单击绿色旗帜测试您的项目。您可以按箭头键使您的飞船左右移动

\--- /task \---