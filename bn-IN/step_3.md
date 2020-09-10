## বজ্রপাতের ঝলক

এখন আপনি মহাকাশযানটিকে বজ্রপাতের মতো আগুন জ্বালানোর ক্ষমতা দিচ্ছেন!

\--- task \---

Scratch library থেকে `Lightning` sprite যোগ করুন.

[[[generic-scratch3-sprite-from-library]]]

\--- /task \---

\--- task \---

গেমটি শুরু হওয়ার পরে ` Lightning ` Sprite টি লুকিয়ে রাখা উচিত যতক্ষণ না মহাকাশযানটি তার লেজার কামানগুলিতে আগুন দেয়।.

`Lightning` sprite এ এই কোড যুক্ত করুন:

![lightning sprite](images/lightning-sprite.png)

```blocks3
when green flag clicked
hide
```

\--- /task \---

এই মুহূর্তে, বিদ্যুতের ঝলকানি মহাকাশযানের তুলনায় সত্যিই বড়!

\--- task \---

নিচে কিছু কোড আছে যেগুলি ইতিমধ্যে `Lightning` sprite এ বর্তমান, আরো কিছু ব্লক যুক্ত করুন sprite টিকে ছোট করতে এবং এটিকে উল্টে দিতে।.

![lightning sprite](images/lightning-sprite.png)

```blocks3
set size to (25) %
point in direction (-90)
```

এবার এটাকে দেখে মনে হচ্ছে মহাকাশযানটি সূচালো বিন্দু থেকে আগুন ছুড়ছে।.

\--- /task \---

\--- task \---

`Spaceship` sprite এ কিছু নতুন কোড যুক্ত করুন বজ্রপাতের একটি ক্লোন তৈরী করার জন্য যখন <kbd>space</kbd> কী চাপা হয়।.

\--- hints \---

\--- hint \---

`When the green flag is clicked`{:class="block3events"}, keep checking `forever`{:class="block3control"} `if`{:class="block3control"} the `space key is pressed`{:class="block3sensing"}, and in that case `create a clone of the Lightning`{:class="block3control"} sprite.

\--- /hint \---

\--- hint \---

যে ব্লকগুলি দরকার তা এখানে রয়েছে:

```blocks3
if <> then
end

forever
end

create clone of (Lightning v)

<key (space v) pressed?>

when flag clicked
```

\--- /hint \---

\--- hint \---

নতুন কোডটি দেখতে এমন হওয়া উচিত:

![rocket sprite](images/rocket-sprite.png)

```blocks3
when flag clicked
forever
    if <key (space v) pressed?> then
        create clone of (Lightning v)
    end
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

যখনই গেম একটি ` Lightning ` sprite এর ক্লোন তৈরি করে, ক্লোনটিকে উপস্থিত হয়ে পর্যায়/stage এর শীর্ষে না পৌঁছানো পর্যন্ত উপরের দিকে ওঠা উচিত। তারপরে ক্লোনটি অদৃশ্য হয়ে যাবে।.

এই কোডটি যুক্ত করুন `Lightning` sprite এ, যাতে পর্যায়ের শেষ প্রান্ত স্পর্শ না করা পর্যন্ত এর ক্লোনগুলি উপরের দিকে চলতে থাকে এবং তারপরে সেগুলি মুছে যায়।.

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

<kbd>space</kbd> কী চেপে দেখুন বজ্রপাত সঠিক ভাবে কাজ করছে কিনা।.

\--- /task \---