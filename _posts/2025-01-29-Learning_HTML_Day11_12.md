---
title: "Day 11 & 12 of Learning/Reviewing Website Building & SaaS"
date: 2025-1-29
categories: [blog]
tags: [Reviews, Website, Programming, HTML]
---
- Disclaimer
    - I will be not be explaining some of the videos on the speaker's specific implementations for his SaaS and only talking about the topics in the video generally

## Where I Have Been
- I have been sick for past week and largely took a break and only did a few videos
- Practically lied on my bed for most of the time due to having the urge to cough or sneeze as soon as I stop being warm either from getting out my blankets or taking of my jacket if I left the room
- The time periods I felt it the most was morning and night as headaches
- Currently I have largely recovered only having to blow my nose occasionally due to a runny nose

## Day 11 - Videos 140-154
- React Controlled Forms
    - Forms where the elements (i.e. input fields, checkboxes, text areas) are controlled by React 
    - Form inputs are always synced with the component’s state
        - Easier to handle form validation, data submission, and user interactions
    - Controlled Components
        - React manages the state of the input value
- API call
    - The connection from the front end to the back end
- Axios
    - A popular JavaScript library used to make HTTP requests in both browser and Node.js
    - Command
    - `npm install axios`
    -   ```javascript
        try {
            const data = await axios.post("/api/board", { name });
            ...
        }
        ```
- React Hot Toast
    - Lightweight, customizable, and accessible toast notification library for React
    - Displays notifications with ease
    - `npm install react-hot-toast`
    -   ```javascript
        import toast from "react-hot-toast";
        ...
        try {
            const data = await axios.post("/api/board", {});

            setName("");

            toast.success("Board created!");
            ...
        } catch (error) {
            toast.error("Something went wrong");
        }
        ```
- Optional Chaining
    - `?.`
    - Safe access to nested properties without causing an error if a property is null or undefined
    - Prevents the need for repetitive checks
    - Also avoids the "Cannot read properties of undefined" error
    - Example:
    -   ```javascript
        /*
        If obj exists -> returns obj.property
        If obj is null or undefined -> returns undefined instead of throwing an error
        */
        const value = obj?.property;
        ```
- Eslint Rules
    - Popular tool for in automating coding standards and locating bugs or erros in JavaScript 
    - Rules that maintain clean, consistent, and error-free code
    -   ```
        // Install ESLint globally
        npm install -g eslint
        // Initialize ESLint
        npx eslint --init
        ```
    - Common Code Style Rules
        - quotes
            - Enforce single or double quotes	
            - Example:
                - "error": ["single"]
        - semi 
            - Require or disallow semicolons
            - Example:
                - "error": ["always"]
        - indent	
            - Enforce indentation (spaces/tabs)	
            - Example:
                - "error": [2, "tab"]
        - max-len
            - Set maximum line length
                - Example:
                    - "error": [80]

## Day 12 - Videos 155-169
- Pricing
    - `Pricing is marketing`
    - Along with the headline impacts the conversion rate the most
    - Free Plans
        - For a solo entrepreneur a free plan is a bad idea as in general only around 3% of free users will upgrade to paid versions
        - Without millions of dollars in marketing it is extremely difficult in building a large enough user base with premium users to support the costs
    - Free Trials
        - For free trials unless the product is a competitor of another tool that already includes a free trial it is usally a bad idea to implement this
        - Harder to find constructive and useful feedback or criticism
    - Alternatives
        - Demo
            - A way for users to test the product along with a video that shows the individual showing off the software
        - Free Credits
            - A type of plan that can be seem in AI image generation where a user is given a few credits which allow them to use the tool for a few uses before displaying the paywall
        - Subscriptions
            - Extremely popular method to use by sellers as most individuals forget about the recurring charge
                - So much so there are numerous of tools and apps that are made to specifically target unused recurring subscriptions
        - One-Time Payments
            - Easier to sell
            - Lose money in the long term as one-time payments usally come with free upgrades or updates so even if there are more mechanisms it typically is free to the users
            - Can always switch to a subscription later on
    - The most common problem with pricing is deciding whether it is just right not too high or too low
    - In the beginning where only a couple of few visiters will notice the website if the price is low it seems to the customers as cheap
    - A common way to determine how to price is by identifying what the competitors are doing
- Payment Processing Solution
    - Companies like Stripe, Lemonsquizy, Paddle, PayPal, etc...
    - Cards like Visa, MasterCard, AMIX, etc...
- Lemon Squeezy
    - Simple Checkout & Subscription Platform for Digital Products
    - Digital products, subscriptions, and SaaS services 
        - Built-in payment processing, tax compliance, and automation