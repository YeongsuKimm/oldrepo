---
# layout: schedule
title: Computer Science and Software Engineering
units: "1,2,3,4,5,6"
course: Games & Projects
---
<h1>Week 0 Projects</h1>
<br><br><br>
<h1>Week 1 Projects</h1>
<h2>- The Notepad</h2>
<h3>On the home page</h3>
<br>
<html>
    <head>
        <style>
            .cal_button {
                background-color:#af0011;
                color: white;
                border-radius:8px;
                /* padding: 30px 30px; */
                transition-duration:0.4s;
                /* position:relative; */
                left:100px;
                font-size:30px;
                color:white;
                width:153px;
                height:100px;
            }
            .cal_button:hover {
                background-color:black;
            }
            #display {
                text-align:center;
                height:75px;
                width:630px;
                font-size:65px;
            }
        </style>
    </head>
    <body>
        <h2>- Simple Calculator</h2>
        <input type="text" id="display" disabled><br>
        <button onclick="appendToDisplay('7')" class="cal_button">7</button>
        <button onclick="appendToDisplay('8')" class="cal_button">8</button>
        <button onclick="appendToDisplay('9')" class="cal_button">9</button>
        <button onclick="appendToDisplay('+')" class="cal_button">+</button><br>
        <button onclick="appendToDisplay('4')" class="cal_button">4</button>
        <button onclick="appendToDisplay('5')" class="cal_button">5</button>
        <button onclick="appendToDisplay('6')" class="cal_button">6</button>
        <button onclick="appendToDisplay('-')" class="cal_button">-</button><br>
        <button onclick="appendToDisplay('1')" class="cal_button">1</button>
        <button onclick="appendToDisplay('2')" class="cal_button">2</button>
        <button onclick="appendToDisplay('3')" class="cal_button">3</button>
        <button onclick="appendToDisplay('*')" class="cal_button">*</button><br>
        <button onclick="appendToDisplay('0')" class="cal_button">0</button>
        <button onclick="clearDisplay()" class="cal_button">C</button>
        <button onclick="calculateResult()" class="cal_button">=</button>
        <button onclick="appendToDisplay('/')" class="cal_button">/</button><br>
        <script>
            function createItem()
            {
                var note = document.createElement("li");
                var item = prompt("Enter note item");
                note.innerHTML = item;
                console.log(note);
                var location = document.getElementById("note");
                // note.appendChild(document.createTextNode(item)); -- set item to note
                location.appendChild(note);
            }
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
