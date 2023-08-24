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
<h1>Hello, Welcome to my page!</h1>


<h2 style="padding-left:2em">About Me:</h2>
<p style="float:right;clear:right;display:block;padding-right:150px"><img src="images/about-me.png" alt="about-me" style="width:200px;height:250px"></p>
<div style="padding-left:4em">    
    <ol style="font-size:15px">
        <li>I was born in South Korea</li>
        <br><br>
        <li>I have a dog <br><img src="images/dog.jpg" alt = "dog" style="width:70px;height:100px"> </li>
        <br><br><br>
        <li>I like music<br><h6>My favorite song</h6><iframe width="280" height="157" src="https://www.youtube.com/embed/ApXoWvfEYVU?si=ihJEORpFZOx7Ik2k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></li>
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


