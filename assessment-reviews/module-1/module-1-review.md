# Module 1 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

## HTML

### Questions

1. What is HTML and what is it used for? 
   -HTML stands for hypertext markup language. It is a language to create web pages and web applications
2. What is the difference between an ID and a class?
   -Id's are unique: each element can only have one id. 
   -Classes are not unique. You can have as many as you want for an element. You can use multiple classes on the same element.
3. What does it mean to write "semantic" HTML?
   Using HTML markup reinforce the meaning of the information in webpages and web applications, not just definitng its presentation or look. Ex. h1, h2, p,

### Exercises

1. Write a paragraph tag with a class of "highlight" and content "Watch out!". 
<p class = "highlight">Watch out!</p>
2. Write an HTML image tag to show an image called `profile-picture.jpg`.
<img src = "profile-picture.jpg">
3. Write a link tag that links to http://google.com.
<a href="http://google.com"></a>
5. Write an complete standard HTML document outline (including a DOCTYPE, and `<html>`, `<head>`, and `<body>` tags).
<DOCTYPE! html></html>
<head>
<script type="text/javascript" src="main.js"></script>
<link rel="stylesheet" href="main.css">
</head>
<body></body>
6. Inside of the code for the previous exercise, write the appropriate tag to link to a script file called `main.js`.
7. Inside of the code for the previous exercise, write the appropriate tag to link to a stylesheet file called `main.css`.
8. Write a numbered list in HTML and list three of your favorite books.
<ol>
  <li>In Cold Blood</li>
  <li>Blood Meridian</li>
  <li>The Greatest Game Ever Played</li>
</ol>
9. Fix the indentation of the following HTML sample:

  ```html
  <div>
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ul>
  </div>
  ```

## CSS

### Questions

1. What is CSS and what is it used for? 
-Stands for cascading style sheets. It is code that changes the appearance of html.
2. What is the CSS box model?
-it is a way of thinking about designing content, which include the content itself, the padding that surrounds the content, the border, and the margin (which is outside of the box, between the box and another element.)
3. What's the difference between margin and padding? 
-margin is outside of the border, padding is inside, between the border and the content.

### Exercises

1. Write a CSS rule to make the text of all `h1` tags red. 

h1 {
   color: red;
   }
   

2. Write a CSS rule to make the background color of the link with `class="btn"` blue:

  ```html
  <a href="#" class="btn">Learn more</a>
  ```
  .btn {
      background-color: blue;
      }

3. Write a CSS rule to give the first paragraph in the following HTML a font size of `20px`, but not the second paragraph.

  ```html
  <header class="jumbotron">
    <p class="large-paragraph">Hello, World!</p>
  </header>

<p>Welcome to this awesome website!</p>
  ```
  
  .large-paragraph {
  font-size: 20px;
  }

## JavaScript

### Questions

1. What is a function? What are they used for?
-A function is a block of code designed to perform a task. They take data or variables in, perform a set of task(s) on them, and return the result.
2. What is the difference between `==` and `===`?
They are both operation operators. == checks the equality of two values. === checks the equality of two values as well as the equality of the two types of values.
3. What is the difference between global and local scope variables?
-global variables are defined outside of the function, and can be accessed on any function within the program. Local variables are defined within a function and are only accessed inside the function.
4. What is a boolean value?
-a boolean value represents one of two answers, true or false.
5. What is an array?
- an array is a list that stores multiple values in a single variable.

### Exercises

1. Write a line that declares a variable called `myName` and set its value to your name.
- var myName = "Gabe"
2. Write a loop that logs the numbers 1 through 10 to the console.
- for (var i = 1; i <= 10; i++) {
  console.log(i)
3. Translate the following pseudocode into JavaScript: if `score` is greater than `3` and `lives` is greater than `0`, alert "You win!".
- if (score > 3 && lives > 0) {
  alert("You win!")
}

4. Write a function `sayHello` that takes one argument, a name, and logs "Hello, <name>!" to the console. Then, call the function below the function definition and pass in your name as the argument.
- function helloName(name) {
  console.log("Hello " + name + "!");
}
helloName("Gabe");

5. What would the following script log to the console?

  ```javascript
  var currentSong = "Call Me Maybe";

  function setSong(song) {
    currentSong = song;
  }

  setSong("Friday, Friday");

  console.log(currentSong);
  ```
  
  - "Friday, Friday"

6. What would the following script log to the console?

  ```javascript
  var add = function(a, b) {
    return a + b;
  }

  var result = add(3, 7);

  console.log(result);
  ```
  
  - 10

7. What would the following script log to the console?

  ```javascript
  var helloGoodbye = function(name) {
    return sayHello(name) + " " + sayGoodbye(name);
  }

  var sayHello = function(name) {
    return "Hello " + name " !";
  }

  var sayGoodbye = function(name) {
    return "Goodbye " + name " !";
  }

  console.log(helloGoodbye("Sarah"));
  ```- Hello Sarah ! Goodbye Sarah !
        --That is what I thought it would do, but I tried it and it ran syntax error "unexpected string"


8. Write a function `findLongestWord()` that takes an array of words and returns the length of the longest one.
9. Define a function `sum()` that sums all the numbers in an array of numbers. For example, `sum([1,2,3,4])` should return 10.
10. Write a function that takes a character (i.e. a string of length 1) and returns true if it is a vowel, false otherwise.

function character(letter) {
  if (letter == "a" || letter == "A") {
  console.log("true");
  }
    else if (letter == "e" || letter == "E") {
      console.log("true");
    }
    else if (letter == "i" || letter == "I") {
      console.log("true");
    }
    else if (letter == "o" || letter == "O") {
      console.log("true");
    }
      else if (letter == "u" || letter == "U") {
      console.log("true")
        
      } else {
        console.log("false");
  }
}
 
  character("i");
  
  //I'm sure there is a more efficient way to do this. Possibly using an array? 


11. Write the correct line to make `"Woof!"` show up in the console based on this script:

  ```javascript
  var pet = {
    name: "Charles",
    goodDog: true,
    speak: function() {
      console.log("Woof!");
    }
  };
  ```
  - pet.speak

12. Using the same script as above, write the correct line to log the dog's name to the console.
- console.log(pet.name);

## Command Line

### Questions

1. What is the command line and what is it used for?
-It's a user interface that allows the user to interact with the computer through commands, written with successive lines of text (instead of using a mouse)
2. What does the command `ls` do? 
-it lists files with the current directory.
3. What does the command `pwd` do?
-stands for 'print working document', it outputs a full pathname of the current working directory.
4. What does the following command do: `cd my-cool-project`
-cd takes a directory name as an argument, and switches into that directory.

### Exercises

1. Write the command to make a new directory called "my-cool-project".
- mkdir my-cool-project
2. Write the command to create a file called "index.html".
- touch index.html
3. Write the command to delete a file called "main.css".
- rm main.css

## Git

### Questions

1. What is Git and what is it used for?
git is an open source version control system. It allows people to collaborate on the same project and save your history of changes.
2. What's the difference between a local repository and a remote repository?
a local repo is on your computer, remote is on a remote server.  

### Exercises

1. Write the command that you would use to create a new local Git repository.
- git init
2. Write the command to stage a file called `index.html` to be committed.
- git add index.html
3. Write the command to view the current status of the git repository.
- git status
