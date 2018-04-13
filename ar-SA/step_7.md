## إخفاء أفراس الفضاء

عندما تصطدم سفينة الفضاء، يجب أن تختفي كل الأفراس لإعطاء اللاعب فرصة لاستعادة القوة.

+ أضف قالب إلى التعليمة البرمجية بهدف `بث` رسالة "اصطدام" عندما تلامس سفينة الفضاء فرسًا.

[[[generic-scratch-broadcast-message]]]

--- hints ---
--- hint ---
أنشئ قالب `بُث` 'اصطدام' من خلال سحب القالب من علامة التبويب **أحداث** ثم النقر على القائمة المنسدلة وتحديد **رسالة جديدة**.
--- /hint ---
--- hint ---
يجب أن يكون القالب كما يلي:
```blocks
broadcast [hit v]
```
--- /hint ---
--- hint ---
يجب أن تكون التعليمة البرمجية كما يلي:

```blocks
when flag clicked
switch costume to [normal v]
wait until <touching [Hippo1 v]>?
switch costume to [hit v]
broadcast [hit v]
```
--- /hint ---
--- /hints ---

ستتلقى كل نسخ الكائن `Hippo` هذه الرسالة، لذا يمكنك الآن أن تأمرهم بالاختفاء عندما تصطدم سفينة الفضاء.

+ أضف هذه التعليمة البرمجية إلى الكائن `Hippo`:

```blocks
when I receive [hit v]
delete this clone
```

+ اختبر هذه التعليمة البرمجية ببدء لعبة جديدة وجعل السفينة تصطدم بفرس.

![screenshot](images/invaders-hippo-collide.png)

بعد اصطدام السفينة، تبدأ الأفراس في الظهور مرة أخرى في الوقت الذي لا تزال فيه السفينة متفجرة! لنعطِ فرصة للسفينة لتستعيد نفسها بعد الاصطدام.

+ أضف قالب `كرِّر باستمرار`{:class="blockcontrol"} بحيث يشمل التعليمة البرمجية ككل لكي تتكرر العملية، وقالب `انتظر`{:class="blockcontrol"} في النهاية لإضافة فترة إيقاف مؤقت قصيرة قبل أن تبدأ الأفراس في الظهور مرة أخرى.

```blocks
when flag clicked
forever
    switch costume to [normal v]
    wait until <touching [Hippo1 v]>?
    switch costume to [hit v]
    broadcast [hit v]
    wait (1) secs
end
```

--- challenge ---
### التحدي: المحاولات والنتيجة

في الوقت الحالي، لدى اللاعب عدد لانهائي من المحاولات. هل يمكنك إضافة `المستويات`{:class="blockdata"} أو `النتيجة`{:class="blockdata"} أو حتى `أعلى نتيجة`{:class="blockdata"} إلى لعبتك؟

[[[generic-scratch-high-score]]]
--- /challenge ---
