## صواعق برقية

الآن سوف نعطي سفينة الفضاء القدرة على إطلاق صواعق برقية!

--- task ---

أضف كائن `Lightning` من مكتبة سكراتش.

[[[generic-scratch3-sprite-from-library]]]

--- /task ---

--- task ---

عندما تبدأ اللعبة، يجب أن يكون كائن `البرق` مختفياً إلى أن تطلق سفينة الفضاء مدافع الليزر.

أضف هذه التعليمات البرمجية إلى الكائن `Lightning`:

![كائن البرق](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

--- /task ---

في الوقت الحالي، صاعقة البرق كبيرة جدًا مقارنة بسفينة الفضاء!

--- task ---

بعد كتلة التعليمات البرمجية الخاصة بالكائن `Lightning`، أضف بعض الكتل لجعل الكائن أصغر وإظهاره بشكل مقلوب.

![كائن البرق](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

الآن يبدو أنها تطلق نهاية مدببة - أولاً من سفينة الفضاء.

--- /task ---

--- task ---

أضف بعض التعليمات البرمجية الجديدة لتجعل كائن `Spaceship` يُطلق صاعقة برقية جديدة في أي وقت يتم فيه الضغط على مفتاح <kbd>المسافة</kbd>.

--- hints ---


--- hint ---

`عند النقر فوق العلم الأخضر`{:class="block3events"}، استمر في التحقق `إلى الأبد`{:class="block3control"} `إذا`{:class="block3control"} تم الضغط على `مفتاح المسافة`{:class="block3sensing"}، في هذه الحالة `أنشئ نسخة من كائن البرق`{:class="block3control"}.

--- /hint ---

--- hint ---

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

--- /hint ---

--- hint ---

هذا ما يجب أن يبدو عليه الرمز البرمجي الجديد:

![كائن الصاروخ](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
	if <key (space v) pressed?> then
		create clone of (Lightning v)
	end
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

كلما تقوم اللعبة بإنشاء نسخة من الكائن `Lightning`، يجب أن تظهر النسخة ثم تتحرك للأعلى حتى تصل إلى قمة المنصة. ثم يجب أن تختفي النسخة.

أضف هذه التعليمات البرمجية إلى الكائن `Lightning` بحيث تتحرك الكائنات المستنسخة لأعلى حتى تلامس حافة المنصة، ثم يتم حذفها.

![كائن البرق](images/lightning-sprite.png)

```blocks3
  when I start as a clone
	go to (Spaceship v)
  show
	repeat until <touching (edge v) ?>
		change y by (10)
	end
	delete this clone
```

--- /task ---

--- task ---

اضغط على مفتاح <kbd>المسافة</kbd> لتختبر ما إذا كانت الصواعق البرقية تُطلق الآن من مكانها الصحيح أم لا.

--- /task ---