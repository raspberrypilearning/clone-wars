## 太空蝙蝠

为使您的游戏变得更有难度一点，您将要创建一个向飞船扔橙子的蝙蝠。

![一只向飞船投橙子的蝙蝠](images/bat-oranges.png)

\--- task \---

添加一个`蝙蝠`角色并将其旋转风格设置为 **左-右**。

\--- /task \---

\--- task \---

使`蝙蝠`角色在舞台顶部从左至右`移动`{:class="block3motion"}`重复执行`{:class="block3control"}。

![蝙蝠角色](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

请记得测试您的代码。

\--- /task \---

如果您看一下蝙蝠的造型，您会发现它有四种不同的造型：

![截屏](images/invaders-bat-costume.png)

\--- task \---

使用`下一个造型` {:class =“ block3looks”}代码块使蝙蝠在移动时拍打翅膀。

\--- hints \---

\--- hint \---

蝙蝠移动后，应显示`下一个造型` {:class =“ block3looks”}，然后`等待` {:class =“ block3control”}一小段时间。

\--- /hint \---

\--- hint \---

您需要将这些代码块添加到您的代码中：

```blocks3
wait (0.3) seconds

next costume
```

\--- /hint \---

\--- hint \---

You code should look like this:

```blocks3
when flag clicked
set size to (50) %
forever
move (10) steps
if on edge, bounce

+ next costume
+ wait (0.3) seconds
end
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
when flag clicked
forever
    wait (pick random (5) to (10)) secs
    create clone of (Orange v)
end
```

\--- /task \---

\--- task \---

Add code to the `Orange` to make each of its clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

![orange sprite](images/orange-sprite.png)

```blocks3
    when flag clicked
    hide

    when I start as a clone
    go to (Bat v)
    show
    repeat until <touching (edge v)?
        change y by (-4)
    end
    delete this clone
```

\--- /task \---

\--- task \---

Add some more code to the `Orange` sprite so that when an `Orange` clone hits the `Spaceship` sprite, the clone also disappears to give the player a chance to reset:

![orange sprite](images/orange-sprite.png)

```blocks3
    when I receive [hit v]
    delete this clone
```

\--- /task \---

\--- task \---

Modify the code of your `Spaceship` sprite so that the sprite is "hit" when it touches a `Hippo` sprite or an `Orange` sprite:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    wait until < <touching (Hippo1 v)?> or <touching (Orange v)?>>
```

\--- /task \---

\--- task \---

Test your game. What happens if the spaceship gets hit by a falling orange?

\--- /task \---