Notes for a LinkedIn course: https://www.linkedin.com/learning/javascript-essential-training-3
<br>This will become an annotated README at the end of the course.


# JavaScript Essential Training Raw Notes

Introduction

- Webpages are made up of HTML, CSS, and JavaScript
  - HTML = Markdown, CSS= presentational enhancement, JavaScript interacts with HTML and CSS to provide dynamic layer
- Java vs. JavaScript
  - Not related
  - JavaScript was attempt to try to license a scripting language for Java
  - Java = solo application, JavaScript = interactive webpages
  - JavaScript
    - Conforms to ECMAScript (ES) standard
    - Web browsers can often take a while to adapt new technology
      - May need transpilers for webpages in updated JavaScript to run on outdated browsers
    - jQuery
      - Library of JavaScript Functions
      - main Library
    - JavaScript frameworks
      - AngularJS, React, etc.
      - Front end application frameworks to build Webpages
      - Make webpages faster (not in this course)
    - Node.js
      - Use JavaScript as server side language
      - run advanced operations

Basics
- Tools
  - No compilation
  - Runs within browsers
  - Code editor
    - standard or IDE (integrated code environment)
    - Use Atom in this course
  - Browser - any will do
    - develop in 1 browser, but test in all available
    - Use Chrome here
    - Also use Atom Live Server to streamline debugging process

- Browser Console
  - Chrome's dev tools and Console
  - Exercise file 02_02
    - index.html is blank in chrome
  - <b>Ctrl</b>+<b>Shift</b>+<b>I</b> opens dev Tools
  - Console (<b>Ctrl</b>+<b>Shift</b>+<b>J</b>) is CMD for browser for on the fly changes
    - Can type commands directly
      - alert("I love Ducks!") prints "I love Ducks!" or alert(5+13) prints 18


      ``` javascript
          var date = new Date()
          alert("Today is " + date)
      ```
      ```
      Today is: Thu Feb 13 2020 18:00:00 GMT-0600 (Central Standard Time)
      ```


        - Use <b>Shift</b>+<b>Enter</b> to move down a line
        - can use console.log() instead of alert() if you don't want it in a pop-up
  - Elements tab will show you HTML structure
    - Start with empty head and body
    - Change the body of the HTML in console (without saving it to html file)

        ```JavaScript
        document.body.innerHTML= "<h1>The date today is " + date + "</h1>"
        ```
        ```
        The date today is Thu Feb 13 2020 18:00:00 GMT-0600 (Central Standard Time)
        ```    

    - Make the date more readable by applying methods to the variable

        ```JavaScript
        document.body.innerHTML= "<h1>The date today is " + date.getMonth() + "/" + date.getDate() + "/" + date.getYear() + "</h1>"
        ```
        ```
        The date today is 2/13/20
        ```



    - JavaScript indexes start at zero!!

  - Get browser to run our JavaScript
    - Can add it to HTML itself or get the webpage to read a separate JavaScript File
    - 02_03\index.html --> Exercise_inline-JavaScript.html
      - JavaScript (<script></script>) can be placed in the:
        - head - run before contents are rendered
        - body - run with elements
        - after body - run after elements are rendered
      - Need to put ";" at end of each line
      - cannot use document.body.innerHTML in the head of the HTML document because it runs top to bottom and the body has not been rendered yet
        - causes render blocking
    - 02_04\index.html --> Exercise_External-JavaScript_file.html
      - Script starts off placed after end of body, ok for small scripts
      - external script is script.js
        - can be referenced in the <script> using: <script src= "script.js"></script>
      - cannot be placed in the head for same reason listed above
        - using "async" or "defer" attributes in the <script> tag can prevent render blocking


- Writing good JavaScript (things to remember)
  - Case sensitive
  - Use camelCase
    - variables start with LOWERCASE letter
    - Objects and Classes start with UPPERCASE
    - CONSTANTS are all caps
  - Whitespace is ignored but must be used to make code human readable
  - End each statement with a semicolon
    - only necessary in certain situations, but helps with human readability
  - Comment liberally (same syntax as C++)
    - "//" for single line
    - "/\* \*/" for multiline



Working with Data
  - Variables
    - name cannot start with number
    - var declaration isn't necessary, but you may run into scoping problems
    - Syntax:

    ``` javascript
    var variableName = assignedValue;


    var a, b, sum;
    a = 4;
    b = 5;
    sum = a+b;

    ```

  - Data Types (6)
      - Numeric = regular numbers and integers;
      - String = letters and symbols; can use \" \" or \' \'
      - Boolean = true/false; lowercase, no quotation marks
      - null = empty; lowercase, no quotation marks
      - Undefined = create variable but don't set it to anything
      - Symbol, not included here
    - use console.log(typeof variableName) to get the variable type
    -Exercise 03_02
      - open console

      ``` javascript

        > console.log(typeof negInteger)
        VM115:1 number
        undefined
        > console.log(typeof escQuote)
        VM167:1 string
        undefined
        > console.log(typeof theSunIsWarm)
        VM209:1 boolean
        undefined
        > console.log(typeof emptyInside)
        VM262:1 object
        undefined
        > console.log(typeof justAnotherVariable)
        VM310:1 undefined
        undefined

      ```
    - Operators
      - = is an assignment; == is equality;
      - +, -, *, / ; PEMDAS; pretty standard
      - += , -=, *= for shorthand
      - ++ adds 1, -- subtracts 1
        - placing operator AFTER variableName (ex. a++) changes variable assignment

    - Strings and numbers
      - adding numeric and string creates string


      ``` JavaScript
      var a, b, sum;
      a = 4;
      b = "5";
      sum = a+b;


      // in console
      > sum
      "45"
      ```
    - Conditionals
      - if/else
        - Syntax
        ``` javascript
        if (condition){
          Do something;
        }else{
          Do something else;
        }
        ```
      - equality
        - == can compare between datatypes; === is more strict
      - < , > , <= , >= , != , !==, and ! are all standard definitions
      - && is and; || is or
      - Ternary Operator (has 3 pieces)
        - condition ? true : false

      ``` javascript
      a==b ? console.log("Match"): console.log("No match"); //make sure to comment

      //is the same as

      if (a==b){
        console.log("Match");
      }else{
        console.log("No match");
      }
      ```

    - Arrays
      - stores several related items; can be different datatypes
      - starts at zero
      - syntax
      ``` javascript
      var pens = new Array("red", "green", "blue");

      //in console
      > pens[2]
      blue
      ```
      - Properties and methods
        - can be accessed using a "." after the variableName
        - properties are aspects of the object, methods are functions which can manipulate the variable
        - good examples are listed in exercise 03_08


Functions and Objects

JavaScript and the DOM, Part 1: Changing the DOM elements

Project: Creating an analog clock

JavaScript and the DOM, Part 2: Events

Project: Typing speed tester

Loops

Project: Automated Responsive Images Markup

Troubleshooting, Validating, and Minifying JavaScript

Bonus Chapter: Ask the instructor
