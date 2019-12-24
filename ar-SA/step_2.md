## إنشاء سفينة فضاء

أولاً قم بعمل مركبة فضائية يمكنها الدفاع عن الأرض!

\--- task \---

افتح المشروع المبدئي "حرب العوالم".

**بالاتصال بالانترنت**: افتح المشروع المبدئي من هنا [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target="_blank"}.

اذا كنت تملك حساب على منصة السكراتش (Scratch) فيمكنك عمل نسخة بالضغط على **Remix**.

**بدون اتصال انترنت** حمّل المشروع المبدئي من [rpf.io/p/en/clone-wars-go](http://rpf.io/p/en/clone-wars-go)، ثم افتحه باستخدام محرر سكراتش بدون اتصال انترنيت.

اذا تحتاج تنزيل وتنصيب برنامج السكراتش Scratch على جهازك الشخصي، ستجده في [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

\--- /task \---

![starter project](images/starter-project.png)

\--- task \---

أضف هذا الرمز إلى كائن سفينة الفضاء لجعلها تتحرك يسارًا إذا كان السهم المضغوط هو <kbd>يسار</kbd>:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    عند نقر ⚑
كرر باستمرار 
  إذا <key (left arrow v) pressed?> 
    غيِّر الموضع س بمقدار (-4)
  end
end
```

ينتقل المحور السيني من الجانب الأيسر من المنصة إلى الجانب الأيمن. هذا يعني أن سفينة الفضاء تنتقل إلى اليسار عندما تطرح من قيمة المحور `س` لسفينة الفضاء. So this code block is the part that makes your spaceship move left:

```blocks3
غيِّر الموضع س بمقدار (-4)
```

\--- /task \---

\--- task \---

Add some more code inside the `forever`{:class="block3control"} block to make your spaceship move to the right if the <kbd>right</kbd> arrow key is pressed.

\--- hints \---

\--- hint \---

Subtracting `4` from the spaceship's `x` position made it move left, so how could you make the spaceship move right by `4` instead?

\--- hint/ \---

\--- hint \---

You need the same code block, but with a different number:

```blocks3
غيِّر الموضع س بمقدار ()
```

\--- hint/ \---

\--- hint \---

Here is the code you need to add below the other code inside the `forever`{:class="block3control"} block:

![rocket sprite](images/rocket-sprite.png)

```blocks3
if <key (right arrow v) pressed?> then
    change x by (4)
end
```

\--- hint/ \---

\--- hints/ \---

\--- /task \---

\--- task \---

Test your project by clicking the green flag. Can you press the arrow keys to make your spaceship move left and right?

\--- /task \---