---
title: "Day 5 & 6 of Learning/Reviewing Website Building"
date: 2025-1-15
categories: [blog]
tags: [Reviews, Website, Programming, HTML]
---
## Day 5 - Videos 51-66
- Git
    - allows for the ability to easily switch between versions of code and rollback whenever needed
    - commit is to add a comment to what is being pushed to the github repository
    - git.ignore is to add files that should not be added to the Github repository
- NextJS Structure
    - `npm run dev` -> start a local development server
    - `page.js` builds the html pages
        - pages are always titled `page.js`
        - new pages requires a new folder in the app directory
    - **h1** tag -> header1
    - **div** tag -> adds text underneath the header tag
- Eslint
    - developer dependency that can find and fix JavaScript code
    - statically analyzes code to fix issues and problems
- Link
    - allows the ability to travel between pages
    ```javascript
    <a href="/folder_name">Name</a>
    ```
    - another way to do this is at the top of the `page.js` file add
    ```javascript
    import Link from "next/Link"
    ...
    <Link href="/folder_name">Name</Link>
    ```
- Layout
    - `layout.js` this file will be applied to all `page.js` underneath
        - top of the file includes
    ```javascript
    import "./globals.css";
    ```
    - `global.cs` like its name implies injects all the CSS properties to each page
- React
    - JavaScript library used to speed up the process and provides reusability for User Interfaces
        - including a button
        - Login button example
        ```javascript
        <button onClick={() => console.log("Logging in")}>Login</button>
        ```
    - `components` is each piece in a user interface
        - similar to a Lego Block each component together creates the interface
        - allows for the ability to easily customize these components and reuse them across all pages
        1. inside the main repository create a new folder
        2. name it whatever you choose a good name could be components
        3. create a JavaScript file by naming something related and adding a .js at the end
        4. add the functionality using functions, imports, etc
    - Two fundamental things in JavaScript
        - `return`(keyword) -> can be used in any function to breaks the execution of the code
            - any code under the return keyword will become unreachable at least inside of the function or whatever it is encased in
        - `import`/`export`(statements) -> allows for seperation of the code to seperate files
            - to use code from a different file `import` is used
            - then for the code to available in `page.js` `export` is used
            - Example
        ```javascript
        import Link from "next/Link"
        ...
        export default Name
        ```
## Day 6 - Videos 67-84
- GSX
    - React components are functions that return GSX