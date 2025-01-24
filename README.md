# Unresponsive Node.js Server

This repository demonstrates a common Node.js issue: an unresponsive server caused by a long-running synchronous operation within the request handler.  The `server.js` file contains the problematic code.  The `serverSolution.js` file provides a solution using asynchronous operations.

## Problem

The server.js code includes a `while` loop that simulates a 5-second delay.  This blocks the event loop, preventing the server from responding to other requests during this time.  This leads to unresponsive behavior and poor performance.

## Solution

The solution involves refactoring the code to use asynchronous operations or offloading the long-running task to a worker thread or a message queue to avoid blocking the main thread.