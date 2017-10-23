# Module 2 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

*Note: any topics from the first assessment should be reviewed in addition to the questions below!*

## CSS

### Questions

1. What is the box model?
  -The CSS box model is a design/layout concept. All html elements can be considered a box. When styling HTML, the box model is what informs the layout decisions of content. It consists of:
    1. content: the html element
    2. padding: the space between the content and the border
    3. border: the outer edge of the content and padding
    4. margin: the space between the border and the next element
2. What is the difference between block and inline elements?
  -HTML block elements are by default stacked vertically, on separate lines. 
  -Inline elements are on the same horizontal line, for example, the navigation.
3. What is responsive design?
  -
4. Which selector is more specific, a tag selector or class selector?
5. What does `box-sizing` do?
6. What's the difference between `relative` and `absolute` positioning?

### Exercises

1. Write a CSS rule to turn the background color of the link with the `.btn` class blue on hover:

  ```html
  <a href="#" class="btn">Learn more</a>
  ```

2. Write a CSS rule to give the `.container` a maximum width of `980px` when the browser window is wider than `1200px`:

  ```html
  <div class="container">
    <h1>I'm a heading!</h1>
  </div>
  ```

3. Which text would be red in the following example?

  ```html
  <style>
    section p:last-child {
      color: red;
    }
  </style>

  <section>
    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p>
  </section>
  <section>
    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p>
  </section>
  ```

4. Open this [JSBin](http://jsbin.com/qigiwuhepe/1/edit?html,css,output). Write a CSS rule using floats to make the HTML sample into a four column layout. Paste your udpated link below.

## JavaScript

### Questions

1. What is a callback?

### Exercises

1. Write a function `filterLongWords()` that takes an array of words and an integer `num` and returns the array of words that are longer than `num`.

````function filterLongestWords(words, num) {
  // 1. filter through the array
  var longerThanNumArr = [];
  for(var i = 0; i<words.length; i++) {
    if(words[i].length > num) {
      longerThanNumArr.push(words[i])
    }  
  }
}
filterLongestWords(["golden", "chihuaha", "labrador", "mut", "sheperd"], 1)
````
    
2. Write a function `charFreq()` that takes a string and builds a frequency listing of the characters contained in it. Represent the frequency listing as a Javascript object. Try it with something like `charFreq("abbabcbdbabdbdbabababcbcbab")`.

````function charFreq(str) {
  var freqObj = {};
  for(var i = 0; i<str.length; i++) {
    if (!freqObj[str[i]]) {
      freqObj[str[i]] = 1;
    } else {
      freqObj[str[i]] += 1;
    }
  }
  console.log(freqObj);
}
charFreq("abcdefg");
````

## DOM Scripting

### Questions

1. What does DOM stand for and what is it?
  DOM stands for document object model. When a web browser loads a web page, it creats a document object model, which treats all html and css as an object represented as a tree. the dom allows JavaScript to dynamically access and update the content, structure, and style of a document.

### Exercises

1. Write a JavaScript statement that finds the element with the ID, `next`, and saves it to a variable called `nextButton`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  ```
  ````var nextButton = document.getElementById("next");
  ````

2. Write another line that updates the text of `nextButton` to `"Next image"`.

  ````nextButton.innerHTML = "Next image";
  ````

3. Write another line that adds a click event listener to `nextButton` so that when it's clicked the browser alerts `"Next image coming up."`.

````nextButton.addEventListener(click, function () { 
  alert("Next image coming up"); 
  });
  ````

## jQuery

### Questions

1. What is a JavaScript library and why do we use them?
  -A JavaScript library is a library of pre-written JavaScript which allows for easier development of JavaScript-based     applications. It can simplify common tasks and reduce the amount of code that the developer has to write.
2. What is jQuery for?
  -jQuery is the most popular JavaScript library used today.
### Exercises

1. Write a statement to select all elements with the `.btn` class using a jQuery selector and save them to a variable called `buttons`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  <a href="#" id="beginning" class="btn">Beginning</a>
  <a href="#" id="previous" class="btn">Previous</a>
  ```
  ````var $buttons = $(".btn)";
  ````
  
2. Write another line that adds a click event to the buttons that logs `'click'` to the console when the button is clicked. Use the jQuery syntax.

  ````$(buttons).click(function () {
  console.log("click"); 
  });
  ````
  
## Angular

### Questions

1. How is a framework different than a library?
2. What is a controller?
3. What is a view?
4. What is a single page application?
5. What is a directive in Angular?

## Git

### Exercises

1. Write a command to create a new branch called `bug-fix`.
2. If you're on the `master` branch, write a command to merge a branch called `bug-fix` into the `master` branch.
