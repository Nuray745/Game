# 🍎 Sweet Catcher: Ready for a Sweet Adventure?

Welcome to the world of **Sweet Catcher**!

<p align="center">
  <img src="assets/game.png" alt="Game Flow" width="600">
</p>

## 🎮 The Magical World of the Game

At the heart of the game lies a very simple and fun mechanic:

* **Start Button:** Simply click the "Start" button to begin your adventure.
* **Falling Treasures:** Once the game starts, various items will begin to rain down from the sky every 800ms.
* **Basket's Mission:** Your main task is to guide the basket in the right direction and "catch" the falling items before they hit the ground.

## 🍭 What to Catch, What to Avoid?

Be careful with the items that will fall into your basket:

* **Sweets (Donut, Candy, Cupcake):** These are your best friends; each one earns you +10 points!
* **Chili Pepper:** Stay away from this mischievous item, as it deducts 15 points from your score.
* **Bomb:** Oh no, be careful! If you catch a bomb, you lose 1 life, and the screen will warn you (with a shake effect).

## 🛑 When Does the Game End?

Like all good things, you must be careful here too. The game ends in the following cases:
* Your lives run out (Lives <= 0)
* Your score runs out (Score <= 0)

When the game ends, the "Game Over" screen opens, where you can see your high score.

## 🛠️ Technical Details (What Happens in the Background?)

* **Persistence:** To keep the game interesting, your high scores are stored in `localStorage`.
* **Dynamic UI:** Your score and life count update in real-time on the screen within seconds.

---

Ready your basket and start gathering the highest score! Good luck! 🍭✨
