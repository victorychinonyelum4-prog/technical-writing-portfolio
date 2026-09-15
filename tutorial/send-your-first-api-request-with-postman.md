# Send Your First API Request With Postman: A Step-by-step Guide for Beginners
API testing isn't a niche activity. In [Postman’s 2025 State of the API report](https://www.postman.com/state-of-api/2025/?utm_source), 81% of respondents said they test APIs. Developers and testers have sent API requests to interact with and test functionality exposed by an API. Developers can use API requests to retrieve, edit, or delete data, debug errors, and understand how an API behaves before connecting it to other software.

In this tutorial, you'll learn how to send your first API request using Postman, understand the response you receive, and avoid common beginner mistakes.
## What You'll Need
Before you send any API requests, here are a few things you’ll need:
- A computer with internet access.
- A free Postman account — use the web version at postman.com or install the desktop app.
- A free public API to practice with. For this tutorial, we’ll use the Bored API’s random activity endpoint: https://bored-api.appbrewery.com/random.

I chose Bored’s API because it’s simple and easy to read; most importantly, it’s a public API — anyone with the URL can access it.
## What is an API Request?
An API request is a message sent by a client — such as Postman — to an API server to request information or to perform an action. 

The flow is simple: the client sends a request → the server sends back a response.

Think of ordering at a restaurant. You (client) give your order to the waiter. The kitchen (server) prepares it, and the waiter brings back your food (the response). 
Servers and applications follow a shared set of rules called HTTP to exchange these messages over the internet.
An API request can contain several pieces of information, including:
- URL: The address of the API endpoint you want to send the request to.
- HTTP method: Tells the API what kind of operation the client wants to perform, such as `GET` or `POST`.
- Headers: Provide additional information about the request.
- Body: Contains data sent with the request when the API requires it — usually for `POST` and `PUT` request methods.
- Parameters: Provide additional values that can modify or identify the request resource.
  
The response also contains important information, including a status code, headers, when applicable, and a response body.
## Key Components of an API Request and Response
An API request and its response are both built from a few core pieces — here's what each one does.
### The HTTP methods
HTTP methods tell an API what kind of operation the client wants to perform. Here are the most common methods and what they do:
| Methods | Common purpose |
|---|---|
| `GET` | Retrieves information from the server |
| `POST` | Sends data to create a resource or perform an action |
| `PUT` | Replace existing information |
| `PATCH` | Partially updates a resource |
| `DELETE` | Removes information from the server |

For example, a `GET` request might retrieve a customer’s profile, while a `POST` request might create a new customer. The exact behavior depends on how an API is designed, so you should always check the API’s documentation before sending a request.
### Headers
Headers provide additional information about a request or response.
For example, a request might include an `Authorization` header containing credentials or an API token. A request can also include a `Content-Type` header to indicate the format of the data being sent.
### Body
The request body contains data that the client sends to the API.
For example, a POST request might include a JSON body containing information needed to create a new user.
GET requests commonly don't require a request body, while POST, PUT, and PATCH requests commonly use one.
### Status Codes
A status code is a three-digit number that tells the client what happened when the server processed the request. For example:
- `200 OK` — means the request was successful.
- `201 Created` — The request successfully created a resource.
- `404 Not Found` — The requested resource or endpoint could not be found. 
- `500 Internal Server Error` — The server encountered an unexpected problem.
## How to Send an API Request Using Postman?
Postman is an API client that lets you create and send API requests and inspect the responses.
You can use the Postman desktop app or web app. Postman recommends the desktop app for the full experience, while the web app can also be used for many API tasks:
1.	**Open Postman**: Go to Postman. At the top right, click Sign up for free and register.
2.	**Create a new request tab**: After signing in, you’ll land in your default workspace — usually named My Workspace. Open it, then click the Add (+) icon to open a new request tab.
   <img width="1365" height="637" alt="Request new tab" src="https://github.com/user-attachments/assets/becde4b8-c8e4-42d5-958b-15f1eaa29591" />

3.	**Choose a request method**: In the request tab, you'll see a method dropdown next to the URL field. Select `GET`. Enter your endpoint in the URL field: https://bored-api.appbrewery.com/random
   <img width="1365" height="647" alt="postman downdrop" src="https://github.com/user-attachments/assets/3260fe56-a73f-4077-b3b0-5f7c4161b5f6" />

4. **Send the request**: Click Send
5.	**Read the response in the panel below**.
   <img width="1362" height="635" alt="postman respond" src="https://github.com/user-attachments/assets/9e6165d7-05d1-4c1e-8314-659297dc2e2a" />
   
6.	**Save your request**: Click Save next to the Send button, then choose or create a collection to store it. Collections let you organise related requests together, so you can find and reuse them later.
## Understanding The Response
The Bored API replies in JSON (JavaScript Object Notation). Postman can display other formats such as XML, HTML, and YAML, but JSON is widely used for exchanging structured data because it’s relatively easy for both people and programs to read.
### Status Codes
At the top of the response panel, you will see `200 OK`. This means the request worked and there were no errors.
### Time and Size
Next to the status, you will see something like 2.37s and 1.15KB. The response took 2.37 seconds and is 1.15 kilobytes in size. Note: This doesn’t mean all responses might be at 2.37 seconds; it depends on how long yours took to respond.
### The Response Body
- `activity` — the suggested activity, for example "Meditate for five minutes"
- `availability` — how readily available the activity is
- `type` — the category, for example "relaxation"
- `participants` — how many people the activity needs
- `price` — the relative cost, where 0 means free
- `accessibility` — how difficult the activity is to do
- `duration` — how long it takes
- `kidFriendly` — whether the activity is suitable forchildren
- `link` — an optional related link
- `key` — a unique identifier for the activity
## Common Beginner Mistakes
- Choosing the wrong HTTP method: Before you click Send, be clear on your goal. The method you use to retrieve data is not the one you use to send data. For example, GET is commonly used to retrieve data, while POST is commonly used to create or submit data. The API documentation should tell you which method to use for each endpoint.
- Typing the wrong URL: A misspelling or incorrectly capitalised URL path can cause a `404 Not Found` error instead of the expected response.
- Confusing status code: Don't assume every error means Postman is broken. Check the method, URL, parameters, authentication, and the API's documentation first.
## Wrapping Up
You have now sent your first API request. You chose a method, entered an endpoint, sent the request, and read the response. That is the same process developers and testers use every day.
Save your request to a collection, then try a different public API and see what comes back.

To learn more about how API responses work, check out [What happens when you send an API request](github.com/victorychinonyelum4-prog/technical-writing-portfolio/blob/main/explanation/what-happens-when-you-send-an-api-request.md)
