# Entry 4
##### 3/9/26

### How have I been learning my tool? And finished MVP of my project

Over the past month , I've been learning more about my tool, specifically stuff that will go into my MVP. For example, a big part that I've been learning with my partner was about how to implement the API my partner created into the kaboom game I created. We started testing a bunch of things such as different ways to run the code and what would be the best way for the user to study and have fun playing. 
```JS
async function getQuestion(unit) {
try {
    const res = await fetch(`http://localhost:4000/question/${unit}`);
    if (!res.ok) throw new Error("Bad response");
    return await res.json();
} catch (err) {
    console.error("FETCH ERROR:", err);
    return {
        question: "Failed to load question",
        choices: ["Retry"],
        answer: "Retry"
    };
}
}
scene("question", async ({ levelIndex }) => {
const data = await getQuestion(levelIndex + 1);
add([text("Unit " + (levelIndex + 1), { size: 28 }), pos(100, 40)]);
add([text(data.question, { size: 32 }), pos(100, 120)]);
data.choices.forEach((choice, i) => {
    add([
        text(choice),
        pos(120, 220 + i * 60),
        area(),
        "choice",
        { value: choice }
    ]);
});
onClick("choice", (c) => {
    if (c.value === data.answer) {
        go("game", { i: levelIndex + 1 });
    } else {
        go("game", { i: levelIndex });
    }
});
});
```

This is the code I wrote for the frontend/the game to get the question from the API. I used a function to first create a new screen for the user to see and I made another function that I would within the same one to get the question for the user, and then make everything show up on the screen. With this we were able to finish the full [MVP version](https://edwardp8740.github.io/Periodic-panic/) of the game, though it does not work on github pages just yet, we can get a working version of the game by running it using our IDE. For our beyond MVP we plan on looking into what we could do to make it work everywhere/on github pages as well.

### Skills

Two skills I’ve improved on are consideration and debugging. While working on the game and API, I had to do a lot of debugging to get everything working together. There were times where the questions wouldn’t load or the game wouldn’t switch scenes correctly, so I had to check my fetch function, make sure the API was running, and fix small mistakes in the code. I also had to test different parts of the kaboom game to make sure the answers worked and the player moved to the right level. This ultimately helped me get better at finding problems and fixing them step by step instead of getting stuck. For consideration, my partner and I have been thinking more about the user and what would make the game better to play. We’re trying to make it easy to understand, not too confusing, and still fun at the same time. We also thought about things like how the questions show up, how the player can answer them, and what happens after they get something right or wrong. This helped in realizing that I could add a lot of small fixes to make the game more enjoyable and maybe easier to play.

### Engineering Design Process (EDP)

So far I'm on steps 6-7. We're still testing the game for bugs and everything, and then planning beyond our MVP. What we already have planned is to figure out  how to make our game better and more accessable, (make the game playable on github pages), and adding more complicated questions to the API.

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
