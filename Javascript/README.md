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
  - RightClick = X or Ctrl+Shift+I opens dev Tools
  - Console (Ctrl+SHift+J) is CMD for browser for on the fly changes
    - Can type commands directly
      - alert("I love Ducks!") prints "I love Ducks!" or alert(5+13) prints 18

      ``` javascript
          var date = new Date()
          alert("Today is " + date)
      ```
          - Use Shift+Enter to move down a line
          - can use console.log() instead of alert() if you don't want it in a pop-up
  - Elements tab will show you HTML structure
    - Start with empty head and body
    - Change the body of the HTML in console (without saving it to html file)
    
        ```JavaScript
        document.body.innerHTML= "<h1>The date today is " + date + "</h1>"
        ```
    - Make the date more readable by applying methods to the variable
        document.body.innerHTML= "<h1>The date today is " + date.getMonth() + "/" + date.getDate() + "/" + date.getYear() + "</h1>"
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
    -
  - Data Types

Functions and Objects

JavaScript and the DOM, Part 1: Changing the DOM elements

Project: Creating an analog clock

JavaScript and the DOM, Part 2: Events

Project: Typing speed tester

Loops

Project: Automated Responsive Images Markup

Troubleshooting, Validating, and Minifying JavaScript

Bonus Chapter: Ask the instructor
