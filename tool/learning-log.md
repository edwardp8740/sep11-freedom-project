# Tool Learning Log

## Tool: **Kaboom**

## Project: **To create a game to help study with AP Chem**

---

### 9/29/25:
* Today i'm learning about the basics of kaboom
    * Kaboom is a Javascript game programming library that helps you make games fast and fun.
        * It's known for it's easy to use API and composable component system. This makes it easy for starters to use
* Kaboom info/Basics
    * Make sure to use CDN and **NOT** NPM to install Kaboom
    * [File](kaboom-basics-1.html)
        * In this file I used all the code in the [Kaboom intro](https://kaboomjs.com/doc/intro) and learned some of the basics in kaboom.
        * All notes taken from kaboom code are in my [SEP-11 notes](https://docs.google.com/document/d/18-m2Xyw4GJjMvw5X4Om5a-GfJZ4sW0Rz5B4jdb_gCt4/edit?tab=t.0)
### 10/27/25:
* I decided to try and make a "game" with what I had learned on 9/29 just to see what I could do and have an idea of what I want to learn in the future
    * [File](test-game-1.html)
    * I learned how to make my player move left and right, though it's not smooth like I expected it to be
        * I did this by using functions to let the player be able to move a certain distance when the key is pressed
        * I plan on fixing this by learning how to make smooth movement with kaboom
    * I also learned how I could incorporate functions with kaboom already a little
* I plan on using a [video](https://www.youtube.com/watch?v=4OaHB0JbJDI) to help me learn more about the basics as well as help me recreate already made games to possibly us some of their code to put into my freedom project
### 11/10/25
* Today I will start watching the video and split it up into 4 parts: The Basics, Space Invaders game Mario game, and Zelda game.
    * I will start off from the basics and move in the listed order
BASICS: What is goes over (Refer back to notes to know the code) **NOTE: THIS VIDEO WAS RECORDED IN AN EARLIER VERSION OF KABOOM**
* Goes over how to add a sprite
* Goes over go to add a level

Extra notes:
* Usually just make a folder for every testing game since sprites take up a lot and will be easier to manage with a folder

Summary of everything covered in the video so far
* Due to video's version of Kaboom being out of date, it seems like functions don't work the same
    * This could be resolved by learning straight from the [kaboom page](https://kaboomjs.com/) instead of the video
* I think for now I will just start learning from the kaboom page so I know the code for the latest version of kaboom
    * When I think I have a good enough understanding of all the code on kaboom page I can refer back to the video to see if I can do it then but with the most recent version of kaboom

### 11/17/25

* Today I will be going back into the same [file](kaboom-basics-2/kaboom-basics-2.html) I was using to learn from the video since I still want to learn how to use `addLevel`
    * I figured out why my code wasn't working for `addLevel`, it turns out one of my sprites was named wrong so therefore wouldn't load in correctly and caused my whole code to not work.
    * I added the same features from my other code so the player can move around, in the same choppy way

### 12/8/25

* I tried learning about `c` but I couldn't really figure out what it was for
    * I plan on looking further into `get()` soon
* I also learned about `destory()`, from what I understand it's used as a way to destory/take away from the game when something touches it or anything like that
    * I plan on testing this along with `get()` so I get a good understanding of both of these things
* `readd()` seems to be a way to replace something almost like when you swap characters mid game but I'm not fully sure if I am correct
Future ideas:
* I plan on looking for some videos about `get()`, `destory()`, and `readd()`
    * After this I will test them out by creating something to understand how it works and what I can do with it for future ideas

### 1/9/26

* I found out what `get()`, `destory()` and `readd()` do
    * `get()`
        * It retrieves a list of all game objects currently in the scene that match a specified tag or tags
        * Example: it can be used in a way to tell the player how many things with that specfic tags there are
    * `destory()`
        * it basically just destorys the object and makes it disappear from the screen.
        * Example: it can be used in a way to collect coins
* Using my previous rough draft for a starting game, I tried adding these new things, I used `get()` to count the number of coins and telll the user how many coins there were in the game
* I used `destory()` as a form to show the user they have collected a coin, so that when they touch the coin it will add to the counter and then get rid of the coin.

### 3/2/26

* I learned about how the `health()` component 
    * `health()` works just was you expect it to, you set the number of health/lives the player starts with and you can also set the max health it has, like in minecraft where the max health is 10.
        * `.hurt()` takes away health from the player
        * `.heal()` heals the player/ adds more health to the player
*  I also learned about how the `lifespan()` component works
    * `lifespan()` first you set the timer/how long the thing lasts for and then you can also add an additional animation to the object
* I've made a new testing folder that will hold whatever I need to test certain things 
    * I'm testing how check points work since I want to make a system where it will give the player a new question after every check point, though It's still not decided if it will be like this or not.

### 3/16/26

* I'm going to make to be testing how player damages work and how I can also make ceratin things happen after some condition is met
    * I started with the normal setup and installing the health system
    * I made small ghost enemies to damage the player and added a death screen when the player dies
        * if the play dies then the player has an option to either restart the level completely or continue from last check point
    * I made a win screen too
        * after the player reaches the last checkpoint/flag the player will be shown a win screen congratulating them and they can restart the level again
* I want to be able to make traps/other obstacles to see how they work,
    * Using level devil as a reference for traps and what the goal is to make using this same test game.
* I also want to add other small things into the game so that it feels more like a game, for example like if the player falls off the screen, they die.

### 3/23/26

* I'm using my testing folder to see how to make traps and obstacles
    * I'm aimming to make traps similar to something like stuff you see in level devil
    * I did it in a way, it's not remotely as good but it does do the stuff I want it to, it's buggy and needs a lot of work
* I started by making the base of my main game in my testing folder to get a feel of how the game will play out.
    * The game is buggy and needs work but it is a good starting point for the game.
    * I need to make the game less buggy, fix certain problems, and find a better way for the game to play itself out
    * I figured out how to make the game progress from level to level 
        * I'm thinking about adding a main screen where the player can go back to preivous levels and stuff like that
    * I'm not sure how I will import the API just yet but I have a rough idea on how I can do it.

<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
