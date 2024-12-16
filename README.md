# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js servers: unresponsiveness caused by a long-running operation that blocks the event loop.  The `bug.js` file contains code that simulates this problem.  The solution, in `bugSolution.js`, illustrates how to address it using asynchronous programming.

## Problem

Node.js is single-threaded.  A long-running operation within the request handler prevents the event loop from processing other requests, leading to unresponsiveness.  The provided `bug.js` example simulates this by using a `while` loop to consume CPU time for 5 seconds before responding.

## Solution

The solution involves using asynchronous programming techniques such as `setTimeout`, `setInterval`, or promises to avoid blocking the event loop.  The `bugSolution.js` file presents an example that addresses this by using `setTimeout` to simulate an asynchronous task.