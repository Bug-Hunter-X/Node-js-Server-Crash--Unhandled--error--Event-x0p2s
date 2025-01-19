# Node.js Server Crash: Unhandled 'error' Event

This repository demonstrates a common but easily overlooked error in Node.js server development: unhandled exceptions during request processing.  The server crashes without providing much useful information in the console.

## The Problem

The `server.js` file contains a simple HTTP server.  However, it lacks proper error handling.  If an unexpected error occurs during request processing, the server will crash without logging the error details.

## The Solution

The `server-solution.js` file demonstrates a more robust approach. By adding an `'error'` event listener to the server, we can catch and log any errors, preventing crashes and providing valuable debugging information.

## How to Reproduce

1. Clone this repository.
2. Navigate to the project directory in your terminal.
3. Run `node server.js`
4. Send a request to the server that may trigger an error (e.g., try accessing a non-existent file).

Observe that the server crashes without informative logs.

Now run `node server-solution.js` and repeat step 4.  You'll see that errors are now logged to the console, allowing you to more easily identify and fix the issue.
