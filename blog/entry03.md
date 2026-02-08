# Entry 3
##### 2/2/26

### How have I been learning my tool? And what I plan on learning next?

During the break I was able to complete my goal for the most part. I didn't add the idea of using `readd()` to switch the characters, but I was able to add other stuff that made a count system for amount of coins collected and a system where it would make the coin disappear after collecting/touching the coin. what I did after was make a for loop that would spawn coins and then used `get()` to gather all the sprites with the coin tag in it.

```js
// Get all coins
const allCoins = get("coin");
const allCoinsText = add([
    text(`There are ` + allCoins.length + ` coins in the scene.`),
    pos(20,100),
    fixed(),
])
var totalCoins = 0;
const coinText = add([
    text("Coins: " + totalCoins),
    pos(20, 20),
    fixed(),
])
```

This made an easy way to keep track of how many coins were in the level and how many the player has collected. In this same mini game I was also able to apply `destory()` in the coins function. I basically made it so that when the player touched the coin/collided with the coin, it would disappear and increase the number on the counter of coins colllected.

This is my code:
```js
// Take the coin off of the screen if player touches it
player.onCollide("coin", (coin) => {
    destroy(coin);
    totalCoins++;
    coinText.text = "Coins: " + totalCoins;
});
```

My next goal in mind is to find a way to apple `readd()` into something as well as `follow()`. I want to keep the same idea with `readd()` about making it switch characters and for [`follow()`](https://kaboomjs.com/#follow) to make it like the player is saving someone. It'll have a ceratin button to save them and that way when they press it the person will follow the player to wherever. I want to learn some sort of [health system](https://kaboomjs.com/#health) to add enemies and things like that. This will become a key part to the game since I want to make it hard with lots of enemies and after each death they have to answer some question.

### Skills

Two skills I have improved on is **Problem decomposition** and **How to learn**. When wanting to learn these new components, I started off big and tried learning it all at once. This didn't work out well since I was trying to learn multiple components at the same time and couldn't wrap my head around everything at the same time. I deicided to break down all the components I want to learn over the course of the next few weeks. This makes my task easier as I don't have to worry so much about learning everything right now and having to learn it all at one time. This also improved how I should learn on my own, I normally just try to learn things all at once because I like multitasking. Though it becomes obvious that when learning too many things at the same time can be hard and is not ideal since I won't have a full understanding of everything. This is going to become important because I will be able to get a better understanding of the new code and even code I will write in the future.

### Engineering Design Process (EDP)

As said in previous blogs, I am still on step 2 and 3 because I'm still trying to figure out more about kaboom. I want to keep learning more components and things I can do in kaboom, before trying to do anything big. I need to learn components like I mentioned in my goal so that I can add it to the final product. I'm currently thinking of other things to add as I want to make the final game with multiple levels and other cool things. For now I just need to learn the most needed things then extras I might be able to add.

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
