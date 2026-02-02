# Entry 3
##### 2/2/26

### How have I been learning my tool? And what I plan on learning next?

During the break I was able to complete my goal for the most part. I didn't add the idea of using `readd()` to switch the characters, but I was able to add other stuff that made a count system for amount of coins collected and a system where it would make the coin disappear after collecting/touching the coin. what I did after was make a for loop that would spawn coins and then used `get()` to gather all the sprites with the tag coin in it.

```js
// Get all coins
                const allCoins = get("coin");
                const allCoinsText = add([
                    text(`There are ` + allCoins.length + ` coins in the scene.`),
                    pos(20,100),
                    fixed(),
                ])
```

### 


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
