# Entry 2
##### 12//15/25

### How have I been learning my tool? What is my FP goal over winter break?

Lately I've been trying to go down the list of components and game objects in the [kaboom website](https://kaboomjs.com/) to understand all the components I can use in the future. I learn about `addLevel()` and I think this was a great thing to learn in kaboom. `addLevel()` allows me to create a level/the layout of the map by setting sprites to symbols and using the symbols as a way to draw the map out.

Here's an [example of a level I made](../tool/kaboom-basics-2/kaboom-basics-2.html): 
```js
addLevel([ // map of the level
    "                           ",
    "                           ",
    "           $               ",
    "         =====             ",
    "                           ",
    "                           ",
    "===========================",
], {
    //define the size of tile block
    tileWidth: 100,
    tileHeight: 160,
    // define what each symbol means, by a function returning a component list (what will be passed to add())
    tiles: {
        "$": () => [ 
            sprite("player"),
            area(),
            scale(.1),
            body(),
        ],
        "=": () => [
            sprite("ground"),
            area(),
            scale(.20),
            body({ isStatic: true }),
        ],
    }
})
```

In this example I was able to define each symbol as a different sprite and ultimately create the layout of the game. This should allow me to create layouts much quicker and easier. I also looked over `get()`, `destory()`, and `readd()`, though I'm having a hard time trying to understand the purpose of `get()`. For the others I'm thinking about using `destory()` as a way to like collect coins like in Mario when you touch a good coin, it disappears and you gain a coin. I'm also thinking of using `readd()` as a way to switch from one character to another.

This leads me to my goal over the winter break, I plan on trying to make a mini version of a mario level. I want to use `addLevel()` to create the layout, `destory()` as a form of collecting coins and after a certain amount of coins are collected, you will gain something like a powerup or a life, and if I have time use `readd()` as a way to switch from one character to another. I'm hoping to add all these into the game as well as find out about more stuff so that I can add it to this mini project I'm making for myself.

### Skills

Two skills I improved on since the last blog is **Problem decomposition** and **Debugging**. while I was learning `addLevel()`, I came through a lot of problems since I didn't really understand how it worked. Though, instead of worrying about it I broke down each part to small sections just so that it would be easier to process then one big thing. As I referred back to a method my teacher taught me, by saying what's happening in the code out loud, because of this I was able to figure out what part of my code was messed up and fixed it. This should help me in the future since I'll be able to break stuff down into easier pieces and find bugs quicker.

### Engineering Design Process (EDP)

As of now I am still on step 2 and 3 because I'm still trying to figure out more about kaboom and with that then brainstorming more stuff I could do. I'm going to be in this small little cycle so that I can learn and improve with using kaboom. After this I plan on starying to make prototypes of the final product so that I have something to work off of and use.

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
