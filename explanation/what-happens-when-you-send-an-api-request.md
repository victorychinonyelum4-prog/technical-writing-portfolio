# What Happens When You Send an API Request?
Every time you check the weather on your phone, order food, or ask ChatGPT a question, an API request happens behind the scenes. That invisible exchange is what connects the apps and tools we use every day.

In this guide, we will break down what an API is, how a request travels through the system, and how to read the JSON response that comes back.

## What is an API?
API stands for Application Programming Interface:
- Application: Any software program built to perform a specific job.
- Interface: A shared boundary that lets two systems communicate.
Put simply, an API is a set of rules and protocols that allows different software applications to talk to each other, exchange data, and trigger actions. Developers writing in languages like JavaScript, Python, and Go use APIs to pull data from external servers, rather than rebuilding entire databases from scratch.
## Real-World Examples
You trigger APIs throughout your day without realizing it:
- ChatGPT: When you type a prompt, your browser sends an API request to OpenAI's servers, which process the prompt and stream back the text response.
- Hotel Booking Apps: When you search for hotels in Lagos, the app calls hotel database APIs across different providers to compare prices and availability in real time.
- Social Media & Video: When a website embeds TikTok videos or tracks view metrics, it communicates directly with TikTok's API.
## The Anatomy of an API Request
Every API transaction has two main halves: the Request (what you send) and the Response (what comes back).

To build a request, the client needs two critical pieces of information: an endpoint and an HTTP **(Hypertext Transfer Protocol)** method.
### The Endpoint
An endpoint is the specific web address (URL) on a server where a client goes to access a resource.
Imagine a restaurant app hosted at `https://api.restaurant.com`. If you want to view their menu, the endpoint might look like this:
<https://api.restaurant.com/restaurants/123/menu>
The base domain (`https://api.restaurant.com`) routes to the server, while the path (`/restaurants/123/menu`) tells the server exactly which restaurant and resource you want.
### The HTTP Method
The method tells the server what action to perform on that resource. The four most common methods are:
| Method | Action | Example |
|---|---|---|
| GET | Retrieve a resource | Fetch the menu |
| POST | Create a resource | Place a new food order |
| PUT | Replace a resource | Replace a customer profile |
| DELETE | Remove a resource | Cancel an order |
### Headers
Headers carry metadata about the request. They don’t contain the main data, but rather instructions and context for the server:
- `Authorization`: Passes an API key or bearer token to prove who you are (preventing `401 Unauthorized` errors).
- `Content-Type`: Tells the server the format of the data you are sending, usually `application/json`.
### The Body (Payload)
While `GET` and `DELETE` requests usually don't need data attached, `POST` and `PUT` requests do. The body carries the actual data you want to send to the server—like a new customer profile or items in a shopping cart.
## What Happens When the Request Travels?
When you click a button or send a command via [cURL](https://curl.se/) or [Postman](https://www.postman.com/), the request follows a predictable path:
- **DNS Lookup:** Before sending anything, your device asks a Domain Name System (DNS) server to translate the human-friendly URL (`api.restaurant.com`) into a machine-readable Internet Protocol address (IP address).
- **Sending the Request:** The client connects to that IP address over HTTP/HTTPS, sending along the method, endpoint, headers, and any body payload.
- **Server Authentication & Validation:** The server inspects the request headers to verify your identity and checks whether you have permission to access the resource.
- **Fulfilling the Action:** The server processes your request and interacts with its database to fetch, create, or update the required records.
- **Returning the Response:** The server sends a response containing an HTTP status code (like `200 OK`) and, when applicable, a response body. Many modern APIs use JSON (JavaScript Object Notation) format to structure data.
## Understanding API response
When the server responds, it typically sends back two things: an HTTP Status Code and a JSON payload.
### HTTP Status Codes
Status codes are three-digit numbers indicating whether the request succeeded or failed:
- 200s (Success):
    - `200 OK`: The request succeeded and returned the requested data.
    - `201 Created`: The server successfully created a new resource (e.g., your order was placed).
    - `204 No Content`: The action succeeded, but there is no body data to return (common after deletes).
- 400s (Client Errors):
    - `400 Bad Request`: The request syntax or body was invalid.
    - `401 Unauthorized`: Authentication failed, or an API key was missing.
    - `404 Not Found`: The requested endpoint or resource does not exist.
- 500s (Server Errors):
    - `500 Internal Server Error`: Something went wrong on the server while processing the request.
    - `503 Service Unavailable`: The server is overloaded or down for maintenance.
### The JSON Body
JSON is a lightweight data-interchange format. It is easy for humans to read and write, and easy for machines to parse and generate. JSON represents data using key-value pairs and supports common data types such as strings, numbers, booleans, arrays, objects, and `null`.

JSON is structured as key-value pairs:
```json
{
  "restaurant": "Mama's Kitchen",
  "isOpen": true,
  "rating": 4.8,
  "menu": [
    {
      "name": "Jollof Rice",
      "price": 2500
    },
    {
      "name": "Fried Rice",
      "price": 3000
    }
  ]
}
```
Notice the data types:
- Strings: Text wrapped in double quotes (`"Mama's Kitchen"`).
- Numbers: Unquoted digits (`2500`).
- Booleans: `true` or `false` (`"isOpen": true`).
- Arrays: Ordered lists inside square brackets (`[...]`).
- Objects: Key-value groups enclosed in curly braces (`{...}`).

This mix of strings, numbers, objects, arrays, and booleans is common in JSON responses.
## Types of Web APIs
APIs can also be categorized by how they are accessed or how they combine operations. APIs fall into four primary categories:

- Open APIs (Public APIs): Publicly accessible endpoints that anyone or any registered developer can consume.
- Internal APIs (Private APIs): Used strictly within an organization to let internal teams, microservices, and databases communicate.
- Partner APIs: Shared only with authorized external business partners who have contracts or integration agreements.
- Composite APIs: APIs that bundle calls to multiple endpoints into a single request, speeding up workflows and reducing network round-trips.
## Wrapping Up
APIs can sound intimidating until you break them down: a request goes out, a server does something with it, and a response comes back as structured JSON with a status code letting you know how it went.

Once you recognize those core pieces—the endpoint, the method, and the response—reading developer documentation stops feeling foreign. You start seeing the same reliable pattern across every tool and web app you encounter.
