---
title: "Day 5 & 6 of Learning/Reviewing Website Building SaaS"
date: 2025-1-15
categories: [blog]
tags: [Reviews, Website, Programming, HTML]
---
## Day 5 - Videos 51-66
- Git
    - Allows for the ability to switch between versions of code and rollback whenever needed easily
    - Commit is to add a comment to what is being pushed to the GitHub repository
    - git.ignore is to add files that should not be added to the Github repository
- NextJS Structure
    - `npm run dev` -> start a local development server
    - `page.js` builds the HTML pages
        - Pages are always titled `page.js`
        - New pages require a new folder in the app directory
    - **h1** tag -> header1
    - **div** tag -> adds text underneath the header tag
- Eslint
    - Developer dependency that can find and fix JavaScript code
    - Statically analyzes code to fix issues and problems
- Link
    - Allows the ability to travel between pages
    ```javascript
    <a href="/folder_name">Name</a>
    ```
    - Another way to do this is to add at the top of the `page.js` file add
    ```javascript
    import Link from "next/Link"
    ...
    <Link href="/folder_name">Name</Link>
    ```
- Layout
    - `layout.js` this file will be applied to all `page.js` underneath
        - The top of the file includes
    ```javascript
    import "./globals.css";
    ```
    - `global.cs` like its name implies injects all the CSS properties to each page
- React
    - JavaScript library used to speed up the process and provides reusability for User Interfaces
        - Including a button
        - Login button example
        ```javascript
        <button onClick={() => console.log("Logging in")}>Login</button>
        ```
    - `components` is each piece in a user interface
        - Similar to a Lego Block each component together creates the interface
        - Allows for the ability to customize these components and reuse them across all pages easily
        1. Inside the main repository create a new folder
        2. Name it whatever you choose a good name could be components
        3. Create a JavaScript file by naming something related and adding a .js at the end
        4. Add the functionality using functions, imports, etc
    - Two fundamental things in JavaScript
        - `return`(keyword) -> can be used in any function to break the execution of the code
            - Any code under the return keyword will become unreachable at least inside of the function or whatever it is encased in
        - `import`/`export`(statements) -> allows for separation of the code to separate files
            - To use code from a different file `import` is used
            - Then for the code to be available in `page.js` `export` is used
            - Example
        ```javascript
        import Link from "next/Link"
        ...
        export default Name
        ```
## Day 6 - Videos 67-79
- GSX
    - React components are functions that return GSX
    - Short for JavaScript XML
    - Similar to HTML what is needed is an opening tag and a closing tag
    - Ability to build dynamic user interface without overcomplicating things
    - Example
    ```javascript
    <ButtonLogin />
    {
        console.log("Hi");
    }
    ```
- Props
    - Every react components receives a parameter called props
    - It is empty at the start
- Comments
    - Comments start with `//` and like other typical code does not run
    - The typical thing to do is comment at the start of functions and some lines of code for more readability
- Destructuring
    - Shorthand syntax that unpacks values from arrays or properties from objects into more distinct variables
    - Makes code more readable and concise
    - Example 
    ```javascript
    const [var1, var2, var3] = object;
    ```
- JavaScript Functions
    - Example
    ```javascript
    const doThis = () => {
        // do something
    };
    or
    // looks similar to that of python in making a function
    function doThat() {
        // do something
    }
    ```
- Styling
    - Example
    ```javascript
    return (
        // Header1 in the font size of 48 pixels
        <h1 style={( fontSize: "48px" )}>
            Something
    );
    ```
- CSS Classes
    - Group of CSS properties that will be applied to any element
    - Instead of using style like the above classes can be used
- Tailwind CSS
    - CSS framework that is a large repository with predefined CSS classes
    - There is an extension for it in Visual Studios as well
        - Called Tailwind CSS IntelliSense
        - After hovering over any Tailwind classes it shows the exact CSS properties that are applied
        - It also shows all the potential classes that can be used
- Hero section
    - The first section that users
    - This includes a headline, some text, possibly a button to login, or logo
    - `<section>` tag can be used to easily seperate each section
- Rem
    - A unit of measurement that Tailwind uses
    - The default is 1 REM equals 16 pixels
