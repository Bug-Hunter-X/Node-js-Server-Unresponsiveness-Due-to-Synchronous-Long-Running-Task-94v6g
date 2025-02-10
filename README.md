# Node.js Server Unresponsiveness
This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler blocks the event loop, causing the server to become unresponsive.  The `bug.js` file contains the problematic code.  The solution, provided in `bugSolution.js`, demonstrates how to use asynchronous operations to prevent this blocking behavior.

## How to reproduce the bug:
1. Clone this repository.
2. Run `node bug.js`.
3. Try to access the server (e.g., using `curl http://localhost:3000` or a browser). You'll observe significant delays or the request might time out.

## Solution:
The solution involves using asynchronous operations, which allow other tasks to run concurrently without blocking the event loop. This ensures the server remains responsive.