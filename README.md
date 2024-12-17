# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler can block the event loop, causing the server to become unresponsive.  The `bug.js` file contains the problematic code.  The solution, found in `bugSolution.js`, demonstrates how to use asynchronous operations to avoid this issue.

## How to Reproduce

1. Clone the repository.
2. Run `node bug.js`.
3. Try to access the server (e.g., using `curl http://localhost:3000` or a browser). You'll notice significant delays or unresponsiveness.

## Solution

The solution employs asynchronous programming techniques. This prevents the event loop from being blocked and enables the server to handle multiple requests concurrently without performance issues.