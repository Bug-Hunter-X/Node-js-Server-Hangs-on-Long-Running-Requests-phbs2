# Node.js Server Hang Issue

This repository demonstrates a common Node.js issue: server hangs due to long-running operations blocking the event loop. The `server.js` file contains the problematic code, while `serverSolution.js` provides a solution using asynchronous operations and promises to prevent the event loop from being blocked. 

## Problem

The original server code performs a long-running task (a 5-second delay) directly within the request handler. This blocks the event loop, preventing the server from responding to other requests or handling events. 

## Solution

The solution involves using asynchronous operations and Promises to avoid blocking the event loop. The `serverSolution.js` file demonstrates this approach. 

## How to Run

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `node server.js` (original buggy code) or `node serverSolution.js` (fixed code) to start the server.
4. Send requests to the server using a tool like `curl` or a web browser.