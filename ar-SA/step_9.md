## انتهت اللعبة

لزيادة مستوى صعوبة اللعبة، لننشئ خفاش يرمي برتقالًا على سفينة الفضاء.

![خفاش يرمي برتقالة على سفينة الفضاء](images/bat-oranges.png)

--- task ---

أضف كائن `Bat` وعيِّن أسلوب دورانه إلى **يسار-يمين** فقط.

--- /task ---

--- task ---

اجعل الكائن `Bat` `يتحرك`{:class="block3motion"} من جانب إلى آخر أعلى المنصة ضمن حلقة `كرِّر باستمرار`{:class="block3control"}.

![كائن الخفاش](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

تذكر أن تختبر تعليماتك البرمجية.

--- /task ---

إذا نظرتَ إلى مظاهر الخفاش، فستجد انه لديه أربع مظاهر مختلفة:

![لقطة الشاشة](images/invaders-bat-costume.png)

--- task ---

استخدم لبنة `المظهر التالي`{:class="block3looks"} لتجعل الخفاش يضرب بجناحيه أثناء تحركه.

--- hints ---


--- hint ---

بعد أن يتحرك الخفاش، يجب أن يظهر `المظهر التالي`{:class="block3looks"} ثم `ينتظر`{:class="block3control"} لفترة قصيرة.

--- /hint ---

--- hint ---

تحتاج إلى إضافة هذه الكتل للكود الخاصة بك:

```blocks3
wait (0.3) seconds

next costume
```

--- /hint ---

--- hint ---

يجب أن تبدو التعليمات البرمجية خاصتك بالشكل التالي:

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

--- /hint ---

--- /hints ---

--- /task ---

والآن، لنجعل الخفاش يرمي البرتقال!

--- task ---

أضف كائن `Orange` جديدًا من مكتبة سكراتش.

![لقطة الشاشة](images/invaders-orange.png)

--- /task ---

--- task ---

أضف تعليمات برمجية إلى خفاشك بحيث `عند النقر على العلم`{:class="block3events"}، فإن كائن `الخفاش` `إلى الأبد`{:class="block3control"} `ينتظر`{:class="block3control"} `فترة زمنية عشوائية`{:class="block3operators"}، بين `٥ إلى ١٠`{:class="block3operators"} ثانية، ثم `ينشيء نسخة`{:class="block3control"} من كائن `البرتقالة`.

![كائن الخفاش](images/bat-sprite.png)

```blocks3
when flag clicked
forever
	wait (pick random (5) to (10)) secs
	create clone of (Orange v)
end
```

--- /task ---

--- task ---

أضف التعليمات البرمجية إلى كائن `البرتقالة` لجعل كل نسخة منها تسقط، بدءاً من كائن `الخفاش` نحو أسفل المنصة.

![كائن البرتقالة](images/orange-sprite.png)

```blocks3
    عند نقر ⚑
    اختفِ

    when I start as a clone
	  go to (Bat v)
	  show
	  repeat until <touching (الحافة v)?
		  change y by (-4)
	  end
	  delete this clone
```

--- /task ---

--- task ---

أضف بعض التعليمات البرمجية الأخرى إلى كائن البرتقالة `Orange` بحيث عندما تصطدم `برتقالة` بكائن سفينة الفضاء `Spaceship`، تختفي النسخة الآخرى لتعطي اللاعب فرصة لاستعادة قوته:

![كائن البرتقالة](images/orange-sprite.png)

```blocks3
    when I receive [hit v]
	  delete this clone
```

--- /task ---

--- task ---

قم أيضًا بتعديل التعليمة البرمجية في الكائن `Spaceship` بحيث يصطدم عندما يلامس كائن فرس النهر `Hippo` أو كائن برتقالة `Orange`:

![كائن الصاروخ](images/rocket-sprite.png)

```blocks3
    انتظر حتى <<touching (Hippo1 v)?> أو <touching (Orange v)?>>
```

--- /task ---

--- task ---

اختبر لعبتك. ماذا سيحدث إذا اصطدمت السفينة ببرتقالة ساقطة؟

--- /task ---