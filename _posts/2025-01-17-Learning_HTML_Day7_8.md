---
title: "Day 7 & 8 of Learning/Reviewing Website Building & SaaS"
date: 2025-1-17
categories: [blog]
tags: [Reviews, Website, Programming, HTML]
---
## Day 7 - Videos 80-94
- Config.JS
    - tailwind.css looks at all the class names and generates a CSS file with all the classes required
    - This file contains the ability to customize anything
    - `module.export`
        - Similar to export default
    - Daisyui-Components
        - Website -> daisyui.com
        - Tailwind-Based – Works as a Tailwind CSS plugin, extending its utility-first approach
        - Theming – Built-in themes allowing easy customization of styles.
        - Pre-Styled Components – Including buttons, cards, modals, alerts, forms, etc
        - Accessibility Focused – Follow best practices for accessibility
        - Lightweight & Customizable
- Media Query
    - Has the functionality to set different CSS properties based on the media aka the device being used
            - Mobile, Desktop, Etc
- SVG
    - Scalable Vector Graphics
    - Able to be scaled to any size without the loss of quality
    - Quicker loading times due to the code of the SVG being on the webpage
    - https://heroicons.com/
        - Has a library of usable icons in two formats
            - SVG & JSX
- JavaScript Ternary Operator
    - Javascript conditional operator
    - A way to simplify the if and else statements
    - Example
    -   ```javascript
        const age = 19;
        let canVote;

        if (age >= 18) {
            canVote = "Yes";
        }
        else {
            canVote = "No";
        }
        // to
        canVote = age >= 18 ? "Yes" : "No";
        ```
- ESLint
    - Extension for VS Code
        - Can locate formatting issues and semantic errors and automatically fix them
- Template Literals
    - Allows for easier string interpolation and multi-line strings
    - Example
    -   ```javascript
        const name = "aName";
        isLoggedIn = "True";

        // Normal Greetings
        const greetings1 = "Hello" + name;
        // Greet with the name
        const greetings2 = `Hello ${name}`;
        // If logged on greet with name else say Hello there
        const greetings3 = `Hello ${isLoggedIn ? name : "there"}`;
        ```
- Arrays(JavaScript)
    - Type of data structure
        - can hold more than one value
    - Index starts at zero
    - To use an array use the brackets symbol
        - Example -> `const fruits = ["🍉", "🍓", "🍎"]`
    - Map
        - Goes through each element and makes a new array by implementing a function with it
        - For example
        -   ```javascript
            const HiFruits = fruits.map((fruit) => {
                return `Hi ${fruit}`;
            });
            ```
    - Filter
        - Goes through each element in the array and runs a function
        - For example
        -   ```javascript
            const missingApple = fruits.filter((fruit) => {
                return fruit !== "🍎";
            });
            ```
- React Hooks
    - Functions that use state and lifecycle features in functional components
    - Use state hooks when updated changes the entire appearance of the page
    - Example
    -   ```javascript
        import { useState } from "react";

        function Counter() {
            const [count, setCount] = useState(0);

            return (
                <div>
                    <p>Count: {count}</p>
                    <button onClick={() => setCount(count + 1)}>Increment</button>
                </div>
            );
        }
        ```

## Day 8 - Videos 95-109
- React Server vs React Client Components
    - Components are labeled as a **server** or **client** depending on how its rendered
    - An internet browser has no idea that React's JS or any other library is in use
        - It does not understand the code
        - So React needs to take the code and transform it into something the browser can understand
            - This is known as the rendering process
                - If the rendering is done on the server it is a **Server Component**
                - If the rendering is done on the browser it is a **Client Component**
    - **Server Component**
        - By default, all React components are labeled as **Server Component**
        - `How It Works`
            - When a client visits a website the server checks the React JS code and turns it into a HTML page
            - That page is then sent back to the browser who then shows it to the client
        - `Major Advantages`
            - The code is mostly private and unknown to the users/clients
            - Data that is transmitted across the internet is minimal -> only what the client/user needs to see
            - Reduces the size of the HTML page which makes it run faster
        - `Caveat`
            - React.js features or client components are needed to listen to  events for some elements
    - **Client Component**
        - The server does not compile all the code but rather it sends back an empty skeleton with some guidelines for how to transform it into a valid HTML
        - The client will receive a big JavaScript page and then React will compile the code inside the browser
        - All the client components are transformed into clients.html
        - Unlike server components, these features are visible to the clients 
        - `Major Advantages`
            - User interactivity -> listen for click events or React hooks
            - Allows access to browser features such as storage or alerts
        - To label the component as a client
            - Type on the top of the js file `"use client";`
    - 
- Creating a FAQ Section
    - List of questions and answers
    - When a user clicks on a question the answer should be displayed
    - PsuedoCode
        - First, a use state react hook is required to keep track of whether the question was clicked and when it is unclicked (true to false)
        - Next, a conditional rendering is needed as if it is open then show the answer else show nothing
        - For each question and answer it should return the client component
- Anchor Links
    - Allow for the ability to move to different sections on the page
    - Example 
    -   ```javascript
        <a href="#section1">Go to Section 1</a>
        <a href="#section2">Go to Section 2</a>

        <section id="section1">
            <h2>Section 1</h2>
            p>This is Section 1 content.</p>
        </section>

        <section id="section2">
            <h2>Section 2</h2>
            <p>This is Section 2 content.</p>
        </section>
        ```
- Next.js Image Component
    - In traditional HTML to add an image a source URL is required and an alt can be added for a short description
        - One drawback is that the image resolution and file size are not optimized
    - Example
    -   ```javascript
        import imgDemo from "./img1_ex.jpg";
        import Image from "next/image";
        ...
        <Image src={imgDemo} alt="A Image" />
        ```
- Vercel
    - https://vercel.com/
    - provides a server for use that can take the code and be used publicly
    - Steps (Website Version)
        1. Login or Create an account on Vercel
        2. Import your repository (GitHub, GitLab, or Bitbucket).
        3. Configure the Project
        4. Deploy the Project
            - The preview URL should be -> https://your-project-name.vercel.app
        5. Continuous Deployment
            - Every time you push or update the repository linked to the Vercel it automatically rebuilds and redeploy the project
        6. Custom Domain (Optional)
            - Custom domain (e.g., mywebsite.com) -> Domains section & Add
        7. Monitor and Manage Deployments
            - Vercel has performance analytics
            - It can also monitor deployment status, view logs, or roll back previous versions
- Commands 
    -   ```
        npm run dev   # For development mode  
        npm run build # Build the project  
        npm start     # Start the production build
        ```
- Subdomains
    - After obtaining a domain any prefix(subdomain) before the actual domain is considered a subdomain
    - Example:  
    Main Domain : mywebsite.com 
    Subdomain : blog.mywebsite.com
    - Particularly used to separate different sections or services of a website
- DNS Records
    - A record 
        - Also known as Address Record 
        - points a domain to a IP address
        - The primary record for routing traffic to a website or server
        - Example:  
        Name  : @ or mywebsite.com  
        Value : 1.1.1.1
    - CNAME Record 
        - Also known as Canonical Name Record
        - Maps a subdomain to another domain name rather than an IP address
        - Used to point one domain or subdomain to another domain
        - Example:  
        Name  : www
        Value : mywebsite.com
    - MX Record
        - Also known as Mail Exchange Record
        - Directs email traffic to the mail servers
        - Example:  
        Name     :  @(root domain)
        Value    :  mail.mywebsite.com (mail server address)
        Priority :  10 (lower the higher the priority)
    - TXT Record
        - Also known as Text Record
        - Stores textual information for email validation, domain ownership verification, and security
        - Used for
            - SPF (Sender Policy Framework) prevents email spoofing
            - DKIM (DomainKeys Identified Mail) validates email messages
            - Domain Verification -> Google Search Console or SSL certificates.
        - Example:  
        Name  : @(root domain)  
        Value : v=DKIM1; p=MIGfMA0GCSqGSIb...
- Database
    - Allows for quick and easy storage of data and the ability to move, edit, and delete said data
    - For example for users, the information that needs to be stored in their login information
        - Such as email, username, password, etc
    - Or if it is a website for social interactions the comments and posts need to be also stored
    - Connection stream, API key, lets anyone with the key do anything on the database
    - The connection should be done serverside the client should not be able to connect to the database directly
    - SQL (structured query language)
        - structured
        - MYSQL
            - one of the most popular SQL database
    - NOSQL (non-structured query language)
        - flexible
        - MongoDB
            - one of the most popular no SQL database
- MongoDB Atlas
    - Atlas is a fully managed cloud database service 
        - that allows you to deploy, manage, and scale MongoDB clusters easily
    - Provides built-in security, backups, monitoring, and automation.
    - Steps -> [Website](https://www.mongodb.com/cloud/atlas/register)
        1. Create an Atlas Account
        2. Create a Cluster
            - Go to Database Deployments
            - Choose Shared (Free) or Dedicated (Paid) Cluster
            - Select a Cloud Provider (AWS, GCP, or Azure) and a Region
            - Choose the cluster tier (for free, select M0 (Free Tier))
            - Name your cluster and click "Create Cluster"
        3. Set Up Database Access
            - Go to Database Access
            - Add New Database User
            - Set a login (username and password)
            - Enable Read and Write Access
            - Add User
        4. Allow Network Access
            - Go to Network Access
            - Add IP Address
            - Enable Allow Access from Anywhere or Add the IP Manually
            - Confirm
        5. Connect to Your Cluster
            - Go to Database Deployments
            - Go to the Cluster
            - Connect with MongoDB Compass" (if using Compass) or "Connect using MongoDB Shell".
            - Copy the connection string
                - Example: `(e.g., mongodb+srv://<username>:<password>@cluster0.xxxx.mongodb.net/myFirstDatabase?retryWrites=true&w=majority)`
- MongoDB Compass
    - Graphical interface for interacting with MongoDB databases
    - Steps -> [Website](https://www.mongodb.com/products/tools/compass)
        1. Download and Install Compass
        2. Connect to Your MongoDB Atlas Cluster
            - Open MongoDB Compass
            - Connect to MongoDB by adding the connection string
            - Connect
- Environment Variables
    - Prevents hardcoding sensitive credentials (e.g., MongoDB connection strings)
    - Steps
        1. Create a .env File
        2. Add the MongoDB connection string
        3. Add it to .gitignore
