## صواعق برقية

الآن سوف نعطي سفينة الفضاء القدرة على إطلاق صواعق برقية!

\--- task \---

أضف كائن `Lightning` من مكتبة Scratch.

[[[generic-scratch3-sprite-from-library]]]

\---/task--

\--- task \---

عندما تبدأ اللعبة ، يجب إخفاء كائن ` البرق ` الى أن تطلق سفينة الفضاء مدافع الليزر.

أضف هذه التعليمات البرمجية إلى الكائن ` Lightning `:

![lightning sprite](images/lightning-sprite.png)

```blocks3
عند نقر ⚑
اختف
```

\---/task\---

في الوقت الحالي، صاعقة البرق كبيرة جدًا مقارنة بسفينة الفضاء!

\--- task \---

أدناه التعليمات البرمجية موجودة بالفعل في كائن ` Lightning `، أضف بعض الكتل لجعل الكائن أصغر وتحويله رأسا على عقب.

![lightning sprite](images/lightning-sprite.png)

```blocks3
اجعل الحجم مساوياً (25) %
اتجه نحو الاتجاه (-90 v)
```

الآن يبدو أنها تطلق نهاية مدببة - أولاً من سفينة الفضاء.

\--- /task \---

\--- task \---

أضف بعض التعليمات البرمجية الجديدة لتجعل كائن `Spaceship` يُطلق صاعقة برقية جديدة في أي وقت يتم فيه الضغط على مفتاح <kbd>المسافة</kbd>.

\--- hints \---

\--- hint \---

`When the green flag is clicked`{:class="block3events"}, keep checking `forever`{:class="block3control"} `if`{:class="block3control"} the `space key is pressed`{:class="block3sensing"}, and in that case `create a clone of the Lightning`{:class="block3control"} sprite.

\--- hint/ \---

\--- hint \---

إليك الكتل التي تحتاجها:

```blocks3
if <> then
end

forever
end

create clone of (Lightning v)

<key (space v) pressed?>

when flag clicked
```

\--- hint/ \---

\--- hint \---

Here is what your new code should look like:

![rocket sprite](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
    if <key (space v) pressed?> then
        create clone of (Lightning v)
    end
end
```

\--- hint/ \---

\--- hints/ \---

\--- /task \---

\--- task \---

Whenever the game creates a `Lightning` sprite clone, the clone should appear and then move upwards until it reaches the top of the Stage. Then the clone should disappear.

Add this code to the `Lightning` sprite so that clones of it move upwards until they touch the edge of the Stage, and then they get deleted.

![lightning sprite](images/lightning-sprite.png)

```blocks3
    when I start as a clone
    go to (Spaceship v)
    show
    repeat until <touching (edge v) ?>
        change y by (10)
    end
    delete this clone
```

\--- /task \---

\--- task \---

Press the <kbd>space</kbd> key to test whether the lightning bolt moves correctly.

\--- /task \---