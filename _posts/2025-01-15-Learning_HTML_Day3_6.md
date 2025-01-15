---
title: "Day 3 & 4 of Learning/Reviewing Website Building"
date: 2025-1-15
categories: [blog]
tags: [Reviews, Website, Programming, HTML]
---
## Day 3 - Videos 29-40
- Interactions
    - The foundation of any web page is **HTML**
    - **JavaScript** is used to add interactively and functionality to a webpage
        - It is not required for a webpage to have a **JavaScript**
    - To execute **JavaScript** on **Visual Studios**
        1. Open the developer console
        2. Go to the console tab
    - To write **JavaScript** on a webpage
        - Add JavaScript at the end of the body tag 
            - using the tags `<script>` and `</script>`
- Variables
    - The constants use **const**
    - The variables use **let**
    - The console acts like the standard output in typical coding
        - To do the same thing as `print()`
        - Do `console.log(a_variable)`
- Types
    - **typeof** is the equivalent of **type** in python
        - returns the type of the variable or object
    - Since **let** can be used all types
    - Some of types are: 
        - string : textual data (string)
        - number : integers and floating point (int and floats)
        - bigint : large numbers (long)
        - boolean : true or false (boolean)
        - undefined : variable declared but not assigned a value
        - null : intentional absence of a value
        - symbol : unique identifier
        - object : collection of key-value pairs and other complex entities
        - array : used to store ordered lists
        - function : performs actions or calculations
- Functions
    - To start writing a function it is similar to typical coding
        1. start the function using **const**
        2. add variables using = (*a_variable*)
        3. then add =>
        4. use { at the start of the function and } to end the function
        5. end the function by adding a semicolon(;) at the end
        - Example of a button to that increments after a click
    ```javascript  
    const addLike = (incrementBy) => {  
        likesCounter += incrementBy;  
    };
    ```
- Comments
    - Start comments using **//**
    - Same as typical coding used for more readability
- Objects
    - Similar structure to a function
    1. Start by instantiating the const variable
    2. Add { to start and } to end
    3. Each line should have a comma at the end
    4. End the object by adding a semicolon(;) at the end
    - Example  
    const a_object {};
- Events
    - **addEventListener** to add an event listener
        - `addEventListener("a_variable", () => {});`
- Element Manupilulation
    - `innerText` can add text to objects like a button
    - Used in tandem with document.getElementByID
    - Example  
    `document.getElementByID(variable).innerText = "*text*";`
- Remove Redundancy
    - The biggest thing in any type of coding is to remove redundancy and improve readability
- Separation of Concerns
    - To separate the JavaScript from the HTML and CSS a file **index.js** can be used
    - To use this new JavaScript file
        1. Start writing inside `<script>`
        2. Add src="*the js file name*  
        Example 
         
        `<script src="*js file name*>`
- If else
    - Similar structure to typical coding languages like Python
    - `if (*variable*) {};
    - Each line ends with a semicolon
    - Use `alert()` to send a alert
    - For equivalent use triple `===` rather than double `==` like python

## Day 4 - Videos 41-50
- Textag
    - List of tools developers use to build software
- NodeJs
    - Application that allows JavaScript to be executed on a computer outside of a web browser
    - `https://nodejs.org/en`
- NextJs
    - The framework to structure HTML pages
    - Basically a large container for HTML pages
    - Allows for the ability to easily structure and style multiple pages
    - Command on MAC -> npx create-next-app@*version*
    - Command to run -> npm run dev
    - Url to access -> localhost:3000
- NPM
    - Similar to Docker but for JavaScript used to find open-source packages for JavaScript
    - Each package contains a simple installation command
        - `npm i a_name`
    - To use packages use the file that was created `package.json`
- Dependencies
    - Add dependencies to `package.json`
    - Add plugins to `package.json`
```javascript
plugins: {  
    require('plugin'),  
}
```
- Scripts
    - Script interacts with the entire project
    - Everything that is inside of the script object is executable
    - To run for example a dev script
        1. The first thing to do is to stop the actual script
        2. Use Ctrl C
        3. Type NPM run
