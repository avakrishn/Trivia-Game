# Emoji Trivia Game: What’s the Movie?

## Table of Contents
* [About the Emoji Trivia Game](#about)
* [Technologies used](#tech)
* [Key Features](#features)
* [Play the Game!](#play)
    * [Instructions](#rules)

* [Demo](#Demo)

### **<a id="about"></a> About the Emoji Trivia Game**
An interactive and timed trivia app where users guess the movie based on the emojis displayed. The app features dynamically updated HTML and CSS powered by JavaScript code for the logic and jQuery to manipulate the HTML. 

### **<a id="tech"></a>Technologies used to build the app:**
* HTML5, CSS3, Javascript, jQuery

### **<a id="features"></a>Key Features:**
* The app uses an array of objects to store the trivia game questions, and each object is associated with question, answer choices, and correct answer properties.
    * An example of one object in the Javascript array called movies.: 
        ```
        var movies = [
            {
                id: 0,
                question: "&#x1F427;  &#x1F603; &#x1F463;",
                answers:{
                    a: "FINDING YOUR FEET",
                    b: "MARCH OF THE PENGUINS",
                    c: "HAPPY FEET",
                    d: "PENGUINS OF MADAGASCAR",
                },
                correct: "HAPPY FEET",
                letter: "c",
            }, ...]
        ```
    * Each object in the movies array has question and answer properties. 
    * jQuery was used to dynamically update the html for each question and answer set that is displayed. 
    * The value of the question property is a string of Unicode code point values that have been converted into HTML character escapes. When the html renders, the html character escapes will translate into specific emojis. 
        * How to convert a Unicode code point value into a HTML character escape:
            1. Find the Unicode code point value for the emoji you want to insert. [Here](http://unicode.org/emoji/charts/full-emoji-list.html) is a link to a list of the current emojis and their respective Unicode code point values.
                * For example, the Unicode code point value for 😀 (grinning face emoji) is `U+1F600`.
            2. Replace `U+` with `&#x`to get: `&#x1F600`
            3. Put `;` at the end: `&#x1F600;`
                * In HTML, when the starting contains `&#` and the ending contains `;` it denotes a special character. 
                * The `x` in the escape code indicates to the browser that whatever follows the `x` is hex code. Unicode point values are usually represented in hex code.   

* Each question is timed and is displayed one at a time. If the player answers the question or the time for that question runs out, then a new question is shown. 
    * The setInterval() method was invoked to create a timer for each question.
    * The setTimeout() method was invoked when displaying the next question after the user was told if they answered the question correctly or incorrectly. 

### **<a id="play"></a>Play Emoji Trivia Game: What’s the Movie?**:  https://avakrishn.github.io/Trivia-Game/

* **<a id="rules"></a>Instructions**

    * In this Trivia Game, you will need to choose the correct movie title that corresponds to a combination of emojis that are displayed.

    * You will only see one emoji question at a time and you will need to choose your answer before the question's timer runs out.

    * After you answer the question or the timer runs out, you will be shown the correct answer, and if applicable, the answer that you chose. After a few seconds the next emoji question will be displayed.

    * After you finish the trivia game you will see the number of questions you answered correctly, incorrectly, or left unanswered. 

    * You can then restart the game, which will be a new random set of emoji trivia questions for you to answer!

### **<a id="demo"></a>Demo Images**

    * **Game Start**:
    ![Game Start](https://raw.githubusercontent.com/avakrishn/Word-Guess-Game/master/assets/images/game-start.png)

    * **Win a Round**:
    ![Game Win](https://raw.githubusercontent.com/avakrishn/Word-Guess-Game/master/assets/images/game-win.png)

### **Future Code Development:**
* Source code will be developed over time to handle new features in the future.

### **Issues:**
* If you find an issue while using the app or have a request, <a href="https://github.com/avakrishn/Word-Guess-Game/issues" target="_blank">log the issue or request here</a>. These issues will be addressed in a future code update.
