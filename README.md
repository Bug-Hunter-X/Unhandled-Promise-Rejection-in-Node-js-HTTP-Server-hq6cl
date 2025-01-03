# Unhandled Promise Rejection in Node.js HTTP Server

This repository demonstrates a common error in Node.js: unhandled promise rejections in asynchronous operations within an HTTP server.  The provided code simulates an asynchronous operation that may fail.  Without proper error handling, the server might crash silently or behave unexpectedly.

## Bug

The `bug.js` file contains the buggy code.  The asynchronous operation (`asyncOperation`) lacks comprehensive error handling.  If the promise rejects, the error is logged to the console, but the HTTP response is not handled correctly, leading to a potential 500 error without a clear indication of the issue.

## Solution

The `bugSolution.js` file demonstrates the correct way to handle the potential error within the `.catch` block.  By providing a more informative response to the client and avoiding unhandled rejections, the server operates more reliably and provides better feedback to users in case of failures.