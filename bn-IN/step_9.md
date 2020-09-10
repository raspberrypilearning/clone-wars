## মহাকাশের বাদুড় বা bat

আপনার গেমটি কিছুটা শক্ত করতে আপনি এমন একটি বাদুড় বা bat তৈরি করুন যা মহাকাশযানের উপরে কমলালেবু ছুঁড়ে ফেলে।.

![a bat throwing an orange at the spaceship](images/bat-oranges.png)

--- task ---

একটি `Bat` sprite যুক্ত করুন এবং তার ঘূর্ণন এর দিকটা **left–right** করে দিন.

--- /task ---

--- task ---

`Bat` sprite কে `move`{:class="block3motion"} from left to right at the top of the Stage `forever`{:class="block3control"} করুন.

![a bat throwing an orange at the spaceship](images/bat-sprite.png)

```blocks3
when flag clicked
set size to (50) %
forever
    move (10) steps
    if on edge, bounce
end
```

আপনার কোড পরীক্ষা করতে মনে রাখবেন।.

--- /task ---

আপনি যদি বাদুড়ের dekhen দেখে থাকেন তবে দেখতে পাবেন এটির চারটি আলাদা costume রয়েছে:

![screenshot](images/invaders-bat-costume.png)

--- task ---

`next costume`{:class="block3looks"} ব্লক ব্যবহার করুন যাতে বাদুড়/bat টি সরার সময় তার ডানাগুলি নড়তে থাকে।.

--- hints ---


--- hint ---

বাদুড় চলে যাবার পর এটা `next costume`{:class="block3looks"} দেখাবে এবং তারপর স্বল্প সময়ের অপেক্ষা করবে `wait`{:class="block3control"}.

--- /hint ---

--- hint ---

আপনার কোডগুলিতে আপনাকে এই ব্লকগুলি যুক্ত করতে হবে:

```blocks3
wait (0.3) seconds

next costume
```

--- /hint ---

--- hint ---

আপনার কোডটি দেখতে এমন হওয়া উচিত:

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

এবার বাদুড় কমলালেবু ফেলতে থাকবে!

--- task ---

Scratch library থেকে `Orange` sprite যোগ করুন.

![screenshot](images/invaders-orange.png)

--- /task ---

--- task ---

Add code to your bat so that `when the flag is clicked`{:class="block3events"}, the `Bat` sprite `forever`{:class="block3control"} `waits`{:class="block3control"} for a `random`{:class="block3operators"} length of time between `5 to 10`{:class="block3operators"} seconds and then `creates a clone`{:class="block3control"} of the `Orange` sprite.

![bat sprite](images/bat-sprite.png)

```blocks3
when flag clicked
forever
    wait (pick random (5) to (10)) secs
    create clone of (Orange v)
end
```

--- /task ---

--- task ---

`Bat` sprite থেকে শুরু করে স্টেজের নীচের দিকে কমলালেবুর ক্লোন ফেলতে এর প্রতিটি ` orange ` এ কোড যুক্ত করুন।.

![orange sprite](images/orange-sprite.png)

```blocks3
    when flag clicked
    hide

    when I start as a clone
    go to (Bat v)
    show
    repeat until <touching (edge v)?
        change y by (-4)
    end
    delete this clone
```

--- /task ---

--- task ---

`Orange` sprite এ আরও কিছু কোড যুক্ত করুন যাতে কোনও `orange` ক্লোন যখন `spaceship` sprite কে আঘাত করে, ক্লোনটি প্লেয়ারকে পুনরায় সেট করার সুযোগ দিতে অদৃশ্য হয়ে যায়:

![orange sprite](images/orange-sprite.png)

```blocks3
    when I receive [hit v]
    delete this clone
```

--- /task ---

--- task ---

আপনার `spaceship` sprite র কোড সংশোধন করুন যাতে `hippo` sprite বা `orange` sprite স্পর্শ করলে sprite টি "hit" হয়:

![rocket sprite](images/rocket-sprite.png)

```blocks3
    wait until < <touching (Hippo1 v)?> or <touching (Orange v)?>>
```

--- /task ---

--- task ---

আপনার খেলা পরীক্ষা করুন।মহাকাশযানটা একটি পড়তে থাকা কমলা দ্বারা আঘাত প্রাপ্ত হলে কি হবে?

--- /task ---