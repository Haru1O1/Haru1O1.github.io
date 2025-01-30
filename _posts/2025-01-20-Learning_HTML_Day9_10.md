---
title: "Day 9 & 10 of Learning/Reviewing Website Building & SaaS"
date: 2025-1-20
categories: [blog]
tags: [Reviews, Website, Programming, HTML]
---
## Day 9 - Videos 110-124
- API
    - The most common way users get information from a website is by the server itself returning an HTML page
    - However, since there are things other than an HTML page like images or links APIs are needed
    - An API is a generic word that describes a server that gives access to developers to perform actions
    - For example in building software and web apps API is typically used to communicate with the backend
    - Using the MongoDB package in an application is considered an API
    - In the past, a dedicated server is required to be created to make an API
    - Nowadays NextGS can easily be used to create the API 
        - Steps:
            1. Create a folder called API in the app folder
            2. Create another folder inside the API folder called auth
                - auth - authentication
            3. Create a file called route.js
                - This will become the endpoint for the API
            4. In this file 
            -   ```javascript
                export function GET() {
                    return Response.json({ message : "API has been hit" });
                }
                export function POST() {

                }
                ```
            5. To access this part on localhost add the folder API and auth to it -> /api/auth/
- Auth.js
    - Boilerplate code for user authentication
    - Installation
        1. Go to the terminal or the command line interface of the OS
        2. Type `nmp install next.auth@beta`
        3. Press enter it will now be installed in the dependency
- User Authentication
    - When a client visits a website and goes to the login page
    - The server sends back the sign-in.html page
    - This login page could have several different options to log in or sign up, whether using login credentials '(email or password)' or a third-party sign-in like Google or Facebook.
    - The latter uses a provider so if a client chooses to use the provider to sign in it sends a post request to the API and passes the parameters such as the provider and login creds
- Cookies
    - Small piece of data that is sent by the webservers
    - For example:
        - The API to an internet browser then stores this data on the computer or phone
    - Cookies are used universally throughout the internet
        - Can be used for tracking analytics, user preference, session tokens, etc ...
        - One example is using cookies to create a last-click attribution model where the cookie is used to identify the last person who interacted with a customer before they made a purchase
    - Two crucial parts are also required to use user authentication features
        - The first one is having a database to save the user and session data
        - The second is setting up the third-party provider login
- Emails
    - Two types of emails
        - Transactional
            - Sent based on interactions with a service or platform
            - Typically automated
            - Event-triggered emails
            - Examples:
                - Account-related
                - Order-related
                - User actions
        - Marketing
            - Promotional emails sent to a list of subscribers to drive engagement, sales, or awareness
            - Require user consent to opt-in - Examples:
                - Promotional offers
                - Newsletters
                - Referral programs
    - Setting up a service to send transactional emails
        - One provider is called Mailgun
            - A relatively popular email API service designed for sending, receiving, and tracking emails
            - Includes a free plan
        - It is usually the best choice to use a subdomain for the email source as it reduces the impact of damaged reputation if the system is attacked
- OAuth Login
    - Oauth.js has a ton of providers
        - Example:
            - Apple, Discord, Google, Github, Facebook, Emails, Etc ...
    - Usually one social provider and one email-based provider should be included on a website
    - Magic Links are usually used instead of email and passwords as passwords no matter how secure if leaked ruin the login process
        - This means that the website typically asks for an email address associated with the login
        - The server then checks to see if the email address has been used or is stored in the database
        - If it is then it sends a unique link to the email and after being clicked with allows the user to log in
    - This process of using magic links also simplifies the process of resetting passwords
    - Typically the go-to way to websites used to reset passwords
- OAuth Login (Google)
    1. Go to Google Cloud and create or log to a account
    2. Create a new project
    3. Go to API and Services
    4. Then to Credentials
    5. Configure a consent screen
        - Internal - only available to people within the organization
        - External - available to user with a Google account
- JavaScript AND & OR
    - Used to combine multiple expressions and return a boolean (true or false)
    - Logical AND (&&)
        - Returns the first false value or the last true value if all values are true
    -   ```javascript
        console.log(true && false); // false
        console.log(true && true);  // true
        console.log("Hello" && "World"); // "World" (both true)
        console.log(null && "Hi");  // null (null is false)
        ```
    - Logical OR (||)
        - Returns the first true value or the last false value if all values are false
    -   ```javascript
        console.log(true || false); // true
        console.log(false || false); // false
        console.log(null || "Hi");  // "Hi" (null is false)
        console.log("" || 0 || false || "FB"); // "FB" (as everything is false)
        ```
    - && has higher precedence than ||
    -   ```javascript
        /*
        Returns 10
        First Statement 5 && 10 -> (true && true) so last truth is 10
        Second Statement 0 || 10 -> (false || true) so first truth is 10
        */
        console.log(0 || (5 && 10));
        /*
        Returns Fallback
        First Statement null && "Hi" -> (false && true) so first false is null
        Second Statement null || "Fallback" -> (false || true) so first true is "Fallback"
        */
        console.log((null && "Hi") || "Fallback"); 
        ```
- JavaScript Promise
    - A value that may be available now, or in the future, or never
    - Used for asynchronous operations like fetching data, reading files, or making API calls
    - A Promise takes an executor function
        - resolve → Call when the operation is successful.
        - reject → Call when there is an error.
    -   ```javascript
        const myPromise = new Promise((resolve, reject) => {
            setTimeout(() => {
                let LoadData = true;  // Change to false to test rejection
                if (LoadData) {
                    resolve("Data is loaded!");  // Resolved
                } else {
                    reject("Error in loading data.");  // Rejected
                }
            }, 2000);
        });
        ```
- JavaScript Async & Await
    - Built-in keywords used for handling asynchronous code in a more readable manner compared to using Promise
    - Async Function
        - Keyword used to define a function that will always return a JavaScript Promise
        - Inside the function await keyword can be used
    -   ```javascript
        async function myAsyncFunction() {
            // Some asynchronous code will go here
        }
        ```
    - Await Keyword
        - Used inside an Async function to pause the execution of the function until a Javascript Promise resolves or rejects
        -   ```javascript
            async function fetchData() {
                const result = await myPromise;  // Waits until the promise resolves
                console.log(result);
            }
            ```
- JavaScript Try & Catch
    - Used for handling exceptions in JavaScript
    -   ```javascript
        try {
            // throws an error
            let result = faultyOperation(); 
        } catch (error) {
            // handle the error
            console.error("An error has occurred:", error);
        }
        ```
    - The try block contains the part of the code that might caused an error
    - The catch block contains the part of the code inside the try block that will only run if an error is found
    - The error parameter in the catch block refers to the specific error that was thrown
## Day 10 - Videos 125-139
