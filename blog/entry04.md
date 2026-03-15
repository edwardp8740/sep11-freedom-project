# Entry 4
##### 3/9/26

### How have I been learning my tool? And how have I made progress towards my MVP?

Over the past month , I've been learning more about my tool, mostly stuff that will go into my MVP. For example, a big part that I learned was how to make a checkpoint in kaboom. I want to use checkpoints as a way to give the user the questions they need to answer, so every time they reach a check point they get a question  and have to answer it to progress in the level.

```JS
// Checkpoint object
const checkpoint = add([
    sprite("flag"),
    pos(600, 600), // position of where the check point is
    area(),
    scale(.2),
    "checkpoint",
])

player.onCollide("checkpoint", (cp) => { // when player touches the checkpoint set that as their new spawnpoint
    checkpointPos = cp.pos.clone()
    debug.log("Checkpoint saved!") // just to show the checkpoint worked
})
```

This is the code I wrote for my checkpoint. Using the `.onCollide`, I also want to be able to run the API my partner is making for me. In other words it will allow me to give the player the question when they touch the check point.

Another thing I learned about my tool was a health system that will also play a role in my MVP. I need a health system in my game so that every time the player dies they have to restart from the beginning/checkpoint, and because I learned how to make a health system I can also put in enemies and traps now that will make it difficult for the player to progress.

```JS
const player = add([ // health of the player
    health(3),
])

player.onCollide("bad", (bad) => { // when they touch something with the tag "bad", -1 health
    player.hurt(1)
    bad.hurt(1)
})

// triggers when hp reaches 0/ when player dies restart game
player.on("death", () => {
    destroy(player)
    go("lose")
})
```
This is the [health system](https://kaboomjs.com/#health) I learned. I will purposely make the game difficult so that I can use this health system to its fullest.

### Skills

Two skills I've improved on is **Problem decomposition** and **How to learn**. I'm still trying to break down everything I need for my mvp into even smaller pieces, because I've been realizing that I need to know a lot just to make a good decent game/level. I've broken down the main parts of the level into small pieces like the health system and checkpoints I mentioned earlier. It's easier to see it this way because I can see what parts are truly important and needed vs what would be nice to have but not needed. I've also been trying to see what is the most efficient way I learn. For example, I've been using the kaboom website instead of videos and I seem to learn it pretty easily beecause the code is really simplified and explained in [kaboom](https://kaboomjs.com/). I'm doing this so that I don't waste much of the time I could spend learning other stuff about kaboom.

### Engineering Design Process (EDP)

So far I'm going back and forth from steps 2-5. I'm still learning but learning for my MVP version of my game. Though I am trying to work on it with what I already know. As I learn new things, I try to see how I can use them in my MVP and what I could do with them along with everything I already know. I might be here for a bit but I will eventually move onto fully focusing on creating the MVP of my game.

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
