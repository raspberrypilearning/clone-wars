## 우주 박쥐

게임을 조금 더 어렵게 만들려면 우주선에서 오렌지를 던지는 박쥐를 만들어야합니다.

![우주선에서 오렌지를 던지는 박쥐](images/bat-oranges.png)

\--- task \---

`박쥐` 스프라이트를 추가하고 회전 스타일을 왼쪽에서 오른쪽으로 **설정하십시오**.

\--- /task \---

\--- task \---

`Bat` 스프라이트 `Stage <code>의 맨 위에서 왼쪽에서 오른쪽으로`{: class = "block3motion"} 영원히</code>{: class = "block3control"} 이동시킵니다.

![박쥐 스프 라이트](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

Remember to test your code.

\--- /task \---

If you look at the bat's costumes, you can see that it has four different ones:

![스크린샷](images/invaders-bat-costume.png)

\--- task \---

Use the `next costume`{:class="block3looks"} block to make the bat flap its wings as it moves.

\--- 힌트 \---

\--- hint \---

After the bat has moved, it should show the `next costume`{:class="block3looks"} and then `wait`{:class="block3control"} for a short time.

\--- /귀뜸말 \---

\--- hint \---

You need to add these blocks to you code:

```blocks3
wait (0.3) seconds

next costume
```

\--- /귀뜸말 \---

\--- hint \--- You code should look like this:

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

\--- /귀뜸말 \---

\--- / 귀뜸말 \---

\--- /task \---

Now make the bat throw oranges!

\--- task \---

Add an `Orange` sprite from the Scratch library.

![스크린샷](images/invaders-orange.png)

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