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
This is the health system I learned

### Skills



### Engineering Design Process (EDP)

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
