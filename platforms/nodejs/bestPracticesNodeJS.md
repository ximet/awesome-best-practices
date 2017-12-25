# NodeJS Best Practices

- #### Understand the Event Loop
     It is necessary to understand how it works and how it interacts with it. See picture:
     ![alt text](https://raw.githubusercontent.com/azat-co/nc-posts/master/how-event-loop-really-works/images/event-loop.png "Event Loop NodeJS")

***

- #### Use try-catch

   Try-catch is a JavaScript language construct that you can use to catch exceptions in synchronous code. Use try-catch, for example, to handle file(JSON, org and other) parsing errors as shown below.

***

- #### Don’t use synchronous functions

   Synchronous functions and methods tie up the executing process until they return.

***

- #### Use ES2015

   A year passed and ES2015 support grew to 99% with Node v6.

***

- #### Use Promises

   Promises will handle any exceptions (both explicit and implicit) in asynchronous code blocks that use then()

***

- #### Use JS CodeStyle

   For the help this point use:
    - ESLint
    - JSHint

***


- #### Use JWT for your REST API

   JWT consist:
    1. Header
    2. Payload
    3. Signature for your payload

***

- #### Use HTTP Methods for your RESTful API

***

- #### Use a small subset HTTP status codes

   For example only main status code:
    200. OK status
    201. Created
    304. Not Modified
    400. Bad Request
    401. Unauthorized
    403. Forbidden
    404. Not Found
    500. Internal Server Error

***

- #### Pick good framework for your NODE.js REST API

   Frameworks:
    1. Express
    2. Koa
    3. Restify - for build strict API services
    4. Hapi

***

- #### Test your NODE.js REST APIs

***

- #### Create documentation for your NODE.js REST APIs

***
___
## Video link with best practices:

1. [JavaScript best practices, Node.js, and how to end poverty with Eric Elliott](https://www.youtube.com/watch?v=pVNagJzzaFg) - 17 Jun. 2015
2. [Panel: Best Practices for Contributing to Node.js Core - James Snell, IBM](https://www.youtube.com/watch?v=sZdPHi5EMKI) - 24 Sep. 2016
3. [Best Practices using TypeScript with Node.js by Bryan Hughes, Microsoft](https://www.youtube.com/watch?v=ATUvAQZaTbM) - 15 Dec. 2016
