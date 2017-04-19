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

___
## Video link with best practices:

1. [JavaScript best practices, Node.js, and how to end poverty with Eric Elliott](https://www.youtube.com/watch?v=pVNagJzzaFg) - 17 Jun. 2015
2. [Panel: Best Practices for Contributing to Node.js Core - James Snell, IBM](https://www.youtube.com/watch?v=sZdPHi5EMKI) - 24 Sep. 2016
3. [Best Practices using TypeScript with Node.js by Bryan Hughes, Microsoft](https://www.youtube.com/watch?v=ATUvAQZaTbM) - 15 Dec. 2016
