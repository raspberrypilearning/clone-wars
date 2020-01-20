## انتهت اللعبة

لزيادة مستوى صعوبة اللعبة، لننشئ خفاش يرمي برتقالًا على سفينة الفضاء.

![خفاش يرمي برتقالة على سفينة الفضاء](images/bat-oranges.png)

\--- task \---

أضف كائن `Bat` وعيِّن أسلوب دورانه إلى **يسار-يمين** فقط.

\---/task--

\--- task \---

اجعل الكائن `Bat` `يتحرك`{:class="blockmotion"} من جانب إلى آخر أعلى المنصة ضمن حلقة `كرِّر باستمرار`{:class="blockcontrol"}.

![كائن الخفاش](images/bat-sprite.png)

```blocks3
عند نقر ⚑
اجعل الحجم مساويًا (50) ٪
كرِّر باستمرار 
  تحرك (10) خطوة
  ارتد إذا كنت عند الحافة
end
```

تذكر أن تختبر تعليماتك البرمجية.

\---/task\---

إذا نظرتَ إلى مظاهر الخفاش، فستجد انه لديه أربع مظاهر مختلفة:

![لقطة الشاشة](images/invaders-bat-costume.png)

\--- task \---

استخدم لبنة `المظهر التالي`{:class="blocklooks"} لتجعل الخفاش يضرب بجناحيه أثناء تحركه.

\--- hints \---

\--- hint \---

بعد أن يتحرك الخفاش، يجب أن يظهر `المظهر التالي`{:class="blocklooks"} ثم `ينتظر`{:class="blockcontrol"} لفترة قصيرة.

\--- hint/ \---

\--- hint \---

تحتاج إلى إضافة هذه الكتل للكود الخاصة بك:

```blocks3
انتظر (0.3) ثانية

المظهر التالي
```

\--- hint/ \---

\--- hint \---

You code should look like this:

```blocks3
عند نقر ⚑
اجعل الحجم مساويًا (50) ٪
كرِّر باستمرار 
 تحرك (10) خطوة
 ارتد إذا كنت عند الحافة

 + المظهر التالي
 + انتظر (0.3) ثانية
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
عند نقر ⚑
كرِّر باستمرار 
  انتظر (عدد عشوائي بين (5) و (10)) ثانية
  أنشئ نسخة من (Orange v)
end
```

\--- /task \---

\--- task \---

Add code to the `Orange` to make each of its clone drop, starting from the `Bat` sprite and falling towards the bottom of the Stage.

![orange sprite](images/orange-sprite.png)

```blocks3
    عند نقر ⚑
اختفِ

عندما تبدأ نسخة مني
اذهب إلى (Bat v)
اظهر
كرِّر حتى< ملامس لـ (edge v)
  غيِّر الموضع ص بمقدار (-4)
end
احذف هذه النسخة
```

\--- /task \---

\--- task \---

Add some more code to the `Orange` sprite so that when an `Orange` clone hits the `Spaceship` sprite, the clone also disappears to give the player a chance to reset:

![orange sprite](images/orange-sprite.png)

```blocks3
    عندما تستقبل [hit v]
احذف هذه النسخة
```

\--- /task \---

\--- task \---

Modify the code of your `Spaceship` sprite so that the sprite is "hit" when it touches a `Hippo` sprite or an `Orange` sprite:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    انتظر حتى <<touching (Hippo1 v)?> أو<touching (Orange v)?>>
```

\--- /task \---

\--- task \---

Test your game. What happens if the spaceship gets hit by a falling orange?

\--- /task \---