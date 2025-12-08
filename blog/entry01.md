# Entry 1
##### 11/3/25

### What tool am I using and what am I making with it?

The tool that I am going to use is Kaboom to make a 2D platformer games for people to study AP chemistry with my partner. As someone who is taking AP Chem, studying is very, very important because learning everything only from classes can be very difficult and not enough time to let your brain process everything at your own pace. Now when I study, I find it very hard to look at a paper and just study, it becomes uninteresting and boring even after a little time. I find it much easier to study and entertain myself at the same time. This is where I got my idea of making a 2D platformer game to make studying interesting and productive.

So far using Kaboom, I have learned basic things to make something similar to the dinosaur game you get when you have no wifi. I learned this from the [Kaboom intruduction page](https://kaboomjs.com/doc/intro), it should me the basic is of things I might add to my chemistry game. Though, I didn't have the image they used for the game so I would have to add an different image so that the game will run normally,([game](../tool/kaboom-basics-1.html)). After learning all of this I made a new folder to tets out how to make characters move as well as just a testing ground to see what I might want to add to my game. I found out that even though I know how to make a character move, it doesn't move smoothly as it would in other games so I will learn on how to do that.

Here's the code for the choppy movement
```js
function moveLeft() {
    player.move(-MOVE_SPEED, 0); // Move left along the x-axis
    };
function moveRight() {
    player.move(MOVE_SPEED, 0); // Move left along the x-axis
    };
onKeyPress("a", moveLeft); // move left when user presses a
onKeyPress("d", moveRight); // move right when user presses d
```

It moves in a way that teleports to that spot instead of the accelerating and then staying at the max speed, this creates some sort of choppy movement instead of the regular smooth movement like normal games.
### Skills

A skill/skills I have improved on are **Collaboration**/**Communication**. I wanted to work with my partner because we had similar ideas for chemistry. It took a long while to talk about what we were going to make and how we would make it. Within this long talk it showed me how good long talks, even if boring, could be very good and useful in certain situations. If I didn't have that long talk with my partner, we wouldn't have found a way to work together and find a way to work together.

Another skill I've improved was **Creativity**. When talking to my friend about possible ways to work together and combine our tools, I had to really open my mind to stuff. I was able to think bac to previous games I've played like kahoot and blooket to help study and I remembered just how well it worked for me and my classmates. This showed me I can use already made things to help me come up with new stuff to make and get ideas.


### Engineering Design Process

I feel as though I am on step 2 moving to step 3 because I have already defined my problem and am researching with my tool to find ways to help resolve it. My next step is to brainstorm and continue to learn more about my tool because I still don't know all about my tool just yet. I will be on this step for awhile becausse I want to really get to know how to use my tool and make something great with it, so that future highschool kids can use it to study and do well on their exam.


[Next](entry02.md)

[Home](../README.md)
