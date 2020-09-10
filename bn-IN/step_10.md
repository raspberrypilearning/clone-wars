## খেলা শেষ

এরপরে, আপনি খেলার শেষে একটি 'game over' বার্তা যুক্ত করতে যাচ্ছেন।.

\--- task \---

আপনি যদি ইতিমধ্যে `lives`{:class="block3variables"} নামের একটি নতুন variable না তৈরী থাকেন তবে তৈরি করুন.

আপনার মহাকাশযানটির তিনটি জীবন বা life দিয়ে শুরু হওয়া উচিত এবং যখনই এটিকে জলহস্তী বা hippo বা কমলালেবু বা orange ছুঁয়ে যায় তখন মহাকাশটি একটি জীবন বা life হাবাবে। আপনার গেমটি যখন `lives`{:class="block3variables"} শেষ হয়ে যাবে তখন থামা উচিত।.

\--- /task \---

\--- task \---

`Game Over` নামের নতুন sprite বানান **text** tool ব্যবহার করে.

![screenshot](images/invaders-game-over.png)

\--- /task \---

\--- task \---

মঞ্চে, খেলা শেষ হওয়ার ঠিক আগে `game over`{:class="block3events"} বার্তা সম্প্রচার করুন।.

![gameover sprite](images/stage-sprite.png)

```blocks3
broadcast (game over v) and wait
```

\--- /task \---

\--- task \---

আপনার `Game Over` sprite এ এই কোডটি যুক্ত করুন যাতে এটি খেলা শেষে প্রদর্শিত হয়:

![gameover sprite](images/gameover-sprite.png)

```blocks3
when flag clicked
hide

when I receive [game over v]
show
```

যেহেতু আপনি স্টেজের উপরে একটি `broadcast (game over) and wait`{:class="block3events"} ব্লক ব্যবহার করেছেন, `Game Over` sprite দেখানোর আগে স্টেজটি অপেক্ষা করবে।.

\--- /task \---

\--- task \---

আপনার খেলা পরীক্ষা করুন। আপনি কত পয়েন্ট স্কোর করতে পারেন? গেমটি যদি খুব সহজ বা খুব শক্ত হয় তবে আপনি কি এটির উন্নতি করতে পারেন?

\--- /task \---