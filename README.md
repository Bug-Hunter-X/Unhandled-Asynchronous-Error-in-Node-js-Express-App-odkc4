# Unhandled Asynchronous Error in Node.js

This repository demonstrates a common error in Node.js applications involving unhandled errors within asynchronous operations.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

The original code simulates an asynchronous operation (using `setTimeout`) that may throw an error.  Because the error is thrown within the asynchronous callback, it isn't caught by a `try...catch` block in the main thread, causing the server to crash.

## Solution

The solution uses proper error handling techniques for asynchronous code.  By placing the asynchronous operation within a `try...catch` block and implementing proper error handling within asynchronous callbacks, you prevent the server from crashing and allow for more graceful error management.

## How to Run

1. Clone the repository
2. Navigate to the directory
3. Run `node bug.js` (observe the crash)
4. Run `node bugSolution.js` (observe the graceful error handling)