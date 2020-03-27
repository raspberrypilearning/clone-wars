## إخفاء أفراس الفضاء

عندما تنفجر سفينة الفضاء، يجب أن تختفي كل الأفراس لإعطاء اللاعب فرصة لاستعادة قوته.

--- task ---

أضف تعليمات برمجية إلى كائن سفينة الفضاء لجعلها `تبث`{:class="block3events"} الرسالة "اصطدام" عندما تلمس سفينة الفضاء `فرس النهر`{:class="block3sensing"}.

![كائن الصاروخ](images/rocket-sprite.png)

```blocks3
when flag clicked
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (hit v)
+ broadcast (hit v)
```

--- /task ---

--- task ---

كل نسخ كائنات `فرس النهر` ستتلقى رسالة "اصطدام" ، ويمكنك إرشادهم بالاختفاء عند إصابة سفينة الفضاء بإضافة هذه الكود إلى كائن `فرس النهر`:

![كائن فرس النهر](images/hippo-sprite.png)

```blocks3
when I receive [hit v]
delete this clone
```

--- /task ---

--- task ---

لمعرفة ما إذا كان الكود الجديد يعمل أم لا، انقر فوق العلم الأخضر واجعل سفينة الفضاء تصطدم بفرس النهر.

![لقطة الشاشة](images/invaders-hippo-collide.png)

--- /task ---

بعد انفجار سفينة الفضاء، فإن نسخة جديدة من كائن `فرس النهر` تظهر، لكن سفينة الفضاء ما زالت تنفجر! سفينة الفضاء تحتاج إلى إعادة ضبط نفسها بعد أن تضرب.

--- task ---

أضف كتلة `انتظر`{:class="block3control"} في نهاية التعليمات البرمجية لكائن `Spaceship` لإنشاء وقفة صغيرة قبل أن تبدأ فرس النهر بالظهور مرة أخرى. ثم أضف لبنة `كرر باستمرار`{:class="block3control"} حول جميع التعليمات البرمجية الخاصة بك لتشغيل الكود بشكل متكرر.

![كائن الصاروخ](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
switch costume to (normal v)
wait until <touching (Hippo1 v)>?
switch costume to (hit v)
broadcast (hit v)
+ wait (1) seconds
end
```

--- /task ---