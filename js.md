# 9. Asynchronous JavaScript

## Q78. What is synchronous vs. asynchronous JavaScript? what's the difference? (P1)

Synchronous JavaScript executes code sequentially, meaning it waits for the current operation to finish before moving to the next operation. Asynchronous JavaScript allows certain operations, such as API requests, timers, or file operations, to be handled without blocking the execution of other JavaScript code. For example, when we use fetch() to make an API request, JavaScript can continue executing other code while waiting for the server response. Once the asynchronous operation is ready, its callback or promise continuation can be executed through the event loop.

## Q79. What is a callback? What is "callback hell," and how do Promises/async-await solve it? (P1)

A callback is a function that is passed as an argument to another function so that it can be executed later, usually after a particular operation is completed. Callbacks are commonly used to handle asynchronous operations.

Callback hell occurs when we have multiple asynchronous operations that depend on each other, causing callbacks to become deeply nested. This makes the code difficult to read, maintain, debug, and handle errors in.

Promises solve this problem by representing the eventual result of an asynchronous operation and allowing us to chain operations using .then() and handle errors using .catch(). async/await is built on top of Promises and provides cleaner and more readable syntax, making asynchronous code look similar to synchronous code. It also allows us to handle errors using the familiar try...catch syntax.

## Q80. What is a Promise? What are its states? How does chaining work? (P1)

A Promise is an object that represents the eventual result of an asynchronous operation. A Promise has three states: pending, fulfilled, and rejected. It starts in the pending state and eventually becomes either fulfilled if the operation succeeds or rejected if it fails. Once a Promise is fulfilled or rejected, its state cannot change again.

Promise chaining allows us to perform multiple asynchronous operations sequentially. We can use .then() to handle the result of a Promise, and each .then() returns a new Promise, which allows us to attach another .then(). If we return another Promise from a .then() callback, the next .then() waits for that Promise and receives its result. We can use .catch() to handle errors in the chain.

## Q81. What is async/await, and how does it differ from raw Promises internally? (P1)

## Q82. How do you handle errors with async/await vs. .then()/.catch()? (P1)

## Q83. What happens when an async function throws? What happens if you forget to await it? (P2)

## Q84. What is Promise.all()? What happens if one Promise inside it rejects? (P1)

## Q85. Difference between Promise.all, allSettled, race, and any? (P2)

## Q86. Difference between sequential and parallel API requests — how would you run several at once? (P2)

## Q87. How do you handle concurrent async requests with a concurrency limit? (P3)
