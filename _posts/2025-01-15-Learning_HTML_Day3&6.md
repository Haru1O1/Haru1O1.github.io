---
title: "Day 3-4 of Learning/Reviewing Website Building"
date: 2025-1-15
categories: [blog]
tags: [Reviews, Website, Programming, HTML]
---
## Day 3 - Videos 29-40
- Interactions
    - Foundation of any web page is **HTML**
    - **JavaScript** is used to add interactively and functionality to a webpage
        - It is not required for a webpage to have a **JavaScript**
    - To execute **JavaScript** on **Visual Studios**
        1. Open the developer console
        2. Go to console tab
    - To write **JavaScript** on a webpage
        - Add JavaScript at the end of the body tag 
            - using the tags `<script>` and `</script>`
- Variables
    - the constants use **const**
    - the variables use **let**
    - the console acts like the standard output in typical coding
        - to basically do the samething as `print()`
        - do `console.log(a_variable)`
- Types
    - **typeof** is the equivalent of **type** in python
        - returns the type of the variable or object
    - since **let** can be used all types
    - some of types are: 
        - string : textual data (string)
        - number : integers and floating point (int and floats)
        - bigint : large numbers (long)
        - boolean : true or false (boolean)
        - undefined : variable declared but not assigned a value
        - null : intentional absense of a value
        - symbol : unique identifier
        - object : collection of key-value pair and other complex entities
        - array : used to store ordered lists
        - function : performs actions or calculations
- Functions
    - to start writing a function it is similar to typical coding
        1. start the function using **const**
        2. add variables using = (*a_variable*)
        3. then add =>
        4. use { at the start the function and } to end the function
        5. end the function by adding a semicolon(;) at the end
        - Example of a button to that increments after a click
    ```javascript  
    const addLike = (incrementBy) => {  
        likesCounter += incrementBy;  
    };
    ```
- Comments
    - start comments using **//**
    - same as typical coding used for more readability
- Objects
    - similar structure to a function
    1. start by instantiating const variable
    2. add { to start and } to end
    3. each line should have a comma at the end
    4. end the object by adding a semicolon(;) at the end
    - Example  
    const a_object {};
- Events
    - **addEventListener** to add a event listener
        - `addEventListener("a_variable", () => {});`
- Element Manupilulation
    - innerText can add text to objects like a button
    - used in tamdem with document.getElementByID
    - Example  
    `document.getElementByID(variable).innerText = "*text*";`
- Remove Redundancy
    - biggest thing in any type of coding is to remove redundancy and improve readability
- Seperation of Concerns
    - To seperate the JavaScript from the HTML and CSS a file **index.js** can be used
    - To use this new JavaScript file
        1. Start writing in inside `<script>`
        2. Add src="*the js file name*  
        Example 
         
        `<script src="*js file name*>`
- If else
    - similar structure
    - `if (*variable*) {};
    - each line ends with a semicolon
    - use `alert()` to send a alert
    - for equivalent use triple `===` rather than double `==` like python

## Day 4 - Videos 41-50
- Textag
    - list of tools developer use to build software
- NodeJs
    - application that allows JavaScript to be executed on a computer outside of a web browser
    - `https://nodejs.org/en`
- NextJs
    - framework to structure HTML pages
    - basically a large container for HTML pages
    - allows for the ability to easily structure and style multiple pages
    - Command on MAC -> npx create-next-app@*version*
    - command to run -> npm run dev
    - url to access -> localhost:3000
- NPM
    - Similar to Docker but for JavaScript use to find open source packages for JavaScript
    - Each package contains a simple installation command
        - `npm i a_name`
    - To use packages use the file that was created `package.json`
- Dependencies
    - add dependencies to `package.json`
    - add plugins to `package.json`
```javascript
plugins: {  
    require('plugin'),  
}
```
- Scripts
    - script interacts with the entire project
    - everything that is inside of the script object is executable
    - To run for example a dev script
        1. first thing to do is to stop the actual script
        2. use Ctrl C
        3. type NPM run