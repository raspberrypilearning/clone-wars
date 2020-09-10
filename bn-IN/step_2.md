## একটি মহাকাশযান বানান

প্রথমে এমন একটি মহাকাশযান তৈরি করুন যা পৃথিবীকে রক্ষা করতে পারে!

\--- task \---

'Clone Wars' Scratch starter project টি খুলুন।.

**Online:** স্টার্টার প্রকল্পটি এখানে খুলুন [rpf.io/clone-wars-on](http://rpf.io/clone-wars-on){:target="_blank"}.

আপনার যদি scratch অ্যাকাউন্ট থাকে তবে **Remix** ক্লিক করে একটি অনুলিপি/copy তৈরি করতে পারেন।.

**Offline:** [ rpf.io/p/en/clone-wars-go ](http://rpf.io/p/en/clone-wars-go) থেকে স্টার্টার প্রকল্পটি ডাউনলোড করুন এবং তারপরে অফলাইন সম্পাদক/editor ব্যবহার করে এটি খুলুন।.

আপনার যদি scratch অফলাইন সম্পাদক/editor ডাউনলোড ও ইনস্টল করতে হয় তবে আপনি এটি [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"} এ খুঁজে পেতে পারেন.

\--- /task \---

![starter project](images/starter-project.png)

\--- task \---

এই কোডটি মহাকাশযান sprite এ যুক্ত করুন যাতে <kbd>left</kbd> কি চাপলে মহাকাশ যানটি বাম দিকে ঘুরে যায়:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    when flag clicked
    forever
        if <key (left arrow v) pressed?> then
            change x by (-4)
        end
    end
```

X-axis টি স্টেজের বাম দিক থেকে ডান দিকে যায়।. এর অর্থ হ'ল মহাকাশযান sprite র ` x ` অবস্থানের থেকে মানটি বিয়োগ করলে মহাকাশযান বাম দিকে চলে যায়।. সুতরাং এই কোড ব্লকটি এমন একটি অংশ যা আপনার মহাকাশযানকে বামে স্থানান্তরিত করে:

```blocks3
change x by (-4)
```

\--- /task \---

\--- task \---

`forever`{:class="block3control"} ব্লকে আরো কিছু কোড যুক্ত করুন যাতে আপনার মহাকাশযানটা ডান দিকে ঘরে যখন <kbd>right</kbd> arrow কী চাপা হয়.

\--- hints \---

\--- hint \---

মহাকাশযানের ` x ` অবস্থান থেকে ` 4 ` বিয়োগ করলে এটি বাম দিকে সরে যায়, সুতরাং আপনি কীভাবে তার পরিবর্তে ` 4 ` দ্বারা মহাকাশযানটি ডানদিকে সরাতে পারবেন?

\--- /hint \---

\--- hint \---

আপনার একই কোড ব্লক দরকার, তবে একটি ভিন্ন সংখ্যা সহ:

```blocks3
change x by ( )
```

\--- /hint \---

\--- hint \---

`forever`{:class="block3control"} ব্লকের মধ্যে অন্য কোড এর নিচে যে কোডটি যুক্ত করতে হবে সেটা এখানে দেয়া হল:

![rocket sprite](images/rocket-sprite.png)

```blocks3
if <key (right arrow v) pressed?> then
    change x by (4)
end
```

\--- /hint \---

\--- /hints \---

\--- /task \---

\--- task \---

সবুজ পতাকাটিতে ক্লিক করে প্রকল্পটি পরীক্ষা করুন। আপনার মহাকাশযানটি বাম এবং ডানে সরানোতে আপনি কি তীর কীগুলি/arrow keys চাপতে পারেন?

\--- /task \---