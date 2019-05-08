## أفراس فضاء طائرة

Now you're going to add lots of flying hippos that try to destroy your spaceship.

\--- task \---

Create a new sprite with the 'Hippo1' image in the Scratch library. Use the **shrink** tool to make the `Hippo` sprite a similar size to the `Spaceship` sprite.

![لقطة الشاشة](images/invaders-hippo.png)

\---/task--

\--- task \---

Set the `Hippo` sprite's rotation style to **left-right**.

[[[generic-scratch3-sprite-rotation-style]]]

\--- /task \---

\--- task \---

أضف بعض التعليمات البرمجية لإخفاء الكائن `Hippo` عندما تبدأ اللعبة.

![hippo sprite](images/hippo-sprite.png)

```blocks3
عند نقر ⚑
اختف
```

\--- /task \---

\--- task \---

Add some code to the Stage to create a new `Hippo` clone every few seconds.

\--- hints \---

\--- hint \---

When the `green flag is clicked`{:class="block3events"}, `repeatedly`{:class="block3control"} `wait`{:class="block3control"} `between 2 and 4 seconds`{:class="block3operators"} and then `create a clone of the Hippo sprite`{:class="block3control"}.

\--- hint/ \---

\--- hint \---

إليك الكتل التي تحتاجها:

```blocks3
forever
end

create clone of (Hippo1 v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

\--- hint/ \---

\--- hint \---

و هذا ما يجب أن تبدو عليه التعليمات البرمجية الخاصة بك:

![stage sprite](images/stage-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (2) to (4)) secs
    create clone of (Hippo1 v)
end
```

\--- hint/ \---

\--- hints/ \---

\--- /task \---

Each new hippo clone should appear at a random `x` position, and every clone should have a random speed.

\--- task \---

Create a new variable called `speed`{:class="block3variables"} that is for the `Hippo` sprite only.

[[[generic-scratch3-add-variable]]]

When you've done this correctly, the variable has the name of the sprite next to it, like this:

![لقطة الشاشة](images/invaders-var-test.png)

\--- /task \---

\--- task \---

When each `Hippo` clone starts, pick a random speed and starting place for it. Then show the clone on the screen.

```blocks3
عندما تبدأ نسخة مني
اجعل [speed v] مساوياً (اختر عدداً عشوائياً بين (2) و (4))
اذهب إلى الموضع س: (اختر عدداً عشوائياً بين (-220) و (220)) ص: (150)
اظهر
```

\--- /task \---

\--- task \---

Test your code. Does a new hippo appear every few seconds?

\--- /task \---

At the moment the hippos don't move.

\--- task \---

Each hippo should move around randomly until it gets hit by a lightning bolt. To make that happen, attach this code below the blocks that are already in the `Hippo` sprite's code script:

```blocks3
repeat until <touching (lightning v) ?>
    move (speed :: variables) steps
    turn right (pick random (-10) to (10)) degrees
    if on edge, bounce
end
delete this clone
```

\--- /task \---

\--- task \---

Test your code again. You should see a new hippo clone appear every few seconds, and each clone should move at a different speed.

\--- no-print \---

![لقطة الشاشة](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

Now test the spaceship's laser cannon. If a lightning bolt hits a hippo, does the hippo vanish?

\--- /task \---