# Frontend vs. Backend: A Simple Guide for Beginners

In this article, you'll learn the difference between frontend and backend, what each one does, and how they work together in a web application.

Most modern web applications have a frontend and a backend that work together. A frontend is everything a user sees and interacts with, while the backend is the engine behind it that you don't see.

## What is the frontend?

The frontend, also known as the client-side, is the part of a web application that runs on the user's device, usually in a web browser, and provides the interface they see and interact with.

It creates the visual elements, including images, design, colors, text fields, and even animations. The frontend handles the interface users see and the interactions they perform, such as clicking buttons, filling out forms, and navigating between pages.

The three main technologies used to build the visual part of a website (frontend) are HTML (HyperText Markup Language), CSS (Cascading Style Sheets), and JavaScript.

- HTML is used to create structure and content.
- CSS controls presentation, such as layout, colors, spacing, and typography.
- JavaScript adds behavior and interactivity to the frontend, such as responding to user actions and updating the page.

For example, consider building a house: HTML is the structure of the house. CSS is the paint, layout, and decoration, while JavaScript adds behavior — making a door open when you click a button.

All of these add visual elements to a web page. But a web page that has only beautiful designs, colors, and text can't store data. It can't search for information or respond to you by itself. That's where the backend comes in.

## What is the backend?

The backend, also known as the server-side, is the part of an application that runs on a server and handles processing that shouldn't happen directly in the user's browser. It can process requests, apply business logic, communicate with databases and other services, and return data or other results to the frontend.

The backend pulls data from the database and sends it to the frontend. The frontend then displays it to the user via HTML/JavaScript. Unlike the frontend, which runs in the browser, the backend works behind the scenes on a server.
Examples of backend technologies include ASP.NET Core with C#, Django with Python, Laravel with PHP, Express.js with JavaScript, and Ruby on Rails with Ruby.

The backend can handle tasks such as processing requests, storing and retrieving data, authenticating users, controlling access to resources, sending emails, and applying business rules.

Now that you understand what the frontend and backend do separately, let's look at how they work together in a typical web application.

## How they work together
 <img width="924" height="386" alt="How frontend and backend works together-diagram" src="https://github.com/user-attachments/assets/ad4aced1-4ef1-4913-bdcd-26212a511b91" />

The frontend and backend work together to make a web application function. An API defines how the frontend communicates with the backend, while the backend may communicate with a database to retrieve or store data.

For example, Amazon is a massive global company. The frontend is the showroom — the part customers see and interact with, like the products, buttons, images, and layout.
The backend is the warehouse behind the scenes. It handles things like inventory, payments, orders, and other data the customer doesn't see.

The API is like the store clerk connecting the two. When you click Add to Cart, the frontend sends the request through the API to the backend, which checks the product and processes the request. The backend then sends the result back to the frontend for you to see.

In short:

- **Frontend:** what the user interacts with.
- **API:** Defines how software components communicate.
- **Backend:** processes requests and applies business logic.
- **Database:** stores and retrieves persistent data.

## Frontend vs. Backend

Here's a quick reference of the differences between frontend and backend:

| Objectives | Frontend | Backend |
|---|---|---|
| Where it runs | It runs in the browser and on devices | It runs on the server |
| Common technologies | HTML, CSS, and JavaScript | PHP, Python, Ruby, C#, and JavaScript |
| Main responsibility | Provides the user interface and handles user interactions | Processes requests, applies business logic, and works with data |
| Examples of tasks | Displaying data, handling form interactions, updating the interface | Authenticating users, processing orders, querying a database |

## Key Takeaways

The frontend (client-side) is the part of a web application that users see and interact with, such as buttons you click, the design, and colors. It handles the interface, user interactions, and presentation of information.

The backend (server-side) is the logical system behind every interaction you make with a website. It runs on a server and handles processing, business logic, and communication with data sources such as databases. An API acts as the bridge, carrying data between the backend and the frontend for display.

## FAQs

### Are HTML and CSS programming languages?

No. HTML is a markup language that gives semantics and structure to content, while CSS is a stylesheet language used to control presentation and apply styles to the HTML. JavaScript is a programming language that can add logic and interactivity.

### Is JavaScript only for frontend development?

No. JavaScript is used in both frontend and backend.

### Is an API a third thing?

An API isn't necessarily a separate layer alongside the frontend and backend. It defines how software components communicate. In a typical web application, the frontend may use an API to communicate with the backend.

### What does an API look like in code?

An API is usually accessed by sending a request to an endpoint. For example, a frontend might send a `GET` request to `/users` to retrieve user information. You don't need to understand the code behind the API to understand its basic role: it defines how one piece of software can communicate with another.

### Is a full-stack developer an expert at both frontend and backend?

Not necessarily. A full-stack developer works on both the frontend and backend of an application. They may be highly skilled in both, but their level of expertise can differ between the two areas.
