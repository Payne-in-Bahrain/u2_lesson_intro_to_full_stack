<img src="https://i.imgur.com/PE14J3Y.jpg">

# Intro to Full-Stack Development & HTTP

## Learning Objectives

| Students Will Be Able To: |
|---|
| Explain Full-Stack Web Development |
| Describe Client/Server Architecture |
| Explain the Anatomy of HTTP Requests and Responses |
| Identify the Two Key Components of an HTTP Request |
| Explain How HTTP Requests Can be Initiated From a Browser |
| Explain How HTTP Requests Result in Code Running on a Server |

## Road Map

1. Why Learn Full-Stack Web Development?
2. What is a Full-Stack Developer?
3. SEI Web Technology Stacks
4. Client/Server Architecture
5. What is HTTP?
6. Let's Make an HTTP Request
7. Anatomy of an HTTP Request/Response Messages
8. The Two Key Components of an HTTP Request
9. HTTP Methods
10. URLs
11. Ways to Send HTTP Requests From the Browser
12. How HTTP Requests Run Code on the Server
13. Essential Questions
14. Further Study

## 1. Why Learn Full-Stack Web Development?

According to U.S. News & World Report the second best job in 2021 was that of a **Software Developer**!  In [U.S. News & World Report - 100 Best Jobs of 2022](https://money.usnews.com/careers/best-jobs/rankings/the-100-best-jobs) it's the 5th best job - not bad! 

Further, according to [this 2021 StackOverflow Developer Survey](https://insights.stackoverflow.com/survey/2021#developer-type), **the role of Full-stack Developer is the most popular** as compared to other developer types.

Full-stack engineering roles are often some of the highest demand roles in the software engineering space. They are expected to be knowledgeable of many various topics in software engineering and it's often a great opportunity to increase you market value and learn more about the profession and what specific discipline you'll like to grow further.

The bottom-line is: **Full-stack Developers are in demand**!

## 2. What is a Full-Stack Developer?

A full-stack developer:

- Is a developer who is comfortable working with both frontend, middleware & back-end technologies.

- Can create full-stack applications by writing code that runs in both the browser and a web server.

- Will often **specialize** in frontend or back-end technologies.

- Is a graduate of Software Engineering Immersive!

## 3. SEI Web Technology Stacks

### Web Technology Stack - Unit 2

In this unit, we'll learn 3 of the 4 technologies that comprise the MERN-Stack:

<img src="https://i.imgur.com/FKGehuM.jpg">

### Web Technology Stack - Unit 3

In Unit 3, we'll learn:

<img src="https://i.imgur.com/GuogOfX.png">
<img src="https://i.imgur.com/MjX4aD7.png">

### Web Technology Stack - Unit 4

In Unit 4, we go full MERN-stack:

<img src="https://i.imgur.com/jlKEj7F.png">

## 4. Client/Server Architecture

<img src="https://i.imgur.com/clxiqnO.png">

The terms **client** and **server** can refer to both a **physical device** (computer, tablet, phone, etc.) but can also refer to a **software process**. For example:

- Database software such as PostgreSQL and web servers like Apache are examples of software processes behaving as servers.
- Browser software such as Chrome or Firefox are examples of software clients.
- Physical **servers** connected to the Internet are also referred to as **hosts**.
- Web developers usually think of a "web browser" when they hear "client".
- Often times you'll hear of servers being called **clients**. **Client** is used to define a piece of software that makes requests from another piece of software. It is important to realize that sometimes **clients** are also servers, and at times a server could play the role of **client** and **server**.

> Note: During development, your computer will play the role of BOTH client and web server.

## 5. What is HTTP?

**Hypertext Transfer Protocol (HTTP)** is an application-level network protocol that powers the communications across the [World Wide Web](https://en.wikipedia.org/wiki/World_Wide_Web), more commonly referred to as just **the Web**.

**HTTP is fundamental to web development** - regardless of which back-end or front-end web technology/framework is used.

When a user interacts with an amazing **web application** we developed, it's **HTTP** that informs the **web application** what the **browser** wants and it's **HTTP** that delivers the goods from the server back to the browser. For example, when the user browses to our app:

<img src="https://i.imgur.com/JDFHoZl.png" style="width:80%">

When the response is received by the client, that request/response cycle has ended and there will be no further HTTP communications unless another request is sent by the client.

> Note: It is helpful to note that http is not the only message transfer protocol used in software development. There are numerous alternative protocols all with their own advantages and disadvantages. Protocols like RPC(remote procedure calls), WS(websocket), HTTPS(hyper text transfer protocol secure), FTP(file transfer protocol), SMTP(simple mail transport protocol) among many others. Feel free to look into these alternatives to http at [w3schools types of protocols](https://www.w3schools.in/types-of-network-protocols-and-their-uses) as well as other places on the web, it is a very large topic with decades of development put into it. Keep in mind that these protocols are built on top of other protocols like TCP/ip or UDP/ip, however, we will not be diving too deeply into these topics in this course.

## 6. Let's Make an HTTP Request

Let's open a new tab in Chrome, open DevTools, and click on the **Network** tab where we can inspect HTTP requests and responses.

Now let's browse to General Assembly's site by typing **generalassemb.ly** in the address bar...

Wow! Each one of those lines represents a separate HTTP request made to a server!  Find the line in the left-side pane with **generalassemb.ly** and click on it:

<img src="https://i.imgur.com/fuED3VM.png" style="width:80%">

In the pane on the right you will find all of the information about a particular HTTP request. Select the **Headers** tab and explore!:

<img src="https://i.imgur.com/44W3zEE.png" style="width:80%">

## 7. Anatomy of HTTP Request/Response Messages

The following diagrams an HTTP Request and Response Message: 

<img src="https://i.imgur.com/kCuWuw7.png">

Notice they both have a **Start Line** followed by **Headers**, an **Empty line**, and finally the **Body** of the message.

### Components of an HTTP Request:

1. **Request Line:**
   - The first line of the request contains the HTTP method (e.g., GET, POST), the URL (Uniform Resource Locator) or URI (Uniform Resource Identifier) of the requested resource, and the HTTP version being used.
   - Example: `GET /path/to/resource HTTP/1.1`

2. **Headers:**
   - Headers provide additional information about the request or the client making the request. They are key-value pairs separated by colons.
   - Example:
     ```
     Host: www.example.com
     User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:97.0) Gecko/20100101 Firefox/97.0
     ```

3. **Body (Optional):**
   - The body of the request contains data sent by the client to the server, particularly in the case of POST, PUT, or other methods that allow sending data.
   - Example (for a POST request with form data):
     ```
     username=johndoe&password=secretpassword
     ```

4. **Parameters (Query String):**
   - For GET requests, parameters are often included in the URL as a query string. These parameters provide additional information to the server.
   - Example: `?page=1&limit=10`

5. **HTTP Method:**
   - Specifies the type of request being made (e.g., GET, POST, PUT, DELETE). It defines the operation the client wants to perform on the resource.
   - Example: `GET /path/to/resource HTTP/1.1`

6. **Cookies:**
   - Cookies can be included in the request headers. They are used to store state information on the client side.
   - Example:
     ```
     Cookie: sessionid=abc123; user=JohnDoe
     ```

7. **Authentication Information:**
   - If the server requires authentication, the client may include information such as usernames and passwords.
   - Example (using Basic Authentication):
     ```
     Authorization: Basic base64encoded(username:password)
     ```

These components together make up the structure of an HTTP request. It's important to note that not all components are present in every request; the presence of certain components depends on the type of request and the specific requirements of the server.

### Headers 

**What Are Headers?**
HTTP headers are like special notes that travel with your web requests and responses, providing instructions on how to handle the data. Headers can be compared to the address and instructions on an envelope accompanying your letter, or to specific requests like "no onions" when ordering food at a restaurant.

_Common Headers:_
1. **Content-Type:**
   - Specifies the type of data being sent, like labeling a package with its contents.

2. **CORS (Cross-Origin Resource Sharing):**
   - Acts like permissions, allowing or denying access to resources from different places.

3. **Cache-Control:**
   - Guides browsers and servers on how long they can store and reuse content.

Understanding headers ensures smooth communication between browsers and servers, much like making sure your letter or package reaches its destination correctly. As you dive into web development, you'll naturally become more familiar with these helpful instructions.

Imagine a conversation between you and a server:

- The **Body** is like the package you exchange:
  - When you send a request to the server (like asking for a webpage), you can include information in the Body, like filling out a form.
  - When the server responds, it also uses the Body to send back the requested data, such as the webpage you asked for, an image, or other content.

- The **Content-Type header** is like a label on the package:
  - It tells the browser what kind of data is inside the Body, so it knows how to handle it correctly.
  - Common types include:
    - `text/html`: The Body contains HTML code to display a webpage.
    - `image/png`: The Body contains a PNG image to show.
    - `application/json`: The Body contains structured data in JSON format.

Even though HTTP uses text for communication, the Body can carry various types of data, including images, videos, and other binary formats.

Think of it like receiving a package:

- The Body is the actual content inside the package (the gift, book, or whatever you ordered).
- The Content-Type header is the label on the package that tells you what's inside, so you know how to open and use it.
	
### The Status Code of the Response

The [status code](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html) in the first line of the response message informs us how the request/response went.

It is always a three-digit number that falls within the following ranges/categories:

- 1xx Informational
- 2xx Success
- 3xx Redirection
- 4xx Client Error
- 5xx Server Error

Most HTTP responses will have a status code of `200`, which means **OK**. You also might be familiar with the status code of `404` - **Not Found**.

## 8. The Two Key Components of an HTTP Request 

We saw earlier that every HTTP request message begins with a request-line like this:

```
GET /puppies HTTP/1.1
```

**The two key components of any HTTP request are**:

- The **HTTP method** (`GET` in the example above), and
- The **Path**/**Endpoint** (`/puppies` in the example), also referred to as the **URL** (although more accurately is a **URI**)

The reason these are the key components are because most web frameworks use them to match routes defined on the server (more on routes in a bit).

## 9. HTTP Methods

[HTTP methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods), are used to indicate the desired **action** to be performed for a given resource (specified by the URL) on the server.

The fact that they indicate **action** is why they are also at times called **HTTP Verbs**.

We'll be using the following HTTP Methods when we start defining our application's routes: 

| HTTP Method (Verb) | Desired Action on Server |
|:-:|:-:|
| `GET` | The GET method requests a representation of the specified resource (URL). Requests using GET should only retrieve data. |
| `POST` | The POST method is used to create a resource on the server. |
| `PUT` | The PUT method is used to update a resource on the server. |
| `DELETE` | The DELETE method deletes the specified resource. |

> note: There dozens of additional http verbs that you will likely encounter in your career. It is helpful to be aware of the most common http verbs and to understand how they can be used. See this documentation from [Mozilla's developer network](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods) that explains the 9 most common http verbs. If you choose to dig deeper and investigate the http protocol specifics, you'll see that there are about [39 different http verbs in http1.1](http://www.iana.org/assignments/http-methods/http-methods.xhtml). Even if an http verb is included in the protocol spec, that doesn't mean that all http clients will support all of these verbs, you most likely will not encounter the majority these verbs in your career, but it is helpful to understand how these protocols are designed and utilized.

## 10. URLs

**URL** stands for **Uniform Resource Locator**.

The URL informs the server of what resource the client wants to GET. create (POST), DELETE or UPDATE.

Here's the complete anatomy of a URL:

<img src="https://i.imgur.com/w1igQx0.png">

Developers often refer to just the **path** as a URL.

## 11. Ways to Send HTTP Requests From the Browser

These are ways that a browser can send an HTTP Request:

| Action | HTTP Method(s) Possible |
|---|---|
| Using the _address bar_ | GET |
| User submits an HTML form | POST, GET (used for searches) |
| User clicks a link | GET |
| Using JavaScript | All Methods can be sent using [AJAX](https://developer.mozilla.org/en-US/docs/Web/Guide/AJAX)|

**👀 In this unit our apps will rely on the user clicking links (`<a>` elements) and submitting forms (`<form>` elements) to interact with the app - that's it!**

## 12. How HTTP Requests Run Code on the Server

As full-stack web developers, we'll create user interfaces that display in the browser.

As a user interacts with the app by clicking links and submitting forms, they will cause HTTP requests to be sent to our back-end web application.

In our web app on the back-end, we will create **routes** that listen for these requests from the front-end, and...

Those routes will map HTTP requests to our back-end **code**!

As an example, you want your app to add a new user to your database when they sign up...

<img src="https://i.imgur.com/ltB5IYA.png">

1. The user submits the sign up form.

2. An HTTP request message with the form's data in the request body leaves the browser.

3. The HTTP request is received by the web app's routing and, in this case, would match the route defined to match a `POST /users` (**HTTP Method** & **Path**) HTTP request.

4. The purpose of a defined route is to map an HTTP request to code which is typically a function defined in the "controller" module.  The controller function would perform any necessary data operations, etc.

5. The controller function ultimately responds with an HTTP Response which can either:
    - Containing an HTML page in the message body (in the case of a GET request)
    - Or, with a Status Code of 302 (Redirect), make the browser issue a new GET request.

## 13. ❓ Essential Questions

<details>
<summary>
(1) What is the most common network protocol of the web?
</summary>
<hr>

**HTTP** (Hypertext Transfer Protocol)

<hr>
</details>

<details>
<summary>
(2) Name three HTTP methods/verbs.
</summary>
<hr>

**`GET`**, **`POST`**, **`PUT`** and/or **`DELETE`**

<hr>
</details>

<details>
<summary>
(3) What are the two key components of an HTTP Request that are typically used to match a route on the server?
</summary>
<hr>

The **HTTP Method/Verb** and the **Path/Endpoint/URL**

<hr>
</details>

<details>
<summary>
(4) Explain how an HTTP request makes code run on the server.
</summary>
<hr>

1. An HTTP Request leaves the browser due to user clicking a link, submitting a form or making an API request.

2. The HTTP Request matches a route in the app.

3. The route maps the request to code.

4. The code runs and ultimately sends an HTTP Response back to the browser.

<hr>
</details>

## 14. Further Study

### Ways to Send HTTP Requests Without Using the Browser

There are plenty of developer tools that enable us to issue HTTP requests to servers without using a browser. Pieces of software that perform http request are typically referred to as http **clients**.

- One tool we use later in the course is [Postman](https://www.getpostman.com/). Postman is a critical web development tool. It is extremely powerful and used almost universally across the web development field. Being competent in postman is a critical skill that will prove invaluable throughout your career. The postman team provides [exceptional documentation and guides](https://learning.postman.com/docs/getting-started/introduction/) for using their tool.

- If you prefer to use a command-line tool, most operating systems already have a tool called [cURL](https://en.wikipedia.org/wiki/CURL). If your computer doesn't have cURL installed, you may choose to install it. To learn more about cURL feel free to review this [cURL documentation](https://curl.se/docs/) as well as their [free PDF](https://everything.curl.dev/) that teaches you everything you'd want to know about cURL. Becoming a master of cURL is not a requirement to work in software engineering or mandated by this class, however, its presence is ubiquitous in the software engineering space and you will most likely encounter cURL in many online tutorials and during your career.

- A server with access to a network that supports http communication. We'll be using our node.js servers as http clients in this class when we cover the axios library.
