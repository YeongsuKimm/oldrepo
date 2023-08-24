---
layout: default
title: Student Blog
---


## Build you Home Page here 
This is about your journey. Start now!!!
Go to my [Github account](https://github.com/YeongsuKimm) !!
<br>

<!-- ## Overview of Hacks, Study and Tangibles
Blogging in GitHub pages is a way to learn and code at the same time. 

- Plans, Lists, [Scrum Boards](https://clickup.com/blog/scrum-board/) help you to track key events, show progress and record time.  Effort is a big part of your class grade.  Show plans and time spent!
- [Hacks(Todo)](https://levelup.gitconnected.com/six-ultimate-daily-hacks-for-every-programmer-60f5f10feae) enable you to stay in focus with key requirements of the class.  Each Hack will produce Tangibles.
- Tangibles or [Tangible Artifacts](https://en.wikipedia.org/wiki/Artifact_(software_development)) are things you accumulate as a learner and coder.  -->

<!-- ## MY PAGE -->



<h2>About Me:</h2>
<p style="float:right;clear:right;display:block;padding-right:200px"><img src="images/about-me.png" alt="about-me" style="width:220px;height:280px"></p>
<div style="padding-left:1em">    
    <ol style="font-size:15px">
        <li>I was born in South Korea</li>
        <br><br>
        <li>I have a dog <br><img src="images/dog.jpg" alt = "dog" style="width:70px;height:100px"> </li>
        <br><br><br>
        <li>I like music<br><h6>My favorite song</h6><iframe width="280" height="157" src="https://www.youtube.com/embed/HgzGwKwLmgM?si=LQo3eUvS2LYdTpc8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></li>
        <br>
        <li>I play the violin<h6>My favorite violin piece</h6><iframe width="280" height="157" src="https://www.youtube.com/embed/UFl9xuYP5T8?si=8upDj8Is4BhNkky7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></li>
        <br>
        <li>I enjoy coding<br><img src="images/code.jpg" alt="codeImage" width="280" height="157"></li>
    </ol>
</div>
<br><br><br>
<button class="todo_button" onclick="createItem()">Create a to-do item</button>
<h1>To-do List</h1>
<ol id="to-do">
    <li>Make to-do items permanent</li>
</ol>

<html>
    <head>
        <style>
            .todo_button {
                padding:9px 13px; 
                background-color:#af0011;
                transition-duration:0.4s;
                border-radius:8px;
            }
            .todo_button:hover {
                background-color:#de8e96;
            }
        </style>
    </head>
    <body>
        <script>
            function createItem()
            {
                var todo = document.createElement("li");
                var item = prompt("Enter to-do item");
                todo.innerHTML = item;
                console.log(todo);
                var location = document.getElementById("to-do");
                // todo.appendChild(document.createTextNode(item)); -- set item to todo
                location.appendChild(todo);
            }
        </script>
    </body>
</html>

<!-- 
<html>
<head>
</head>
<body>
    <h1>Simple Calculator</h1>
    <input type="text" id="display" disabled><br>
    <button onclick="appendToDisplay('7')">7</button>
    <button onclick="appendToDisplay('8')">8</button>
    <button onclick="appendToDisplay('9')">9</button>
    <button onclick="appendToDisplay('+')">+</button><br>
    <button onclick="appendToDisplay('4')">4</button>
    <button onclick="appendToDisplay('5')">5</button>
    <button onclick="appendToDisplay('6')">6</button>
    <button onclick="appendToDisplay('-')">-</button><br>
    <button onclick="appendToDisplay('1')">1</button>
    <button onclick="appendToDisplay('2')">2</button>
    <button onclick="appendToDisplay('3')">3</button>
    <button onclick="appendToDisplay('*')">*</button><br>
    <button onclick="appendToDisplay('0')">0</button>
    <button onclick="clearDisplay()">C</button>
    <button onclick="calculateResult()">=</button>
    <button onclick="appendToDisplay('/')">/</button><br>

    <script>
        function appendToDisplay(value) {
            document.getElementById("display").value += value;
        }

        function clearDisplay() {
            document.getElementById("display").value = "";
        }

        function calculateResult() {
            try {
                const expression = document.getElementById("display").value;
                const result = eval(expression);
                document.getElementById("display").value = result;
            } catch (error) {
                document.getElementById("display").value = "Error";
            }
        }
    </script>
</body>
</html>


<html>
<head>
</head>
<body>
    <h1>Word Guess Game</h1>
    <p>Guess the word one letter at a time.</p>
    <p>Guesses Left: <span id="guessesLeft">5</span></p>
    <p>Word: <span id="wordDisplay">_ _ _ _ _</span></p>
    <label for="guessInput">Enter a letter: </label>
    <input type="text" id="guessInput">
    <button onclick="checkGuess()">Guess</button>

    <script>
        // Define the word to be guessed
        const secretWord = "javascript";

        // Initialize variables
        let guessesLeft = 5;
        let wordDisplay = Array(secretWord.length).fill('_');
        let guessedLetters = [];

        // Function to update the word display
        function updateWordDisplay() {
            document.getElementById("wordDisplay").textContent = wordDisplay.join(' ');
        }

        // Function to check if a letter is in the word
        function checkGuess() {
            const guess = document.getElementById("guessInput").value.toLowerCase();
            
            if (guessedLetters.includes(guess)) {
                alert("You've already guessed that letter!");
                return;
            }
            
            guessedLetters.push(guess);
            
            if (secretWord.includes(guess)) {
                for (let i = 0; i < secretWord.length; i++) {
                    if (secretWord[i] === guess) {
                        wordDisplay[i] = guess;
                    }
                }
                updateWordDisplay();
            } else {
                guessesLeft--;
                document.getElementById("guessesLeft").textContent = guessesLeft;
                if (guessesLeft === 0) {
                    alert("Game over! The word was '" + secretWord + "'.");
                    location.reload(); // Reload the page to start a new game
                }
            }

            if (wordDisplay.join('') === secretWord) {
                alert("Congratulations! You've guessed the word: '" + secretWord + "'.");
                location.reload(); // Reload the page to start a new game
            }

            document.getElementById("guessInput").value = '';
        }

        // Initialize the word display
        updateWordDisplay();
    </script>
</body>
</html>
 -->
