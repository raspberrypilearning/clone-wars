## মহাকাশের জলহস্তী বা Hippos

এখন আপনি প্রচুর উড়ন্ত জলহস্তী বা hippo যুক্ত করতে যাচ্ছেন যেগুলি আপনার মহাকাশযানকে ধ্বংস করার চেষ্টা করবে।.

\--- task \---

Scratch library তে 'Hippo 1' চিত্র সহ একটি নতুন sprite তৈরি করুন।** shrink ** tool ব্যবহার করুন ` Hippo ` sprite কে ` Spaceship ` sprite এর সম আকারে তৈরি করতে।.

![The Scratch stage with a starry background. A rocket sits in the middle at the bottom of the stage and a hippo sprite with wings is at the top.](images/invaders-hippo.png)

\--- /task \---

\--- task \---

`Hippo` sprite র ঘূর্ণন শৈলীকে **left-right** এই ভাবে স্থির করুন।.

[[[generic-scratch3-sprite-rotation-style]]]

[[[generic-scratch3-sprite-rotation-style]]]

\--- task \---

যখন খেলা শুরু হয় তখন `Hippo` sprite লুকানোর জন্য কিছু কোড যুক্ত করুন।.

![hippo sprite](images/hippo-sprite.png)

```blocks3
when green flag clicked
hide
```

\--- /task \---

\--- task \---

প্রতি কয়েক সেকেন্ডে একটি নতুন `Hippo` ক্লোন তৈরি করতে স্টেজটিতে কিছু কোড যুক্ত করুন।.

\--- hints \---

\--- hint \---

When the `green flag is clicked`{:class="block3events"}, `repeatedly`{:class="block3control"} `wait`{:class="block3control"} `between 2 and 4 seconds`{:class="block3operators"} and then `create a clone of the Hippo sprite`{:class="block3control"}.

\--- /hint \---

\--- hint \---

আপনার যেগুলি ব্লকগুলি দরকার তা এখানে রয়েছে:

```blocks3
forever
end

create clone of (Hippo1 v)

(pick random (2) to (4))

when flag clicked

wait () secs
```

\--- /hint \---

\--- hint \---

আপনার কোডটি দেখতে এমন হওয়া উচিত:

![stage sprite](images/stage-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (2) to (4)) secs
    create clone of (Hippo1 v)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

প্রতিটি নতুন জলহস্তী বা hippo ক্লোন `x` অক্ষের এর যেকোনো স্থানে উপস্থিত হওয়া উচিত এবং প্রতিটি ক্লোনের গতি অনির্দিষ্ট হওয়া উচিত।.

\--- task \---

শুধুমাত্র `Hippo` sprite এর জন্য `speed`{:class="block3variables"} নামের নতুন variable তৈরী করুন.

[[[generic-scratch3-add-variable]]]

আপনি যখন এটি সঠিকভাবে করবেন, variable টির পাশে দেখবেন sprite র নাম রয়েছে, যা এই রকম দেখতে:

![The variable sprite that reads "Hippo1: speed 0"](images/invaders-var-test.png)

\--- /task \---

\--- task \---

প্রতিটি `hippo` ক্লোন শুরু হয়ে গেলে, যেকোনো গতিবেগ নিয়ে এগুলোকে বসান। তারপরে স্ক্রিনে ক্লোনটি দেখান।.

```blocks3
when I start as a clone
set [speed v] to (pick random (2) to (4))
go to x: (pick random (-220) to (220)) y: (150)
show
```

\--- /task \---

\--- task \---

আপনার কোড পরীক্ষা করুন। কয়েক সেকেন্ড পর পর কি একটি নতুন জলহস্তী বা hippo উপস্থিত হয়?

\--- /task \---

এই মুহুর্তে জলহস্তী বা hippo গুলো নড়াচড়া করে না।.

\--- task \---

প্রতিটি জলহস্তী বা hippo এলোমেলোভাবে ঘুরে বেড়াবে যতক্ষণ না এটি বজ্রপাতের কবলে না পড়ে। এটি করার জন্য, ইতিমধ্যে `hippo` sprite র কোড স্ক্রিপ্টে থাকা ব্লকগুলির নীচে এই কোডটি সংযুক্ত করুন:

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

আপনার কোডটি আবার পরীক্ষা করুন। প্রতি কয়েক সেকেন্ডে একটি নতুন hippo ক্লোন উপস্থিত হওয়া উচিত এবং প্রতিটি ক্লোন আলাদা গতিতে চলবে।.

\--- no-print \---

![Animation of the Hippo sprite flying around, two clones are created and move independently.](images/hippo-clones.gif)

\--- /no-print \---

\--- /task \---

\--- task \---

এখন মহাকাশযানের লেজার কামানটি পরীক্ষা করুন। যদি কোনও বজ্রাঘাত একটি জলহস্তী বা hippo কে আঘাত করে তবে জলহস্তী/hippoটি কী নষ্ট হচ্ছে?

\--- /task \---