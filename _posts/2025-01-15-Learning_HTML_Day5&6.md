---
title: "Day 5-6 of Learning/Reviewing Website Building"
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
    - components is each piece in a user interface
        - similar to a Lego Block
## Day 6 - Videos 67-84
